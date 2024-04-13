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
        
    }
}