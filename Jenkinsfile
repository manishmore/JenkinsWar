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
                j//unit 'nosetests.xml'
              }
            }
          }
        }
        stage ('Speak') {
            steps{
              echo "Hello, CONDITIONAL"
            }
          }
        }
}
