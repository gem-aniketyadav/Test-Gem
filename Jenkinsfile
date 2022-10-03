node {
    stage('Checkout') {
        
        deleteDir()
        checkout scm
    }

    stage('NPM Install') {

        nodejs('NodeJs') {
    // some block
            sh 'npm install'
            sh 'ng build --prod'
            echo "build sccess"
    // sh 'docker build -t demo:latest .'
        }
        
    }
    stage('Deploy') {
        echo "Deploying..."
    }
}