pipeline {
    agent any

    environment {
        VERSION = 'v1.0.0'
    }

    stages {
        stage("build") {
            steps {
                echo "building the app.."
                echo "building version ${VERSION}"
            }
        }

         stage("test") {
          
            steps {
                echo "testing the app..."
            }
        }

        stage("deploy") {
            steps {
                echo "deploying the app...."
            }
        }

    }

    post {
        always {
            echo "ALWAYS"
        }

        success {
            echo "SUCCESS"
        }

        failure {
            echo "FAILURE"
        }
    }

}
