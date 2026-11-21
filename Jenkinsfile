pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Preparando aplicación Hello World...'
                sh 'test -f hello.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Verificando el código...'
                sh "grep -q 'Hello World!' hello.py"
                echo 'Prueba completada correctamente.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Despliegue simulado en entorno de prueba.'
            }
        }
    }
}
