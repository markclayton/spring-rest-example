pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'mvn package'
      }
    }
    stage('Post-Build') {
      steps {
        echo 'Post Build Section'
        veracode(applicationName: 'Example Spring Application', criticality: 'Low', sandboxName: 'Example Spring Application Sandbox', scanName: 'Example Spring Application Scan 01', createSandbox: true)
      }
    }
  }
}