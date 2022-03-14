pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                sh'''rm -rf python
                git clone 'https://github.com/Ray-Shubham/python.git'
                '''
            }
        }
        stage('Creating Files') {
            steps {
                sh '''cd python
                touch file.txt file1.txt file3.txt
                '''
            }
        }
        stage('Git Modification Check') {
            steps {
                sh'''cd python
                pwd
                git remote set-url origin https://Ray-Shubham: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@github.com/Ray-Shubham/python.git
                python3 python_script.py
                '''
            }
        }
    }
}
