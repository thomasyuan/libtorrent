pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                cppcheck --xml --xml-version=2 SOURCE_DIRECTORY 2> report_cppcheck.xml
            }
        }
        stage('cppCheck') {
            steps {
                publishCppcheck pattern:'output/report_cppcheck.xml'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
