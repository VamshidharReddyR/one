pipeline {
    agent any
    stages {
        stage ("code") {
            steps {
                echo "code is checkedout"
            }
        }
        stage ("build") {
            steps {
                sh "mvn clean package"
            }
        }
    }
    post {
        always {
            echo "pipeline is completed"
        }
        success {
            echo "pipeline is succedded"
        }
        failure {
            echo "pipeline is failed"
        }
    }
}
