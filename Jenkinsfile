// node {
//   stage('SCM') {
//     checkout scm
//   }
//   stage('SonarQube Analysis') {
//     def scannerHome = tool 'SonarScanner';
//     withSonarQubeEnv() {
//       bat "${scannerHome}/bin/sonar-scanner"
//     }
//   }
// stage('Quality Gate') {
//     timeout (time: 1, unit: 'HOURS') {
//       waitForQualityGate abortPipeline: true
//       echo "code is good"
//       def getURL = readProperties file: './.scannerwork/report-task.txt'
//       sonarqubeURL = "${getURL['dashboardUrl']}"
//       echo "${sonarqubeURL}"
//       bat 'echo env.sonarqubeURL > report.properties'
// //       bat 'echo ${sonarqubeURL} > report.properties'
//       archiveArtifacts artifacts: 'report.properties', onlyIfSuccessful: true
//     }
// }
// }
// node {
//   stage('SCM') {
//     cleanWs()
//     checkout scm
//   }
//   stage('SonarQube Analysis') {
//     def scannerHome = tool 'SonarScanner';
//     withSonarQubeEnv() {
//       bat "${scannerHome}/bin/sonar-scanner"
//     }
//   }
//   stage('Quality Gate') {
//     timeout (time: 3, unit: 'MINUTES') {
//       waitForQualityGate abortPipeline: true
//       echo "code is good"
//     }
//   }
// }

node {
  
  stage('Build_cause') {
    def causes = currentBuild.rawBuild.getCauses()
    def buildCause = causes.size() > 0 ? causes[0].getShortDescription() : "Unknown"
    env.BUILD_CAUSE = buildCause
    println "Build Cause: ${env.BUILD_CAUSE}"
  }
  
    stage('Checkout') {
        
        deleteDir()
        checkout scm
    }

    stage('NPM Install') {
        
//         nodejs('NodeJs') {
    // some block
//             bat 'npm install'
//             bat 'ng build --prod'
            echo "build sccess"
//             bat 'docker login -u "admin" -p "admin" 127.0.0.1:5000'
//             bat 'docker build -t 127.0.0.1:5000/myapp:1.1 .'
            // bat 'docker push 127.0.0.1:8082/repository/images/myapp:latest'
//             bat 'docker push 127.0.0.1:5000/myapp:1.1'
            // bat 'kubectl create secret docker-registry dockersecret --docker-server=127.0.0.1:8082 --docker-username=admin --docker-password=admin'
            // bat 'kubectl apply -f deployment.yaml'

//         }
//         kubeconfig(credentialsId: 'mykubeconfig', serverUrl: 'https://127.0.0.1:50321') {
//     // some block
//         // bat 'kubectl delete deployment angular-deployment'
//         bat 'kubectl apply -f deployment.yaml'
// }
        
    }
    stage('Deploy') {
        echo "Deploying..."
    }
}
