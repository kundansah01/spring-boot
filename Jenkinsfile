pipeline{
    agent any
    environment{
        SERVER_CREDENTIALS = credentials('test-credential')
        }
    stages{
        stage("Pull Code From GitHub"){
            steps{
                echo "Pull Code From GitHub"
                echo "Your Test Credential are ${SERVER_CREDENTIALS} ${SERVER_CREDENTIALS_PSW}"
            }

        }
    }
}