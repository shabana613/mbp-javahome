pipeline{
    agent any
    tools {
        maven 'maven3'
    }
    stages{
        stage('MAVEN BUILD){
              when{
              branch "develop"
              }
              steps{
                sh "maven clean package"
              }
        }    
    }
}
