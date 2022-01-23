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
            }
 
        }

        stage("Copy File From Jenkins Server To K-Master"){
            steps{
                //echo "Your Test Credential are ${SERVER_CREDENTIALS} ${SERVER_CREDENTIALS_PSW}"
                //withCredentials([usernamePassword(credentialsId: 'k-master', passwordVariable: 'pass', usernameVariable: 'user')]) {
                        //sh "sshpass -p '${pass}' ssh '${user}'@10.0.0.10"
                        //sh 'hostname'
                    //}
                echo "testings"

                }
            }
 
    

        stage('Testing Connection To K-Master'){
            steps{
                script{
                    withCredentials([kubeconfigFile(credentialsId: 'k-master-config', variable: 'KUBECONFIG')]) {
                            sh 'kubectl get nodes'
                            sh 'helm list'
                            sh 'hostname'
                            sh 'pwd'
                            sh 'kubectl -f .\web.yaml'
                    }

                }
            }
        }
    }
}