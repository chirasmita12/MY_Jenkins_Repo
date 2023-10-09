node{
    
    stage('Clone repo'){
        git credentialsId: 'GIT-Credentials', url: 'https://github.com/chirasmita12/MY_Jenkins_Repo.git'
    }
    
    stage('Maven Build'){
        def mavenHome = tool name: "Maven-3.8.5", type: "maven"
        def mavenCMD = "${mavenHome}/bin/mvn"
        sh "${mavenCMD} clean package"
    }
       
       
    stage('Build Image'){
        sh 'docker build -t ashokit/mavenwebapp .'
    }
    
  
}
