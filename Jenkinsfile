CODE_CHANGES = getGitChanges()
pipeline {
    agent any
    stages {
        stage(build) {
             when {
                expression {
                    BRANCH_NAME == 'main' && CODE_CHANGES == true
                }
            }
            steps {
                echo "building stage"
            }
        }
        stage(testing) {
            when {
                expression {
                    BRANCH_NAME == 'dev' || BRANCH_NAME == 'main'
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
}