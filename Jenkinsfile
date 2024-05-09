pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build the code using Maven
                echo 'Building the code using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Run unit and integration tests using JUnit
                echo 'Running unit and integration tests using JUnit'
            }
        }
        stage('Code Analysis') {
            steps {
                // Integrate a code analysis tool (e.g., SonarQube) to analyze the code
                echo 'Integrating SonarQube for code analysis'
            }
        }
        stage('Security Scan') {
            steps {
                // Perform a security scan using a tool like OWASP ZAP or SonarQube
                echo 'Performing security scan using OWASP ZAP'
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploy the application to a staging server (e.g., AWS EC2 instance)
                echo 'Deploying the application to staging server'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Run integration tests on the staging environment
                echo 'Running integration tests on staging environment'
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy the application to a production server (e.g., AWS EC2 instance)
                echo 'Deploying the application to production server'
            }
        }
    }

    post {
        always {
            // Send notification emails at the end of test and security scan stages
                emailext attachLog: true, body: "${currentBuild.result}: ${BUILD_URL}", compressLog: true, 
                         subject: "Build Notification: ${JOB_NAME}-Build# ${BUILD_NUMBER} ${currentBuild.result}", to: 'sumitsainiuiet@gmail.com'
                }
                
    }
}

