node {
     def app 
     stage('clone repository') {
      checkout scm  
    }
     stage('Build docker Image'){
      app = docker.build("myfirstdockeridqqqqqqq/hello-world-docker")
    }
    }
     stage('Push Image'){
       docker.withRegistry('https://registry.hub.docker.com', 'git') {            
       app.push("${env.BUILD_NUMBER}")            
       app.push("latest")   
   }
}