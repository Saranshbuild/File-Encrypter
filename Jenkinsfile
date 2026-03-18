node {
    try {
        stage('Build') {
            sh '''
            echo "Building project..."
            ls
            mkdir -p build
            echo "Dummy build file" > build/output.txt
            '''
        }

        stage('Test') {
            sh '''
            echo "Running tests..."
            echo "All tests passed"
            '''
        }

        stage('Deploy') {
            sh '''
            echo "Deploying..."
            tar -cvf app.tar build/
            '''
        }

        echo "Pipeline executed successfully!"

    } catch (Exception e) {
        echo "Pipeline failed!"
        throw e
    }
}
