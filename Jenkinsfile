pipeline {
    agent any

    stages {
        stage('codecheckout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/pavankumarreddy9368/mavenrep.git']]])
            }
        }
        stage('CLOUD') {
            steps {
                echo 'Testing..'
            }
        }
        stage('INFRA') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
