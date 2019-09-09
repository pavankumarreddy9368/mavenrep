pipeline {
    agent any

    stages {
        stage('codecheckout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/pavankumarreddy9368/mavenrep.git']]])
            }
        }
        stage('build') {
            steps {
               bat 'mvn package'
            }
        }
        stage('INFRA') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
