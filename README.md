* Steps to spin up Jenkins
    * Install Jenkins on a Docker container
        ```sh
        docker pull jenkins/jenkins:lts
        ```
    * Run a container
        ```sh
        docker run --rm --detach --publish 8080:8080 --volume jenkins_home:/var/jenkins_home --name jenkins jenkins/jenkins:lts
        ```
    * Get initial Jenkins admin password
        ```sh
        docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
        ```
    * Install suggested plugins
    * Once plugins are all installed, you'll be prompt to create the admin user
    * Once admin user is set up, the initial set up finishes.



