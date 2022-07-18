pipeline {
    agent any
    stages{
        stage('Run Automation') {
            steps {
                echo "Start running newman, please wait..."
                bat 'newman run "show-fact.postman_collection.json" --disable-unicode  -e "show-fact.postman_environment.json" --timeout-script=9999999 -d "show-fact.csv" --insecure --reporters=htmlextra,cli --reporter-htmlextra-logs true --reporter-htmlextra-export=- > output.txt'
//                 publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'newman/html', reportFiles: 'index.html', reportName: 'show-fact testing', reportTitles: ''])
                echo "Run Newman Success"
            }
        }
    }
}
