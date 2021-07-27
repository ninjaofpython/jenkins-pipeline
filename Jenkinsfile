pipeline {
    agent any 
    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
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
                  BRANCH_NAME == 'main'|| BRANCH_NAME == 'master'

                }
            }
            steps {
                echo 'Testing the application'
            }
        }
        stage("Deploying Schmoney"){
          when {
              expression {
                  params.executeTests
              }
          }
          steps {
              echo 'Deploying the Schmoney'
              echo "deploying ${params.VERSION}"
          }
      }
   }
}
