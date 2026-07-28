pipeline {
    agent any

    stages {
        stage('Cloning java project repo') {
            steps {
               git 'https://github.com/Sharath-yp25/java.git'
            }
        }
        
         stage('Compiling and testing java project') {
            steps {
                 bat '''javac Test.java
                         java Test'''
            }
        }
    }
    
    post {
        success {
            mail bcc: '', 
            body: 'This mail is to inform that build is successful',
            cc: '', 
            from: '', 
            replyTo: '', 
            subject: 'Build success',
            to: 'chandanponnappac@gmail.com'
        }
        
        failure {
             mail bcc: '', 
            body: 'This mail is to inform that build is not successful',
            cc: '', 
            from: '', 
            replyTo: '', 
            subject: 'Build failure',
            to: 'iamchandanponnappa2315@gmail.com'
        }
    }
}
