pipeline {
    agent any

    environment {
        GIT_REPO = "https://github.com/Mouse933/SIT223-Task-6.1C.git/"
        LOG_PATH = "/user/Jenkins/logs/"
        BUILD_TOOL = "Maven"
        UNIT_TEST_TOOL = "JUnit"
        INT_TEST_TOOL = "Citrus"
        CODE_ANALYSIS_TOOL = "CheckStyle"
        SECURITY_TOOL = "Spectral"
        STAGING_SERVER = "AWS EC2 Staging"
        PROD_SERVER = "AWS EC2 Production"
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
                echo "Preparing unit tests using $UNIT_TEST_TOOL"
                echo "Running unit tests"
                echo "Preparing integration tests using $INT_TEST_TOOL"
                echo "Running integration tests"
            }
        }
        stage("Code Analysis") {
            steps {
                echo "Installing $CODE_ANALYSIS_TOOL"
                echo "Sending code to static analysis tool $CODE_ANALYSIS_TOOL"
                echo "Checking code for bugs and issues"
                echo "Code check completed, results can be viewed at $LOG_PATH/$CODE_ANALYSIS_TOOL/results"
            }
        }
        stage("Security Scan") {
            steps {
                echo "Installing $SECURITY_TOOL"
                echo "Running security scan using $SECURITY_TOOL"
                echo "Security scan complete, vulnerability assessment can be viewed at $LOG_PATH/SECURITY_TOOL/results"
            }
        }
        stage("Deploy to Staging") {
            steps {
                echo "Accessing $STAGING_SERVER instance"
                echo "Checking if $STAGING_SERVER is online"
                echo "Deploying to staging server $STAGING_SERVER"
            }
        }
        stage("Integration Tests on Staging") {
            steps {
                echo "Running integration tests using $INT_TEST_TOOL on $STAGING_SERVER staging server"
                echo "Integration tests on program completed, view results at $LOG_PATH/$INT_TEST_TOOL/$STAGING_SERVER/results"
                echo "Note to self, potentially add input cases where user can move the stages along after checking information in results for each testing stage."
            }
        }
        stage("Deploy to Production") {
            steps {
                echo "Collecting information and code from $STAGING_SERVER"
                echo "Pushing to production server $PROD_SERVER"
                echo "Deploying to production server $PROD_SERVER"
            }
        }
    }
}
