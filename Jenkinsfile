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
    
        stage('Checkout') {
            steps {
                // This step pulls the code from the configured Git repository in Jenkins job configuration.
                checkout scm
            }
        }

        stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

        }

        stage("Test Application"){
            steps {
                sh "mvn test"
            }
    }
}        