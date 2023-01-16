pipeline {
    agent any
    stages {
        stage('Clonar repositorio') {
            steps {
                git 'https://github.com/danyelliot/CalculadorFinal.git'
            }
        }
        stage('Construir imagen') {
            steps {
                sh 'docker build -t calculador-python .'
            }
        }
        stage('Ejecutar pruebas') {
            steps {
                sh 'docker run -v $(pwd):/app -w /app calculador-python pytest'
            }
        }
        stage('Desplegar') {
            steps {
                sh 'docker push calculador-python'
            }
        }
    }
}

