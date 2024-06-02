pipeline{
    agent any
    environment{
        DIRECTORY_PATH= "/Users/mari/Library/Mobile Documents/com~apple~CloudDocs/UNI/SIT223 Prof practice in IT/tasks/6.1C/github files"
        TESTING_ENVIRONMENT= "Testing"
        PRODUCTION_ENVIRONMENT= "Mari"
    }
    stages{
        stage('Build'){
            steps{
                echo "fetch the source code from the directory path specified by the environment variable"
                echo "compile the code and generate any necessary artifacts"
            }
        }
        stage('Test'){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }
        stage('Code Quality Check'){
            steps{
                echo "check the quality of the code"
            }
        }
        stage('Deploy'){
            steps{
                echo "deploy the application to a testing environment specified by the environment variable"
            }
        }
    }
}