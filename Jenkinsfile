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
            bat 'docker login -u "admin" -p "admin" 127.0.0.1:8082'
            bat 'docker build -t 127.0.0.1:8082/repository/images/myapp:latest .'
            bat 'docker push 127.0.0.1:8082/repository/images/myapp:latest'
        }
        
    }
    stage('Deploy') {
        echo "Deploying..."
    }
}