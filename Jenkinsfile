pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/prince2489/node-todo-app.git'
            }
        }
        stage('Image Build') {
            steps {
                sh 'docker build . -t prince2489/mynodeapp:v1'
            }
        }
        stage('Image Push') {
            steps {
                sh 'docker push . -t prince2489/mynodeapp:v1'
            }
        }
    }
}
