pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
    	sh 'python3 --version'
        stage("Unit test") {
            steps {
                sh "python3 test_calculador.py"
            }
        }
    }
}

