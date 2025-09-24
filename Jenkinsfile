pipeline {
        agent {
  label 'dev'
}
    tools {
  maven 'Maven'
}
    stages {
        stage('git') {
            steps {
               git 'https://github.com/BVMohan3005/vamsi-sir-dicet_tv.git'
            }
        }
    stage('maven') {
            steps {
               sh 'mvn clean package'
            }
        }
    stage('tomcat') {
            steps {
              deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'tomcat', path: '', url: 'http://65.1.94.114:8080/')], contextPath: 'TV\'s', war: '"**/*.war"'
            }
        }
    }
}
