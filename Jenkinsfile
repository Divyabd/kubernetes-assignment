pipeline{
    agent any

    stages{

    
    //    stage("docker build"){
   //         steps{
   //             sh "docker-compose up "
  //          }
  //      }

    stage("commiting the docker images"){
            steps{
                sh "docker commit kanban-ui divyadockerhub1998/kanban-ui"
                sh "docker commit kanban-app divyadockerhub1998/kanban-appp" 
            }
        }

        stage("pushing the images to docker hub"){
            steps{
                withDockerRegistry([ credentialsId: "dockerhub", url: "" ]){
                    sh "docker push divyadockerhub1998/kanban-app"
                    sh "docker push divyadockerhub1998/kanban-ui"
                }
            }
        }       

      

        
    }
}
