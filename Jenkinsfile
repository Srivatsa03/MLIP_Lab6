pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In Python, we can skip build step or install requirements here.'
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: Running pytest...'

                # Activate venv
                source mlip/bin/activate

                # Run pytest
                pytest

                echo 'pytest completed'
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project (if needed)'
            }
        }
    }
}