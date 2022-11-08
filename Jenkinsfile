pipeline {
    agent any
    tools {
        maven "3.8.6"
    }
    stages {
        stage('Clean and Install') {
            steps {
               bat 'mvn clean install apache-rat:check -Drat.numUnapprovedLicenses=600 package'
            }
        }
        stage('Package') {
            steps {
               bat 'mvn package'
            }
        } 
    }
}
