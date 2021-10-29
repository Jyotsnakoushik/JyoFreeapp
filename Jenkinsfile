pipeline{
    agent any
    stages{
        stage("Maven Build"){
            when {
                branch = "develop"
            }
            steps{
                sh "mvn clean package"
            }
        }
        stage("Sonar Analysis"){
            when {
                branch = "develop"
            }
            steps{
                echo "perform sonar analysis"
            }
        }
        stage("Dev Deploy"){
            when {
                branch = "develop"
            }
            steps{
                echo "Deploy to development"
            }
        }
        stage("Deploy to QA "){
            when {
                branch = "qa"
            }
            steps{
                echo "deploy to qa"
            }
        }
        stage("Deploy to production "){
            when {
                branch = "main"
            }
            steps{
                echo "deploy to prod"
            }
        }
    }
}
