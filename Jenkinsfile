pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compilando y verificando la aplicación...'
                sh 'python3 -m py_compile hello.py test_hello.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Ejecutando pruebas unitarias...'
                sh 'python3 -m unittest -v'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Desplegando aplicación en entorno de prueba...'
                sh 'mkdir -p deploy-test'
                sh 'cp hello.py deploy-test/'
                sh 'python3 deploy-test/hello.py'
            }
        }
    }
}
