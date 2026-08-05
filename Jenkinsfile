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

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-react-app .'
            }
        }

        stage('Tag Docker Image') {
            steps {
                bat 'docker tag my-react-app yasmeen7847/my-react-app:latest'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push yasmeen7847/my-react-app:latest'
            }
        }
    }
}pipeline {
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

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-react-app .'
            }
        }

        stage('Tag Docker Image') {
            steps {
                bat 'docker tag my-react-app yasmeen7847/my-react-app:latest'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push yasmeen7847/my-react-app:latest'
            }
        }
    }
}