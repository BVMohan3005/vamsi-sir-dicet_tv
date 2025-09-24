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
    }
}
