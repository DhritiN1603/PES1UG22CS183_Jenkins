pipeline {
    agent any 
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', 
                branches: [[name: '*/main']], 
                userRemoteConfigs: [[url: 'https://github.com/DhritiN1603/PES1UG22CS183_Jenkins.git']]])
            }
        }

        stage('Build') {
            steps {
                build 'PES1UG22CS183-1'
                sh 'g++ main/new_added.cpp -o output' 
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG22CS183-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploying the application' 
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
