pipeline {
  agent any
  stages {
    stage('Build on k8') {
      steps {
        sh 'pwd'
        sh 'ls'
        sh 'cp -R helm/* .'
        sh 'ls -ltr'
        sh 'pwd'
        sh '/usr/local/bin/helm upgrade --install wfademo-app wfa-demo --set image.repository=wfademoacr.azurecr.io/wfademowithdb --set image.tag=latest'
      }
    }
  }
}
