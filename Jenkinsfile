pipeline {
    agent any

    stages {
        stage('Install Python') {
            steps {
                echo 'Installation de Python...'
                // Adaptez cette commande en fonction de l'environnement de votre agent Jenkins
                sh 'apt-get update && apt-get install -y python3 python3-venv'
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

stage('Test') {
            steps {
                echo 'Exécution des tests...'
                // Ici, vous pouvez exécuter des tests réels si disponibles.
                // Pour cet exemple, nous allons simplement vérifier que Python fonctionne.
                sh 'python --version'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Déploiement de l\'application...'
                // Ici, vous pouvez ajouter des étapes de déploiement.
                // Pour cet exemple, nous allons simplement lancer l'application.
                sh 'python app.py &'
            }
        }
    }
}
