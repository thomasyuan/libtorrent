pipeline {
    agent any

    stages {
        stage('cppCheck') {
            steps {
                sh "cppcheck --enable=all ."
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
