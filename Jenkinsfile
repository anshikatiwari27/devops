pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out the code from your GitHub repository
                checkout([$class: 'GitSCM', 
                    branches: [[name: 'main']], 
                    doGenerateSubmoduleConfigurations: false, 
                    extensions: [], 
                    submoduleCfg: [], 
                    userRemoteConfigs: [[url: 'https://github.com/anshikatiwari27/devops.git']]
                ])
            }
        }

        stage('Deploy to Apache') {
            steps {
                // Copy the code to the Apache document root directory
                bat script: '''
                    xcopy /s /e /y "C:\\Users\\Anshika Tiwari\\Desktop\\Devops" "C:\\Apache24\\htdocs"
                '''
            }
        }
    }
}
