// Types of Jenkinsfile

pipeline{
    agent any
    stages {
        stage('1-GitClone') {
            steps{
                echo "Cloning the Application"
            }
        }
        stage('2-MavenBuild'){
            steps{
                echo "Building the Application"
            }
        }
        stage('3-CodeQuality'){
            steps{
                echo "testing the Application"
            }
        }
        stage('4-UploadArtifacts'){
            steps{
                echo "uploading the Application"
            }
        }
        stage('5-DeployDocker'){
            steps{
                echo "deploying the Application"
            }
        }
    }
}
