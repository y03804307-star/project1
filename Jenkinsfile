pipeline {
    agent any

    tools {
        nodejs "NodeJS"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build React App') {
            steps {
                bat 'npm run build'
            }
        }

        stage('SonarQube Scan') {
            steps {
                script {
                    def scannerHome = tool 'SonarScanner'
                    withSonarQubeEnv('SonarQube') {
                        bat """
${scannerHome}\\bin\\sonar-scanner.bat ^
-Dsonar.projectKey=MyFirstProject ^
-Dsonar.projectName=MyFirstProject ^
-Dsonar.sources=src ^
-Dsonar.host.url=http://localhost:9000
"""
                    }
                }
            }
        }
    }
}