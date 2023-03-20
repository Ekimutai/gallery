pipeline {
    agent any
    
    tools{
     nodejs "node"
    }

    stages {
        stage('clone') {
            steps {
                 git 'https://github.com/Ekimutai/gallery'
            }
        }
        stage('Build'){
            steps{
                echo 'Build successful'
            }
        }
        stage('Tests'){
            steps {
                sh 'npm test'}
        }
        stage('Deploy to render'){
            steps{
                httpRequest httpMode: 'POST', responseHandle: 'NONE', url: 'https://api.render.com/deploy/srv-cfpodbarrk0fd9vgapqg?key=mK7t1pfKCkQ', wrapAsMultipart: false
                echo 'Deploying to render was successful'
                 slackSend channel: 'ip-channel'
            }
        }

       
        stage('Dependencies') {
            steps {
                sh "npm install"


            }
        }
    }
}