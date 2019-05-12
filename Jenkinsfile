pipeline {
    agent any 
    stages {
        stage('source') { 
            steps {
                git credentialsId: 'c76fffcf-cab5-4537-9c61-2cda28bb596d', url: 'https://github.com/wakaleo/game-of-life.git'            }
        }
        stage('build') { 
            steps {
                sh label: '', script: 'mvn package'            }
        }
        stage('aritifacts') { 
            steps {
                archiveArtifacts '**/target/*.jar' 
            }
        }
    }
}
