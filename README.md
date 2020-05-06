# gitbranch1
I had installed docker,apache server and jenkins .
To run this # systemctl start docker
            # systemctl start HTTP
            ## systemctl start jenkins
Make a new repositotry in github
Make a file which have Git branch i.e master,dev1 and dev2 and merge them all and upload to github
Now give permission to access github file using jenkins: https://github.com/nasarjami/gitbranch1.git
make seprate operating sytem using docker such as for master:-
Now configure in jenkins
give permission to jenkins
sudo /etc/sudoers
#Make a operating system using docker 
if sudo docker ps | grep master
then 
echo "already running"
else 
sudo docker run -dit -p 8084:80 -v /master:/usr/local/apache2/htdocs/ --name master1 httpd 
fi
#And copy the content to apache server
sudo cp -v -r -f * /master..

And also give permission that job1 will Trigger only if build is stable i.e dev2
