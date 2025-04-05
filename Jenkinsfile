pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = 'C:\\sonar-scanner-5.0.1.3006-windows\\bin'
        SONAR_HOST_URL = 'http://localhost:9000'
        SONAR_PROJECT_KEY = 'MOHAMED'
        SONAR_LOGIN = 'sqa_6f08f2999ca95c317b44e116bca7c2f41ad891ae'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/geedi098/Jenkins.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('Moh') {
                   bat 'C:\\sonar-scanner-5.0.1.3006-windows\\bin\\sonar-scanner -Dsonar.projectKey=MOHAMED -Dsonar.sources=src -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqa_6f08f2999ca95c317b44e116bca7c2f41ad891ae'
                }
            }
        }
    }
}
