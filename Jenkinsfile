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
    }
}

  node {
  def ParamsFile
  ParamsFile = load "${WORKSPACE}"+“/ParamsFile.groovy”
      stage('end of the file') {
            echo "===== ${WORKSPACE}"
            sh 'pwd'
            sh 'ls -al'
            sh 'env'
            ParamsFile.mycommoncode()
      }
  }


def showMavenVersion(String a) {
    echo a
}
