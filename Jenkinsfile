pipeline {
    agent any
    stages {
        stage("Run unit tests"){
          steps {
            script {
              try {
              echo "Hello, CONDITIONAL----"
              test
              }catch(Exception ex) {
                println("Catching the exception");
                currentBuild.result = 'FAILURE'
              } finally {
                echo "finally..."
                echo currentBuild.result
              }
            }
          }
        }
        stage ('Speak') {
            steps{
              echo "Hello, CONDITIONAL"
            }
          }
        stage('build') {
                steps {
                    echo "Size ${params.size}"
                }
        }
        stage('deploy') {
                steps {
                    echo "Color ${params.color}"
                }
        }
    }
}
