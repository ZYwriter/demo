pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Test') {
      steps {
        echo 'Hello'
        catchError()
        jiraComment(issueKey: 'issueKey', body: 'body')
      }
    }
  }
}