pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                echo 'echckout code...'
                echo "git clone git@github.com:Epoch-me/demo.git"
            }
        }
        stage('build') {
            steps {
                echo 'build code...'
                sh '''
                cd /root/demo/
                go build -o /root/helloworld . 
                '''
            }
        }
        stage('exec') {
            steps {
                echo 'exec code...'
                sh '''
                chmod +x /root/helloworld
                /root/helloworld
                '''
            }
        }
    }
}

