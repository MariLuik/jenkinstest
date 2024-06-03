// Jenkinsfile task 6.1C Mari Luik

pipeline {
    agent any
    environment {
        DIRECTORY_PATH= "/Users/mari/Library/Mobile Documents/com~apple~CloudDocs/UNI/SIT223 Prof practice in IT/tasks/6.1C"
        MAVEN_HOME = "/path/to/maven"
        POSTMAN_HOME = "/path/to/postman"
        CODACY_API_KEY = "codacy_api_key"
        ZAP_HOME = "/path/to/zap"
        GOOGLE_APPLICATION_CREDENTIALS = "/path/to/google/credentials.json"
        PROJECT_ID = "google_cloud_project_id"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
                echo 'mvn clean install'
            }
        }
        stage('Unit and integration tests') {
            steps {
                echo 'Running unit tests using JUnit'
                echo 'mvn test'
                echo 'Running integration tests using Postman'
                echo 'postman-command'
            }
            post {
                success {
                    mail to: 'mariluik@gmail.com',
                         subject: 'Unit and integration test status Email',
                         body: 'Unit and integration testing has been successfully completed!'
                }
                failure {
                    mail to: 'mariluik@gmail.com',
                         subject: '!ATTENTION! Unit and integration test status Email',
                         body: 'Unit and/or integration testing has failed!'
                }
            }
        }
        stage('Code analysis') {
            steps {
                echo 'Analyzing code using Codacy'
                echo 'codacy-command'
            }
        }
        stage('Security scan') {
            steps {
                echo 'Performing security scan using OWASP ZAP'
                echo 'zap-command'
            }
            post {
                success {
                    mail to: 'mariluik@gmail.com',
                         subject: 'Security scan status Email',
                         body: 'Security scan was successfully completed!'
                }
                failure {
                    mail to: 'mariluik@gmail.com',
                         subject: '!ATTENTION! Security scan status Email',
                         body: 'Security scan has failed!'
                }
            }
        }
        stage('Deploy to staging') {
            steps {
                echo 'Deploying to Google Cloud Compute Engine for staging...'
                // insert deployment commands for Google Cloud Compute Engine here
            }
        }
        stage('Staging integration tests') {
            steps {
                echo 'Running integration tests on staging environment using Postman'
                // insetrt postman-command here
            }
            post {
                success {
                    mail to: 'mariluik@gmail.com',
                         subject: 'Staging integration test status Email',
                         body: 'Staging integration testing was successfully completed!'
                }
                failure {
                    mail to: 'mariluik@gmail.com',
                         subject: '!ATTENTION! Staging integration test status Email',
                         body: 'Staging integration testing has failed!'
                }
            }
        }
        stage('Deploy to production') {
            steps {
                echo 'Deploying to Google Cloud Compute Engine for production...'
                // insert deployment commands for Google Cloud Compute Engine here
            }
        }
    }
}
