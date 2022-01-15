pipeline{
    agent any
    environment{
        //SERVER_CREDENTIALS = credentials('test')
        }
    stages{
        stage("Pull Code From GitHub"){
            steps{
                echo "Pull Code From GitHub"
                //echo "Your Test Credential are ${SERVER_CREDENTIALS} ${SERVER_CREDENTIALS_PSW}"
                withCredentials([
                    usernamePassword(credentials: 'test', usernameVariable: USER, passwordVariable: PWD)
                ])
                {
                    echo "printing my credentials ${USER} ${PWD}"
                }
            }
 
        }
    }
} 