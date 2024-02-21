pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/prince2489/node-todo-app.git'
            }
        }
        stage('Dir') {
            steps {
                sh '''
                ls
                pwd
                '''
            }
        }
        stage('Image Build') {
            steps {
                script {
                    // steps{
                    //     docker.withRegistry('', '') {
                    customImage = docker.build("prince2489/mynodeapp:v1")
                    // }
                    }
            // }
        }
        }
        stage('Image Push') {
            steps {
                script{
                    // withDockerRegistry(credentialsId: 'dockerhub-pri') {
                    customImage.push()
                }
            }
            }
        }
    }
}
