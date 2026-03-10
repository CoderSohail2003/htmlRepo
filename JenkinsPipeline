pipeline {
  agent any 
  stages {
    stage('Checkout') {
      steps { // Corrected from 'step'
        echo 'Checking out repo'
        git 'https://github.com/CoderSohail2003/htmlRepo.git'
      }
    }
    stage('Publish') {
      steps { // Corrected from 'step'
        echo 'Publishing HTML'
        publishHTML([
          allowMissing: true, // Corrected casing: allowMissing
          alwaysLinkToLastBuild: false,
          keepAll: false,
          reportDir: '.',
          reportFiles: 'hello.html',
          reportName: 'MY HTML PIPE PAGE'
        ])
      }
    }
  }
}
