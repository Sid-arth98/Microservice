pipeline { 
    agent any
    parameters {
        string(name: 'ServiceName', defaultValue: 'productcatalogservice')
    }
    stages {
        stage('Git checkout') {
            steps {
                script {
                    // Checkout the current branch
                    checkout scm

                    // Call the custom function to build Docker image
                    dockerimagebuild(ServiceName)
                }
            }
        }
    }
}
