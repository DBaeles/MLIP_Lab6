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


                # TODO fill out the path to conda here
                conda activate mlip

                # TODO Complete the command to run pytest
                pytest

                #python3 -m venv mlip
                #source mlip/bin/activate
                #pip install pytest
                #pip install pandas
                #pip install numpy
                #pip install scikit-learn
                #pytest
                #deactivate

                echo 'pytest not runned'
                #exit 1 #comment this line after implementing Jenkinsfile
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
