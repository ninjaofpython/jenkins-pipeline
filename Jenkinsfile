pipeline {
    agent any 
    environment {
        NEW_VERSION = '2.0.0'
    }
        stages {
            stage("build") {
              steps {
                  echo 'Building the application'
                  echo "Building version ${NEW_VERSION}"
              }
            }
        stage("test"){
            when {
                expression {
                  BRANCH_NAME == 'None'|| BRANCH_NAME == 'master'
                }
            }
            steps {
                echo 'Testing the application'
            }
        }
        stage("Deploying Schmoney"){
          steps {
              echo 'Deploying the Schmoney'
          }
      }
   }
}
