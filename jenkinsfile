pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/PaelPavlov/SEDO_Regular-Exam-3.git'
            }
        }

        stage('Restore Dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Build') {
            steps {
                bat 'dotnet build --configuration Release'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'dotnet test --configuration Release --no-build --verbosity normal'
            }
        }
    }

}
