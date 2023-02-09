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
                 withSonarQubeEnv('SONAR_SELF_HOSTED') {
                    sh 'npm install sonarqube-scanner'
                    sh 'npm run build sonar-scanner'
                }
            }
        }
    }
}