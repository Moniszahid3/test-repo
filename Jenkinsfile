pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from GitHub
                git branch: 'main', url: 'https://github.com/Moniszahid3/test-repo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Upgrade pip and install Flask using Windows batch commands
                bat 'python -m pip install --upgrade pip'
                bat 'python -m pip install flask'
            }
        }

        stage('Run Application') {
            steps {
                // Run the Flask app in the background
                bat 'start python views.py'
            }
        }
    }
}
