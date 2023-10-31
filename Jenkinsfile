pipeline {
    agent any
    
    tools {
        maven "M3"
    }
    stages {
        stage('Checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/anagomezbe/lbg-hello-world-maven.git'
            }
        }
        stage('Compile'){
            steps {
                sh "mvn clean compile"
            }
        }
        stage('Test'){
            steps {
                sh "mvn test"
            }
        }
        stage('Package'){
            steps{
                sh "mvn -Dmaven.test.skip package -Dmaven.compile.skip package"
            }
        }
        //comment 2
    }
}