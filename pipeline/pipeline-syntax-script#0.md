pipeline {
    agent any;
    stages{
        stage("code"){
            steps{
             git url: "https://github.com/babluguptaji1/two-tier-flask-app.git", branch: "master"
                echo "code clone ho gaya.."
            }
        }
        stage("Build"){
            steps{
                echo "Dockerfile code Build clone ho gaya.."
            }
        }
        stage("Test"){
            steps{
                echo "Developer / Tester tester tests likh ke dega.."
            }
        }
        stage("Deploy"){
            steps{
                echo "Docker compose se deploy bhi ho gaya.."
            }
        }
    }
}
