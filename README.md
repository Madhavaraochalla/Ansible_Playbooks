     FILE NAME                        EXPLANATION 
playbook1.yml         =         Creating user USING USER MODULE IN ALL HOSTS  madhav  in /tmp/maha file,
                                with shell /bin/bash ,uid 1212, comment "a regular user 

playbook2.yml         =         Installing appache2  USING APT MODULE IN ALL HOSTS 
                                Copying data in to apache2 s/w USING COPY MODULE ,
                                and Restart apache2 s/w USING SERVICE MODULE 

playbook3.yml         =         Copying file USING COPY MODULE 
                                From /etc/passwd 
                                to /tmp
                                
playbook4.yml        =        Installing tomcat and tomcat9-admin s/w's USING APT MODULE 
                              copying tomcat-users.xml file to /etc/passwd USING COPY MODULE 
                              Changing port number 8080 to 9090  USING REPLACE MODULE 
                              Restart service of tomcat, tomcat9-admin  USING SERVICE MODULE
                              After restart waiting 1 min  USING PAUSE MODULE 
                              Checking tomcat9 is responcer on host2 USING URI MODULE 
                      
                          VARIABLES
                      
playbook5.yml      =          Installing/uninstalling s/w's USING APT MODULE WITH VARIABLES
                              GLOBAL SCOPE VARIABLES
                              In command we can give ant software we want 
                              
                              ansible-playbook playbook5.yml -b  --extra-vars "a=tree b=present c=yes"
                            
playbook6.yml      =          Installing/uninstalling s/w's USING APT MODULE AND CREATING FILES USING FILE MODULE  WITH VARIABLES
                              GLOBAL SCOPE VARIABLES
                              same as playbook5.yml file 

playbook7.yml      =          Installing/uninstalling s/w's USING APT MODULE WITH VARIABLES
                              PLAY SCOPE VARIABLES                      
                              Here  variables given in palaybook we can give outside of the playbook also 
                              
                               ansible-playbook playbook5.yml -b  --extra-vars "a=tree b=present c=yes"

               GROUP OF GVROUP WITH HOST SCOPE VARIABLES

playbook8.yml      =         Installing/uninstalling s/w's USING APT MODULE WITH VARIABLES
                             HOST SCOPE VARIABLES                                
                             Here  we alredy create a file group_vars in server this playbook takes vaariables from that file 
                             it's works on server grouping 
       
             CREATING ON SINGLE SERVER 
             
playbook9.yml      =        Creating user with variables ON SERVER 1 USING USER MODULE        
                             name, password, uid, home, comment, shell.

                      LOOPS
                      
playboiok10.yml    =       Installing s/w's with loops USING APT MODULE 
                           S/W'S with lops like tree, maven, git.
