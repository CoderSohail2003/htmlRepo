pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // This pulls your entire repo, including your index.html
                git branch: 'main', url: 'https://github.com/CoderSohail2003/javaJenkins2.git'
            }
        }
        
        stage('Validate File') {
            steps {
                // Just to confirm the file is there on Windows
                bat 'dir'
            }
        }

        stage('Publish GitHub HTML') {
            steps {
                // Points to the file that was just pulled in the Checkout stage
                publishHTML([
                    allowMissing: false,
                    alwaysLinkToLastBuild: false,
                    keepAll: true,
                    reportDir: '.',            // Look in the root workspace
                    reportFiles: 'index.html', // The name of your file in GitHub
                    reportName: 'GitHub Live Report',
                    reportTitles: 'My Repo Content'
                ])
            }
        }
    }
}
