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

            steps {
                echo "building image.."
            }
        }

         stage("test") {
            when {
                expression {
                    BRANCH_NAME == 'dev'
                }
            }
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

        }

        success {

        }

        failure {

        }
    }

}
