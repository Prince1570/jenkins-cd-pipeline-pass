pipeline {
agent any


environment {
DIRECTORY_PATH = 'C\\JenkinsPass\\pipeline-demo' // path of the code directory being fetched
TESTING_ENVIRONMENT = 'QA' // name of the testing environment
PRODUCTION_ENVIRONMENT = 'Patel Prince' // use YOUR name here
}


stages {
stage('Build') {
steps {
echo 'Fetch the source code from the directory path specified by the environment variable'
echo "DIRECTORY_PATH = ${env.DIRECTORY_PATH}"
echo 'Compile the code and generate any necessary artefacts'
}
}


stage('Test') {
steps {
echo 'Unit tests'
echo 'Integration tests'
}
}


stage('Code Quality Check') {
steps {
echo 'Check the quality of the code'
}
}


stage('Deploy') {
steps {
echo 'Deploy the application to a testing environment specified by the environment variable'
echo "Testing to ${env.TESTING_ENVIRONMENT}"
}
}


stage('Approval') {
steps {
echo 'Waiting 10 seconds to simulate manual approval...'
sleep time: 10, unit: 'SECONDS'
}
}


stage('Deploy to Production') {
steps {
echo "Deploying the code to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
}
}
}


post {
success { echo 'Pipeline completed successfully.' }
failure { echo 'Pipeline failed.' }
}
}