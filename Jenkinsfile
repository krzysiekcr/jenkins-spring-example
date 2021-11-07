pipeline {
    agent any

    tools {
        gradle "GRD"
    }

    stages {

        stage ('Build app.') {
            steps {
                sh 'gradle build -x test'
            }
        }

        stage ('Run tests.') {
            steps {
                sh 'gradle test'
            }
        }

        stage ('Deploy.') {
            steps {
                sh 'gradle clean deployHeroku'
            }
        }
    }
}
