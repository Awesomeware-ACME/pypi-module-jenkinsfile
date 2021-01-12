pipeline {
    agent {
        kubernetes {
            defaultContainer 'jnlp'
            yamlFile 'agent-pod.yaml'
        }
    }

    stages {
        stage('Build Poetry Module') {
            container('poetry') {
                sh 'poetry install && poetry build'
            }
        }
    }
}