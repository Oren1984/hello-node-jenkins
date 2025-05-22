pipeline {
    agent any

    environment {
        IMAGE_NAME = "hello-node"
        TAG = "latest"
    }

    stages {
        stage('Checkout Code') {
            steps {
                git https://github.com/Oren1984/hello-node-jenkins.git
            }
        }

        stage('Docker Build & Tag') {
            steps {
                sh 'docker build -t $IMAGE_NAME:$TAG .'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'docker run -d --rm --name $IMAGE_NAME-container -p 3000:3000 $IMAGE_NAME:$TAG'
            }
        }
    }
}
