pipeline {
    agent any
    
    stages {
        stage("clone git"){
            steps{
                git branch:'master' , url:'https://github.com/bensonbaragu/gallery.git'
            }
        }
        stage("Install dependencies"){
            steps{
                sh 'npm install'
            }
        }
        stage("npm test"){
            steps{
                sh 'npm test'
            }
        }
    }
}