pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Deploy') {
            steps {
                deploy adapters: [tomcat7(credentialsId: '0d9061db-e717-4d2a-b07e-bbb7277a57f5', path: '', url: 'http://3.95.218.163:8080/')], contextPath: 'javawebapp', war: '**/java-web-project.war'
            }
        }
    }
}
