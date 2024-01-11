pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/yourusername/yourrepository.git']]])
            }
        }
        stage('Build') {
            steps {
                // Your build commands go here
            }
        }
        // Add more stages as needed
    }
}

