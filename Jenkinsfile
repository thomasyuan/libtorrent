pipeline {
  agent any
  stages {
    stage('cppCheck') {
      steps {
        sh 'cppcheck --enable=all --xml --xml-version=2 . 2> cppcheck-result.xml'
        publishCppcheck(ignoreBlankFiles: true, pattern: '**/cppcheck-result.xml', displayAllErrors: true, displayErrorSeverity: true, displayPerformanceSeverity: true, displayWarningSeverity: true, displayStyleSeverity: true, displayPortabilitySeverity: true, displayNoCategorySeverity: true, failureThreshold: '10', newFailureThreshold: '1', newThreshold: '10', numBuildsInGraph: 10, severityError: true, severityInformation: true, severityNoCategory: true, severityPerformance: true, severityPortability: true, severityStyle: true, severityWarning: true)
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}