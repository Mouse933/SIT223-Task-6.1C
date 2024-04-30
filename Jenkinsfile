pipeline {
    agent any

    environment {
        GIT_REPO = "https://github.com/Mouse933/SIT223-Task-6.1C.git/"
        BUILD_TOOL = "Maven"
    }
    
    stages {
        stage("Build") {
            steps {
                echo "Fetching code from repository: $GIT_REPO"
                echo "Building code using $BUILD_TOOL"
            }
        }
        stage("Unit and Integration Tests") {
            steps {
                echo "Running unit tests (Automation tool specified later)"
                echo "Running integration tests (Tool specified later)"
            }
        }
        stage("Code Analysis") {
            steps {
                echo "Checking code using (insert tool here)"
            }
        }
        stage("Security Scan") {
            steps {
                echo "Running security scan using (insert sec tool here)"
                echo "Security scan complete, vulnerability assessment can be viewed at (insert bogus link)"
            }
        }
        stage("Deploy to Staging") {
            steps {
                echo "Deploying to staging server (insert staging server here as env var)"
            }
        }
        stage("Integration Tests on Staging") {
            steps {
                echo "Running integration tests on staging server"
                echo "Application functions as expected (maybe replace this with link to bogus log file)"
            }
        }
        stage("Deploy to Production") {
            steps {
                echo "Deploying to production server (insert prod server here)"
            }
        }
    }
}
