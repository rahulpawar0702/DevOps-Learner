pipeline { 
  
   agent {label "jenkins-slavenode-01"} 

   stages {
   
     stage('Install Dependencies') { 
        steps { 
           sh 'echo "installing application..."' 
        }
     }
     
     stage('Test') { 
        steps { 
           sh 'echo "testing application..."'
        }
      }

         stage("Deploy application") { 
         steps { 
           sh 'echo "deploying application..."'
         }

     }
  
   	}

   }
