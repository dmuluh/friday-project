pipeline {
    agent any
    environment {
        NEW_VERSIONS = '1.2'
    }
    stages {
        stage(build) {
            steps {
                echo "building stage"
                echo "new version is ${NEW_VERSIONS}"
            }
        }
        stage(testing) {
            steps {
                echo "testing stage"
            }
        }
    }
}