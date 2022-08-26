# AnsibleRoles
test for awx avec repo github
## add new organisation 

![Capture d’écran 2022-08-26 164536](https://user-images.githubusercontent.com/98552911/186943432-1606e819-d238-4a1d-a32f-c9973b277aed.png)
## add new inventory "test" with one ec2-instance
![Capture d’écran 2022-08-26 164651](https://user-images.githubusercontent.com/98552911/186943634-817437f3-4970-4dcc-8772-c0ba63eb5b33.png)
![Capture d’écran 2022-08-26 164900](https://user-images.githubusercontent.com/98552911/186943972-06a108cc-696d-435b-8a34-e905304d62c4.png)
## ceate new project with github scm ("test-playbooks")
check the github repo that contains the ansible playbook that we will run against ec-2 machine 
![Capture d’écran 2022-08-26 165035](https://user-images.githubusercontent.com/98552911/186944397-71531849-e811-46ab-8818-da092cab9621.png)
## playbook it's just for test with motd task
    - name: Configure systems
      hosts: 15.188.50.218
      become: yes

      tasks:

    - name: Call Roles
      hosts: 15.188.50.218
      roles:
       #- hostname
       #- firewalld
       #- ntp-config
       - motd
## add a template "configure motd" to the project "test-playbooks"
![Capture d’écran 2022-08-26 165932](https://user-images.githubusercontent.com/98552911/186945729-676931a7-08b2-4927-a03b-a30fc931d3f7.png)
![Capture d’écran 2022-08-26 170038](https://user-images.githubusercontent.com/98552911/186945962-1ed909ff-ee57-4abb-8f01-47ac912dede3.png)
## running the playbook within the template
![Capture d’écran 2022-08-26 170255](https://user-images.githubusercontent.com/98552911/186946374-6d23c253-c48a-489d-bbcb-4b8e89a0e248.png)
## the playbook was running succesfully in our ec2-instance 
![Capture d’écran 2022-08-26 170351](https://user-images.githubusercontent.com/98552911/186946660-ff2560c2-3a9b-4050-80ec-246be8d158d1.png)
