# A Foodeys Vagrant Development Environment

To build and run the Java EE 7 app from https://github.com/JUGCologne/Foodeys in a CentOS virtual machine running NetBeans 7.3 and GlassFish 4:

    vagrant up
    vagrant ssh
    cd /downloads && ./download.sh && unzip \*.zip
    mkdir ~/NetBeansProjects
    cd ~/NetBeansProjects
    git clone https://github.com/JUGCologne/Foodeys.git
    exit
    vagrant halt
    vagrant up
    ssh vagrant
    /downloads/glassfish4/bin/asadmin start-database

Then log in to GNOME with vagrant/vagrant and:

- launch NetBeans with `/downloads/netbeans/bin/netbeans`
- add a GlassFish sever using the path `/downloads/glassfish4`
- open the Foodeys project
- click "Resolve" to initiate a priming build 
- run the project and <http://localhost:8080/Application/> should open
