pipeline {
    agent any
    
    stages {
        stage('Build image') {
            bat 'docker build -t Priyanka-001/docker-project:getting-started .'
        }
    
         stage('Push image') {
             steps {
                withDockerRegistry([ credentialsId: "priyab173", url: "" ]) {
                bat 'docker push Priyanka-001/docker-project:getting-started'
         
                }
        
             } 
         }
        // stage('Build Docker Image') {
        //     steps {
        //       bat 'docker build -t Priyanka-001/docker-project:getting-started .'
        //     }
        // }
        // stage('Login') {
        //     steps {
        //         bat 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
        //     }
        // }
        // stage('Push Docker Image') {
        //     steps {
        //      bat 'docker push Priyanka-001/docker-project:getting-started'
        //     }
        // }
        stage('Deploy') {
            steps {
                echo "deploying..."
            }
        }
    }
}
