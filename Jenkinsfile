
pipeline {
  agent any
  tools {
     maven 'Maven'
     jdk 'jdk'
  }
  stages {

    stage('Build') {
        steps {
          sh 'mvn clean test'
        }
      }

    stage('Publish report') {
    steps {
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: true, keepAll: true, reportDir: 'cucumber-report', reportFiles: 'example.html', reportName: 'report', reportTitles: 'report'])
         }
    }

  }
}
