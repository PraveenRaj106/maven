pipeline {
    agent{
        label 's1'
    }
    stages {
        stage('SCM-maven') {
            steps {
                git branch: 'main', url: 'https://github.com/PraveenRaj106/maven.git'
            }
        }
        stage('package-maven'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('SCM-script') {
            steps {
                git branch: 'feature', url: 'https://github.com/PraveenRaj106/maven.git'
            }
        }
        stage('run-script'){
            steps{
                sh 'sh script.sh'
            }
        }
    } 
}
