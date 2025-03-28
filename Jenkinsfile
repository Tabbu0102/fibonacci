pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Tabbu0102/fibonacci.git'  // Change to your repo URL
            }
        }

        stage('Generate Fibonacci') {
            steps {
                script {
                    def fibonacci = { n ->
                        def sequence = [0, 1]
                        for (int i = 2; i < n; i++) {
                            sequence << (sequence[i - 1] + sequence[i - 2])
                        }
                        return sequence.take(n)
                    }

                    def userInput = 10  // Change this value or make it dynamic
                    echo "Fibonacci sequence up to ${userInput}: ${fibonacci(userInput)}"
                }
            }
        }
    }
}
