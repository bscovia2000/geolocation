pipeline {

     agent any
     tools {
  maven 'M2_HOMW'
}
    triggers {
  pollSCM '* * * * *'

}
    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh mvn 'mvn package'
           }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                step'Deploy Step'
                
            }
        }
    
    
