def gv
pipeline {
    agent any

    environment {
        VERSION = 'v1.0.0'
    }

    stages {
        stage("init") {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }
        stage("build") {
            steps {
                gv.build()
            }
        }

         stage("test") {
            // when {
            //     expression {
            //         BRANCH_NAME == 'dev'
            //     }
            // }
            steps {
               gv.test()
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
