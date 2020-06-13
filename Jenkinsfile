pipeline {
    agent any
    stages {
        stage("Run unit tests"){
          steps {
            script {
              try {
              echo "Hello, CONDITIONAL----"
              } finally {
                echo "finally..."
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
