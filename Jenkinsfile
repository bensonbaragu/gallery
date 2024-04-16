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
                sh 'npm test ./test'
            }            
        }        
    }
    post {                
                success {
                    mail to: 'bensonbaragu@gmail.com',
                         subject: 'Test Success - Jenkins Pipeline',
                         body: "The tests in the Jenkins pipeline have passed successfully."
                }
                
            }
}