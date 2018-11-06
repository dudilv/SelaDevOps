pipeline {
  agent any
  stages {
    stage('Build Demo App') {
      when {
        expression {
          params.REQUESTED_ACTION == 'Build'
        }
      }
      steps {
        sh '''npn install npn
        npn run build'''
      }
    }
    stage('Test') {
      steps {
        sh '''npn install npn
        npn run build'''
      }
    }
  }
  parameters {
    choice(name: 'REQUESTED_ACTION', choices: '''Build
    Stage
    ''', description: 'Type of action to perform')
  }
}
