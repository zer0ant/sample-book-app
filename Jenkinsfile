pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    build()
                }
            }
        }
        stage('Deploy to DEV') {
            steps {
                script{
                    deploy("DEV", 1010) 
                }
            }
        }
        stage('Tests on DEV') {
            steps {
                script{
                    test("DEV")
                }
            }
        }
        stage('Deploy to STG') {
            steps {
                script{
                    deploy("STG", 1020) 
                }
            }
        }
        stage('Tests on STG') {
            steps {
                script{
                    test("STG")
                }
            }
        }
        stage('Deploy to PRD') {
            steps {
                script{
                    deploy("PRD", 1030)
                }
            }
        }
        stage('Tests on PRD') {
            steps {
                script{
                    test("PRD") 
                }
            }
        }
    }
}


def build() {
    echo 'Building of node application is starting ..'
    bat "dir"
    bat "npm -v"
    bat "npm install"

}

def deploy(String environment, int port) {
    echo "Deployment to ${environment} has started .."
   // bat "pm2 delete ${environment}"
   // bat "pm2 start -n \"${environment}\" index.js -- ${port}"
}

def test(String environment) {
    echo "Testing on ${environment} has started .."
   // bat "npm test"
}