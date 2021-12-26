pipeline{
    agent any
    SERVER_CREDENTIALS = credential('test-credential')
    stages{
        stage("Pull Code From GitHub"){
            steps{
                echo "Pull Code From GitHub"
                echo "Your Test Credential are ${SERVER_CREDENTIALS}"
            }

        }
    }
}