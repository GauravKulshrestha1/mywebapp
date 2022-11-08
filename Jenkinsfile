pipeline {
    agent any
    tools {
        maven "3.8.6"
    }
    stages {
        stage('Clean and Install') {
            steps {
               bat 'mvn clean install apache-rat:check -Drat.numUnapprovedLicenses=600 package -D maven.javadoc.skip=true assembly:single -Dhadoop.profile=2'
            }
        }
        stage('Package') {
            steps {
               bat 'mvn package'
            }
        } 
    }
}
