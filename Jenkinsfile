pipeline {
    agent any

    stages {
        stage('cppCheck') {
            steps {
                sh "cppcheck --enable=all --xml --xml-version=2 ."
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
