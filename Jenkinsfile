pipeline {
    agent any

    stages {
        stage('Clonar i reposítorio') {
            steps {
                git branch: 'main', url: 'https://github.com/EBAC-QE/testes-e2e-ebac-shop.git'
            }
        }
         stage('Instalar dependência') {
            steps {
                sh '''npm install'''
            }
        }
         stage('Executar Testes') {
            steps {
               sh 'NO_COLOR=1 npm run Cy:run'
            }
        }
    }
}
