pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/prince2489/node-todo-app.git'
            }
        }
    }
}
