pipeline{
    agent any

    stages{

    
        stage("docker build"){
            steps{
                sh "docker-compose up --build"
            }
        }

    stage("commiting the docker images"){
            steps{
                sh "docker commit kanban-ui divyadockerhub1998/kanban-ui"
                sh "docker commit kanban-app divyadockerhub1998/kanban-appp" 
            }
        }

        stage("pushing the images to docker hub"){
            steps{
                withDockerRegistry([ credentialsId: "f584bcd1-20ad-4372-a6d8-aaecfaf8096e", url: "" ]){
                    sh "docker push divyadockerhub1998/kanban-ui"
                    sh "docker push divyadockerhub1998/kanban-ui"
                }
            }
        }       

      

        
    }
}
