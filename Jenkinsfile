pipeline {
   agent { docker { image 'maven:3.6.3' } } 
     stages {
      stage ('build'){
        steps {
         sh 'mvn --version'
         echo "maven version"
         }
        }

      stage('Dev') {
        steps {
         echo "Build"
         echo "Run"
	}
       }
      } 
     post {
         always {
          echo "I will run always"
          }
         success {
          echo "I run on success"
          }
         failure { 
          echo "I run on fail"
          }
         }  
      
     }

