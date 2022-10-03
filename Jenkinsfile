node {
    stage('Checkout') {
        
        deleteDir()
        checkout scm
    }

    stage('NPM Install') {

        nodejs('NodeJs') {
    // some block
            bat 'npm install'
            bat 'ng build --prod'
            echo "build sccess"
            bat 'docker build -t demo:latest .'
        }
        
    }
    stage('Deploy') {
        echo "Deploying..."
    }
}