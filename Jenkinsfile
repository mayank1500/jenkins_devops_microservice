pipeline {
   agent any
   environment {
     dockerHome = tool 'Mydocker'
     mavenHome = tool 'Mymaven'
     PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
}
   stages {
      stage ('build'){
        steps {
         sh 'mvn --version'
         echo "maven version"
         }
        }

      stage('print PATH') {
        steps {
         echo "PATH contains : ${env.PATH}"
         echo "docker : ${env.dockerHome}" 
         echo "maven ${env.mavenHome}"
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

