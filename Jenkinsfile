pipeline {
agent any
stages{
stage('clone and clean repo'){
steps {
    // bat "rmdir /Q /S Timesheet"
    bat "git clone https://github.com/Alaeddinehnana/Bootstrap4.git"
    bat "mvn clean -f Bootstrap4"
}

}
stage('Test'){

steps{ bat "mvn test -f Bootstrap4"
    
}}
stage('Deploy'){
steps {

bat "mvn package -f Bootstrap4"
bat "mvn deploy -f Bootstrap4"
bat "mvn sonar:sonar -f Bootstrap4"
}

}
}
}
