pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS183-1 main/new_added.cpp' 
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS183-1'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deploying the application..."
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed' 
        }
    }
}
