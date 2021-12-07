@Library('pipeline-library-demo')_
pipeline {
    agent  any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5', daysToKeepStr: '14'))
        timestamps()
    }
    environment { 
        ENV_NAME                 = "dev" 
        SQUAD_NAME               = "devops"
    }
    stages{
        stage ("start"){
            steps {
                script{
                    standardPipeline
                }
            
            }
        }
        
    }
    
}
