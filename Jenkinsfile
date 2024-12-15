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
                // Use the full path to Python for pip installation
                bat '"C:\\Users\\monis zahid\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install --upgrade pip'
                bat '"C:\\Users\\monis zahid\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install flask'
            }
        }

        stage('Run Application') {
            steps {
                // Start the Flask app using the full Python path
                bat 'start "FlaskApp" "C:\\Users\\monis zahid\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" views.py'
            }
        }
    }
}
