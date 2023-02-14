pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ ./main/single.cpp -o PES1UG20CS490'
                build job: 'PES1UG20CS490-1'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS490'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deployment stage"'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
