pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Gradle'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit Tests using TestComplete'
                echo 'Integration Tests using TestComplete'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Code analysis using FindBugs'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Code security check using Flawnter'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy in dev server in EC2'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration tests on the staging environment'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy in production server in EC2'
            }
        }
    }
}
