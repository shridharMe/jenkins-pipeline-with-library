@Library('pipeline-library-demo')_
pipeline {
    agent  any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5', daysToKeepStr: '14'))
        timestamps()
    }
    parameters { 
        choice(choices: 'dev', description: 'Select the env to deploy', name: 'ENV_NAME')
        choice(choices: 'devops', description: 'Select the team to deploy', name: 'SQUAD_NAME')
    }
    stages{
        stage ("start"){
            steps {
                script{
                    standardPipeline()
                }
            
            }
        }
        
    }
    
}
