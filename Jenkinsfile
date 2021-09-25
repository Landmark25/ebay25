// Types of Jenkinsfile
// to get the list of jenkins environmental variables <publicIp_address>:8080/env-vars.html/
// setting up a conditon 
// CODE_CHANGES = getGitChanges()
pipeline{
    agent any
    //defining environmental variables 
    environment{
        NEW_VERSION = '1.3.0'
    } 
    stages {
        stage('1-GitClone') {
            steps{
                echo "Cloning the Application"
            }
        }
        stage('2-MavenBuild'){
            steps{
                echo "Building the Application"
                echo "Building version ${NEW_VERSION}"
            }
        }
        stage('3-CodeQuality'){
            steps{
                echo "testing the Application"
            }
        }
        stage('4-UploadArtifacts'){
            when {
                expression{
                  //  BRANCH_NAME == 'dev' || BRANCH_NAME == 'master'
                 //   BRANCH_NAME  == 'dev'  && CODE_CHANGES == true
                }
            }
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
    post{
        // Conditions
        always{

        }
        success{

        }
        failure{

        }

    }
}

