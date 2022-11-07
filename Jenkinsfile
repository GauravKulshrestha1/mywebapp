pipeline {
    agent any
    tools {
        maven "3.8.6"
    }
    stages {
        stage('Clean and Install') {
            steps {
               bat 'mvn clean install -Drat.numUnapprovedLicenses=500'
            }
        }
        stage('Package') {
            steps {
               bat 'mvn package'
            }
        } 
    }
}
