pipeline {
    agent any

    tools {
        gradle "GRD"
    }

    stages {

        stage ('Build app.') {
            steps {
                sh 'gradle clean build -x test'
            }
        }

        stage ('Run tests.') {
            steps {
                sh 'gradle test'
            }
        }

        stage ('Deploy.') {
            steps {
                sh 'gradle deployHeroku'
            }
        }
    }
}
