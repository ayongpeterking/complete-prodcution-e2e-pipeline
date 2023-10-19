pipeline{
    agent{
        label "docker-node"
    }
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
    
    stages{
        stage("Cleanup Workspace"){
            steps {
                cleanWs()
            }

        }
    

        stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

        }
    }
}        