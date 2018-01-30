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
        hubotApprove(failOnError: true, message: 'ok to test', room: 'automatically', url: 'https://github.com/ZYwriter/demo.git')
        catchError()
        jiraComment(issueKey: 'issueKey', body: 'body')
      }
    }
  }
}