pipeline {
    agent any
    tools {
        nodejs "nodejs20"
    }
    stages {
        stage("Install") {
            steps {
                sh "npm i -g pm2"
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
                sh "pnpm start:prod"
            }
        }
    }
}
