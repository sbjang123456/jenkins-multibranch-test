pipeline {
    agent any
    tools {
        nodejs "NodeJS 20.11.0"
    }
    stages {
        stage("Install") {
            steps {
                sh "npm i -g pnpm"
                sh "pnpm i"
            }
        }
        stage("Build") {
            steps {
                sh "pnpm build"
            }
        }
        stage("Start") {
            steps {
                sh "pnpm start"
            }
        }
    }
}
