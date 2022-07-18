pipeline {
    agent any
    stage('Test API Rest') {
        steps {
            sh 'newman run show-fact.postman_collection.json --disable-unicode  -e show-fact.postman_environment.json -d show-fact.csv --insecure --reporters=htmlextra,cli --reporter-htmlextra-logs true --reporter-htmlextra-export=- > output.txt'

            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'var/reports/newman/html', reportFiles: 'index.html', reportName: 'Newman API Test', reportTitles: ''])
        }
    }
}
