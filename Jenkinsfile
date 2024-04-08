pipeline {
  agent any
  stages {
    stage('Start Docker') {
      steps {
        sh "service docker start"
      }
    }
    stage('scan') {
      steps {
        sh "docker run -v ${WORKSPACE}:/src --workdir /src returntocorp/semgrep --config p/ci --config p/security-audit --config p/secrets"
      }
    }
  }
}
