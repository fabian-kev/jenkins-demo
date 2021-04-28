def gv
properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/fabian-kev/jenkins-demo.git/'], pipelineTriggers([githubPush()])])
pipeline {
    agent any

    environment {
        VERSION = 'v1.2.0'
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
               script {
                    gv.build()
               }
            }
        }

         stage("test") {
            // when {
            //     expression {
            //         BRANCH_NAME == 'dev'
            //     }
            // }
            steps {
                script {
                    gv.test()
                }
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
            echo "always"
        }

        success {
             echo "success"
        }

        failure {
             echo "Failure"
        }
    }

}
