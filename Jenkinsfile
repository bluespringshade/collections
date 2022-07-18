pipeline {
    agent any
    stages{
        stage('Test API Rest') {
            steps {
                sh 'newman run show-fact.postman_collection.json --disable-unicode  -e show-fact.postman_environment.json -d show-fact.csv --insecure --reporters=htmlextra,cli --reporter-htmlextra-logs true --reporter-htmlextra-export=- > output.txt'
            }
        }
    }
}
