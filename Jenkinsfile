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
    stage('deploy') {
            steps {
              deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'tomcat', path: '', url: 'http://3.7.70.1:8080')], contextPath: 'tv\'s', war: '**/*.war'
            }
        }
    }
}
