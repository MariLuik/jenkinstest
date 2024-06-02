pipeline{
    agent any
    environment{
        DIRECTORY_PATH= "/Users/mari/Library/Mobile Documents/com~apple~CloudDocs/UNI/SIT223 Prof practice in IT/tasks/6.1C/github files"
        TESTING_ENVIRONMENT= "Testing"
        PRODUCTION_ENVIRONMENT= "Mari"
    }
    stages{
        stage("Build"){
            steps{
                echo "Building the code using Maven"
            }
              post{
                success{
                    mail to: "mariluik@gmail.com",
                    subject: "Unit and integration test status Email",
                    body: "Unit and integration testing has been successfully completed!"
                }
     
            }
        }
    }
}
