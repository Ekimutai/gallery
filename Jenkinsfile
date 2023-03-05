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
       
        stage('Dependencies') {
            steps {
                sh "npm install"


            }
        }
    }
}