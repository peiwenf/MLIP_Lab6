pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # Fill out the path to conda and initialize it
                sudo /opt/conda/bin/conda init

                # Activate the Conda environment and run pytest
                sudo /opt/conda/bin/conda run -n my_env pytest

                # Comment out the exit line after implementation
                # echo 'pytest not runned'
                # exit 1
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
