
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Utilisation des credentials pour cloner le dépôt GitHub
                git credentialsId: '5a7c9d41-962d-44ca-8a27-49348f8b6e59', url: 'https://github.com/garcin21/projet-maven.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the app...'
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the app...'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the app...'
                // Remplacez par la commande réelle de déploiement
                sh 'scp target/myapp.war user@server:/path/to/deploy'
            }
        }
    }
}
