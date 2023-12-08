pipeline {
    agent any

    stages {
        stage('Install Python') {
            steps {
                echo 'Installation de Python...'
                // Adaptez cette commande en fonction de l'environnement de votre agent Jenkins
                sh 'sudo apt-get update && sudo apt-get install -y python3 python3-venv'
            }
        }

        stage('Setup') {
            steps {
                echo 'Préparation de l\'environnement...'
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate'
            }
        }

        stage('Build') {
            steps {
                echo 'Installation des dépendances...'
                sh 'pip install -r requirements.txt'
            }
        }

        // Reste du Jenkinsfile...
    }
}
