// Using git without checkout
pipeline {
  agent any
  parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'BRANCH', type: 'PT_BRANCH'
  }
  stages {
    stage('Init') {
      steps {
        git branch: "${params.BRANCH}", url: 'https://github.com/bluespringshade/automation-runner.git'
      }
    }
  }
}