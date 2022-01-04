pipeline {
    agent any
    stages {
        stage ('compilation') {
          steps {
              sh 'mvn -B compile'
          }  
        }
        stage ('static code analysis') {
            steps {
                sh 'echo hello there. this is static code analysis stub'
    //            sh '/home/ubuntu/sonar-scanner-4.6.2.2472-linux/bin/sonar-scanner'
            }
        }
        stage ('package') {
            steps {
               sh 'mvn -B package'
            }
        }
        stage ('build and publish to dockerhub') {
           steps {
                sh 'sudo docker build -t berylobi/ab:latest .'
               sh 'sudo docker push berylobi/ab:latest'
          }    
       }        
    }
post {
  always {
      sh 'echo the build as completed'
  }
  success {
    sh 'echo the buid is successfull'
  }
  failure {
    sh 'echo the buid failed'
     }
   }
} 
