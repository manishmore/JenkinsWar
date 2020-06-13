pipeline {
    agent any
    def ParamsFile = load “ParamsFile.groovy”
    stages {
        stage("Run unit tests"){
          steps {
            script {
              try {
              echo "Hello, CONDITIONAL----"
              test
              }catch(Exception ex) {
                println("Catching the exception");
                currentBuild.result = 'UNSTABLE'
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
              showMavenVersion("--maven")
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
        stage('end of the file') {
            steps {
               ParamsFile.mycommoncode()
            }
        }
    }
}

def showMavenVersion(String a) {
    echo a
}
