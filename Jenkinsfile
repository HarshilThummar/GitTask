def gv

pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                echo 'Building step...'
            }
        }
        stage("test") {
            when {
                expression {
                    BRANCH_NAME == 'dev' || BRANCH_NAME == 'stage'
                }
            }
            steps {
                echo 'Testing step...'
            }
        }
        stage("deploy") {
            steps {
                echo 'Deploying step...'
            }
        }
    }
}
