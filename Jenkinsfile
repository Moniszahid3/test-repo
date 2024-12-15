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
                // Use cmd.exe explicitly to run commands
                bat 'cmd.exe /c "C:\\Python313\\python.exe -m pip install --upgrade pip"'
                bat 'cmd.exe /c "C:\\Python313\\python.exe -m pip install flask"'
            }
        }

        stage('Run Application') {
            steps {
                // Start the Flask app using the full Python path
                bat 'cmd.exe /c "start C:\\Python313\\python.exe views.py"'
            }
        }
    }
}
