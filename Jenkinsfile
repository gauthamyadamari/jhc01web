pipeline {
    agent any
    stages {
        stage ("maven build") {
            steps{
                sh 'mvn clean package'
            }
        }
         stage ("deploy to dev") {
             when {
                 branch "develop"
             }
            steps{
                echo "deploy to development server"
            }
        }
         stage ("deploy to stage") {
             when {
                 branch "stage"
             }
            steps{
                echo "deploy to staging server"
            }
        }
        stage ("deploy to prod") {
             when {
                 branch "main"
             }
            steps{
                echo "deploy to production server"
            }
        }
    }
}
