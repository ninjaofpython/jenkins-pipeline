pipeline {
  agent any 
  environment {
    NEW_VERSION = '2.0.0'
    SERVER_CREDENTIALS = credentials('server-credentials')
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
            withCredentials([
              usernamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PWD)
            ])
            script {
                def test = 2 + 2 > 3 ? "Too much sauce from the repo not the replay" : "No sauce at all I must be white."
                  echo test
             }
         }
      }
   }
}
