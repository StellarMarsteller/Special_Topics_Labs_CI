
node {

  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/StellarMarsteller/Special_Topics_Labs_CI.git'
  }

  stage('Build') {
    // you should build this repo with a maven build step here
    withMaven (maven: 'maven3') {
              sh "mvn package"
            }
  }

  post {
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }
}