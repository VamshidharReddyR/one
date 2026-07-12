pipeline {
    agent any 
    stages {
        stage ("code") {
            steps {
                git "https://github.com/VamshidharReddyR/one.git"
            }
        }
        stage ("build") {
            steps {
                sh "mvn clean package"
            }
        }
        stage ("image") {
            steps {
                sh "docker build -t tomcat ."
            }
        }
    }
    post {
        success {
            echo "the pipeline is succeded"
        }
        failure {
            echo "the pipielin is failed"
        }
        always {
            echo "the pipelien is completed"
        }
    }
}
