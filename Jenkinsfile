pipeline {
    triggers {
  pollSCM '* * * * *'
}
agent any
stages {
    stage ('maven package') {
        steps {
            sh 'mvn clean'
            sh 'mnv install'
            sh 'mvn package'

            }
      }
      stage("test") {
          steps {
              sh 'mvn test'
          }
      }
      stage('Deploy') {
            steps {
                echo 'Deploy Step'
                sleep 10
            }
        }
        stage('Docker') {
            steps {
                echo 'Image step'
            }
        }
    }
}

    

    
        

