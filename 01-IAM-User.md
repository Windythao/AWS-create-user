- refer https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/?fbclid=IwAR1bJKl4XHDL1VP0ICkPgsBY1DLFo5i_nhPQYMlaOfWvpNgBN51po8iuO5s
![image](https://user-images.githubusercontent.com/87864528/142994263-c30461ed-4ea8-450b-945c-2ce6a2d8b2cf.png)

![image](https://user-images.githubusercontent.com/87864528/142994711-3611aa6e-aaac-4fea-8fc8-bce396a4fbc4.png)

![image](https://user-images.githubusercontent.com/87864528/142995836-78414d2e-6cbe-43a5-88a8-b892810dd7fc.png)

- VPC for EC2 machine
![image](https://user-images.githubusercontent.com/87864528/142996613-4a1b783d-22d2-4af0-bc03-fdfed90ebf04.png)
Create V (EC2)
![image](https://user-images.githubusercontent.com/87864528/142996877-5a4572f0-c379-49f4-9112-60c5fcc1660a.png)
![image](https://user-images.githubusercontent.com/87864528/142996978-0096b8d8-dc5d-4e2a-a489-16fd2e55084d.png)
![image](https://user-images.githubusercontent.com/87864528/142997120-cf61d850-33bf-48da-9215-887cf596e47e.png)
![image](https://user-images.githubusercontent.com/87864528/142997363-7527237e-97df-4dac-8be4-13c601b72a48.png)
![image](https://user-images.githubusercontent.com/87864528/142997452-ab474ec6-c820-441e-a9fa-785fab686bd2.png)
![image](https://user-images.githubusercontent.com/87864528/142998015-2afbd0b6-b75f-4b2e-86a0-fb7ae6765cd9.png)
![image](https://user-images.githubusercontent.com/87864528/142998304-3f4cd1dc-e691-4154-852f-2f328e12c016.png)
![image](https://user-images.githubusercontent.com/87864528/142999332-f92812fc-710a-4f77-85d9-43cbec52d9dc.png)

![image](https://user-images.githubusercontent.com/87864528/143001092-8c2c1ca8-1e80-4f90-8303-3849744c6ce8.png)

[ec2-user ~]$ sudo yum update –y
Add the Jenkins repo using the following command:

[ec2-user ~]$ sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
Import a key file from Jenkins-CI to enable installation from the package:

[ec2-user ~]$ sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
[ec2-user ~]$ sudo yum upgrade
Install Jenkins:

[ec2-user ~]$ sudo yum install jenkins java-1.8.0-openjdk-devel -y
[ec2-user ~]$ sudo systemctl daemon-reload
Start Jenkins as a service:

[ec2-user ~]$ sudo systemctl start jenkins
You can check the status of the Jenkins service using the command:

[ec2-user ~]$ sudo systemctl status jenkins
Configure Jenkins
Jenkins is now installed and running on your EC2 instance. To configure Jenkins:

Connect to http://<your_server_public_DNS>:8080 from your favorite browser. You will be able to access Jenkins through its management interface:

   - Fix installation issue (error daemon..)
   ```
   33  sudo amazon-linux-extras install epel -y
   34  sudo yum update -y
   35  sudo yum install jenkins java-1.8.0-openjdk-devel
   36  sudo systemctl start jenkins
   37  sudo systemctl status jenkins
   cmd: type sudo su -> sudo cat /var/lib/jenkins/secrets/initialAdminPassword
   ```
   
![image](https://user-images.githubusercontent.com/87864528/143036463-9df90c9f-4b85-4092-883f-ca7efc498a3b.png)
![image](https://user-images.githubusercontent.com/87864528/143037195-8993cd8d-5d47-44bc-9008-992931a0c155.png)
![image](https://user-images.githubusercontent.com/87864528/143038039-9559b545-05a3-450a-9d99-8fa454e62174.png)
![image](https://user-images.githubusercontent.com/87864528/143038145-7d4271e8-f165-496f-8f6f-bd4243e6714a.png)
![image](https://user-images.githubusercontent.com/87864528/143038257-13a01075-f7b1-411a-ada0-cb89c6cc6ab9.png)

- Quiz:
![image](https://user-images.githubusercontent.com/87864528/143039186-206c929d-61bb-497e-b20d-477824c44c2f.png)
![image](https://user-images.githubusercontent.com/87864528/143039781-d19e7711-d051-4c88-bba8-f799cd00ca31.png)
![image](https://user-images.githubusercontent.com/87864528/143040246-33b56f4b-1cbf-4841-a375-560eb9deba3b.png)


