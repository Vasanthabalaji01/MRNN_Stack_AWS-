# MRNN_Stack_AWS-
MRNN Mysql_React_Node_Nginx in AWS fullstack develop to deployment

in client

    cd client 
    npm install
    npm run npm start

in backend

    cd backend
    npm install
    node index.js

client run in <ec2_ip>:3000
<br>
backend run in <ec2_ip>:8800
<br>
set your <ec2_ip>:8800 path in react to connect backend to frontend <br>
<br>
code
<br>
     client -> src -> pages -> Add.jsx, Books.jsx, Update.jsx #replace your <ec2_ip> <br>
<br>

upload in your ec2 

setup in enginx

    systemctl start nginx.service
    systemctl enable nginx.service

setup react app in nginx
    
    rm -rf * user/share/nginx/html
    cd home/ec2-user/client/build
    cp -r * user/share/nginx/html

start backend     

    cd home/ec2-user/backend
    node index.js
