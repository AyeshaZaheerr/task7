pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                // Check out your code from your GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/Bambokyo/groovy.git']]])
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Call the deployToEnvironment function with the input string
                    A = load 'ayesha.groovy'
                    A.FunctionProd('TEsT')
                }
            }
        }
    }
}
