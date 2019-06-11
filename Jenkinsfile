pipeline {
    agent any

    stages {
        stage('cppCheck') {
            steps {
                sh label: '', returnStatus: true, script: 'cppcheck -j 4 --enable=all --xml --xml-version=2 . 2> cppcheck.xml
 cppcheck-result.xml'
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
