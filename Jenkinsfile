pipeline {
    agent any
    stages {
        stage(build) {
            steps {
                echo "building stage"
            }
        }
        stage(testing) {
            when {
                expression {
                    BRANCH_NAME == 'dev' ||BRANCH_NAME == 'master'
                }
            }
            steps {
                echo "testing stage"
            }
        }
        stage(deployment) {
            steps {
                echo "deployment stage"
            }
        }
    }
    post {
        always {
            //
        }
    }
}