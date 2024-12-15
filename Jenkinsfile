pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Moniszahid3/test-repo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat "C:\\Python313\\python.exe -m pip install --upgrade pip"
                bat "C:\\Python313\\python.exe -m pip install flask"
            }
        }

        stage('Run Application') {
            steps {
                bat "start C:\\Python313\\python.exe views.py"
            }
        }
    }
}
