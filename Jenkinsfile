
pipeline {
  agent any
  tools {
     maven 'Maven 3.3.9'
     jdk 'jdk8'
  }
  stages {

    stage('Build') {
        steps {
          sh 'mvn clean test'
        }
      }

    stage('Publish report') {
         publishHTML([allowMissing: false, alwaysLinkToLastBuild: true, keepAll: true, reportDir: 'cucumber-report', reportFiles: 'example.html', reportName: 'report', reportTitles: 'report'])
    }

  }
}
