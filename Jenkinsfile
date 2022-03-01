pipeline{
    agent any
    tools {
        maven 'maven3'
    }
    stages {
        stage("Maven Build"){
            when {
                branch 'develop'
            }
            steps{
                sh "mvn clean package" 
            }
        }

        stage("Sonar Analysis"){
            when {
                branch 'develop'
            }
            steps{
                echo "sonar analysis"
            }
        }
        stage("Upload to Nexus"){
            when {
                branch 'develop'
            }
            steps{
                echo "upload war file to nexus"
            }
        }

        stage("Deploy to dev and test"){
            when {
                branch 'develop'
            }
            steps{
                echo "deploying to development..."
                echo "deploying to test..."
            }
        }
        stage("Deploy to UAT"){
            when {
                branch 'uat'
            }
            steps{
                echo "deploying to uat..."
            }
        }
        stage("Deploy to Prod"){
            when {
                branch 'master'
            }
            steps{
                echo "deploying to production..."
            }
        }
    }
}