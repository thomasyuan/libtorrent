pipeline {
    agent any

    stages {
        stage('cppCheck') {
            steps {
                sh 'cppcheck --enable=all --xml --xml-version=2 . 2> cppcheck-result.xml && cat cppcheck-result.xml'
                publishCppcheck allowNoReport: true, ignoreBlankFiles: true, pattern: '**/cppcheck-result.xml'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
