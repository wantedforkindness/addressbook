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
    //    stage ('deploy to tomcat') {
    //       steps {
   //             sh 'cp ./target/addressbook-2.0.war /var/lib/tomcat9/webapps/addressbook.war' 
  //        }    
 //      }        
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
