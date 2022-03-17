pipeline{
    agent any
    tools{
        maven 'maven3'
    }
    stages{
        stage("maven build") {
            when{
                branch 'develop'
            }
            steps{
                sh "maven clean package"
            }
        }
    }
}
