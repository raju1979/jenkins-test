node {
    stage('Checkout SCM') {
        git branch: 'jenkins_test', url: 'git@github.com:raju1979/jenkins-test.git'
    }

    stage('Install node modules') {
        sh "npm install"
    }

    stage("Test") {
        sh "npm run test-headless"
    }

    stage("Build") {
        sh "npm run build --prod"
    }
}
