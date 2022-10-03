node {
    stage('Checkout') {
        
        deleteDir()
        checkout scm
    }

    stage('NPM Install') {

            sh 'npm install'
        
    }


    // stage('Lint') {
    //     sh 'ng lint'
    // }

    stage('Build') {
        milestone()
        sh 'ng build --prod '
    }


    stage('Deploy') {
        echo "Deploying..."
    }
}