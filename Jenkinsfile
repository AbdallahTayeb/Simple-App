pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                echo 'Préparation de l\'environnement...'
                sh 'python -m venv venv'
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
