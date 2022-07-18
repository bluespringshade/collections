pipeline {
    agent any
    stages{
        stage('Run Automation') {
            steps {
                sh 'newman run show-fact.postman_collection.json --disable-unicode  -e show-fact.postman_environment.json -d show-fact.csv --insecure -r junit,html --reporter-junit-export var/reports/newman/junit/newman.xml --reporter-html-export var/reports/newman/html/index.html'

            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'var/reports/newman/html', reportFiles: 'index.html', reportName: 'Newman API Test', reportTitles: ''])
            }
        }
    }
}
