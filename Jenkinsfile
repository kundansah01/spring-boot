pipeline{
    agent any
    environment{
        NEW_Version = '1.0.1'
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

                stage("Copy File From Jenkins Server To K-Master"){
            steps{
                echo "Copy File From Jenkins Server To K-Master"
                //echo "Your Test Credential are ${SERVER_CREDENTIALS} ${SERVER_CREDENTIALS_PSW}"
                withCredentials([usernamePassword(credentialsId: 'k-master', passwordVariable: 'pass', usernameVariable: 'user')]) {
                        sh 'sshpass -p ${pass} ssh ${user}@10.0.0.10'
                        sh 'hostname'
                }
                {
                    echo "printing my credentials ${user} ${pass}"
                }
            }
 
        }
    }
} 