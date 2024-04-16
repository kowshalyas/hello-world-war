properties([
                        parameters([
                            choice(
                                choices: ['package', 'compile'], 
                                name: 'arg'
                            ),
                            string(
                                defaultValue:'', 
                                name: 'version', 
                                trim: true
                            )
                        ])
                    ])
    pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
