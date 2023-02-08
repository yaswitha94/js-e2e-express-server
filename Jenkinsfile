pipeline{
    agent { label 'openjdk-8' }
    stages{
        stage('vcs') {
            steps{
                git url: 'https://github.com/yaswitha94/js-e2e-express-server.git',
                branch: 'main'
            }
        }

        stage('build') {
            steps{
                sh 'npm install'
                sh 'npm run build'
            }
        }
    }
}