pipeline {
    agent any
    
    stages {
        stage("clone git"){
            steps{
                git branch:'master' , url:'https://github.com/bensonbaragu/gallery.gi'
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
            post {
                always {
                    junit '**/junit.xml'
                }
                success {
                    mail to: 'bensonbaragu@gmail.com',
                         subject: 'Test Success - Jenkins Pipeline',
                         body: "The tests in the Jenkins pipeline have passed successfully."
                }
                
            }
        }
    }
}