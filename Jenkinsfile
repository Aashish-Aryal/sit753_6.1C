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
            post {
                success {
                    emailext subject: "Test Success",
                        body: "The tests have passed successfully.",
                        to: "s224158554@deakin.edu.au"
                }
                failure {
                    emailext subject: "Test Failure",
                        body: "The tests have failed. Please check the logs for details.",
                        to: "s224158554@deakin.edu.au",
                        attachLog: true
                }
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
            post {
                success {
                    emailext subject: "Security Scan Success",
                        body: "The Security Scans have passed successfully.",
                        to: "s224158554@deakin.edu.au"
                }
                failure {
                    emailext subject: "Security Scan Failure",
                        body: "The Security Scans have failed. Please check the logs for details.",
                        to: "s224158554@deakin.edu.au",
                        attachLog: true
                }
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
