pipeline {
  agent any 
  environment {
    NEW_VERSION = '1.3.0'
  }
  stages {
    stage("build") {
        steps {
            echo 'Building the application' 
            echo "Building version ${NEW_VERSION}"    
          } 
        }
    stage("test"){
        steps {
            echo 'Testing the application'
        }
      }
    stage("deploy_schmoney"){
        steps {
            echo 'Deploying schomoney'
            script {
                def test = 2 + 2 > 3 ? "Too much sauce from the repo not the replay" : "No sauce at all I must be white."
                  echo test
             }
         }
      }
   }
}
