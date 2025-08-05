pipeline{

agent none
tools{
    maven 'mymaven'
}
    stages{
        stage('Checkout code')
        {
            agent any
            steps{
                git 'https://github.com/Anmolrock/Medicure-Healthcare-Devops.git'
            }
        }
        
        stage('Package code')
        {
            agent any
            steps{
                sh 'mvn package'
            }
        }
        
        stage('Build Image')
        {
            agent any
            steps{
                sh 'docker build -t myimage:project2 .'
            }
        }
    
    stage('push the image to dockerHub')
    {
        agent any
        steps{
            withCredentials([string(credentialsId: 'DOCKER_HUB_PASWD', variable: 'DOCKER_HUB_PASWD')]) {
            sh 'docker login -u anmol792 -p ${DOCKER_HUB_PASWD}'
}
            sh 'docker tag myimage:project2 anmol792/myimage:project2'
                sh 'docker push anmol792/myimage:project2'

        }
    }
    
    
     stage('Deploy on Test server')
        {
            agent {
                label 'test_server'
                
            }
            steps{
                sh 'docker run -d -P anmol792/myimage:project2 '
            }
        }

    }
    
}
