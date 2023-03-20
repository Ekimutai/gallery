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
       
        stage('Dependencies') {
            steps {
                sh "npm install"


            }
        }
    }
}