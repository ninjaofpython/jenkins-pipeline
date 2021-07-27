pipeline {
    agent any 

        stages {
            stage("build") {
              steps {
                  echo 'Building the application'
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
