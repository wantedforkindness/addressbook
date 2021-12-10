pipeline {
    agent any 
    stages {
        stage ('compilation') {
          steps {
              sh 'echo hello there. this is compilation'
              sh 'echo hello world'
          }  
        }
        stage ('deployment') {
            steps {
                sh 'echo hello there. this is deployment'
            }
        }
        stage ('finalize') {
            steps {
                sh 'echo hello there. this is finalization'
            }
        }
        stage ('send mail') {
            steps {
                mail bcc: '', body: 'the build is finish', cc: '', from: '', replyTo: '', subject: 'this is the build email', to: 'berylebok1@gmail.com'
            }    
        }        
    }
    post {
  always {
    // One or more steps need to be included within each condition's block.
  }
  success {
    // One or more steps need to be included within each condition's block.
  }
  failure {
    // One or more steps need to be included within each condition's block.
  }
}
} 
