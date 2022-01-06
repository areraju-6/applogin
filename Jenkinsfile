properties([pipelineTriggers([githubPush()])])

pipeline {
    agent {label "slave1"}
    stages {
        stage ("clone") {
            steps {
                git url: 'https://github.com/tejesh555/applogin.git'
            }
        }
        stage ("build") {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
