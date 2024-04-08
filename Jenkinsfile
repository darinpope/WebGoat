pipeline {
  agent any
  stages {
    stage('scan') {
      steps {
        sh "docker run -v ${WORKSPACE}:/src --workdir /src returntocorp/semgrep --config p/ci --config p/security-audit --config p/secrets"
      }
    }
  }
}
