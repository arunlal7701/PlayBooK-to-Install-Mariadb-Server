# PlayBooK-to-Install-Mariadb-Server
PlayBooK to Install Mariadb Server
```
---
- name: "Installing And Configuring MariaDb"
  hosts: all
  become: true
  tasks:
    
    - name: "Mariadb - Installation"
      yum:
        name: mariadb-server
        state: present
          
    - name: "Mariadb - Restarting/Enabling"
      service:
        name: mariadb
        state: restarted
        enabled: true
