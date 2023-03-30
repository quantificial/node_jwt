npm install express

curl -i localhost:3001/super-secure-resource

npm install jsonwebtoken

curl -X POST http://localhost:3001/login --header "Content-Type: application/json" --data '{ "username": "admin", "password": "admin" }'

return 

{"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjoiYWRtaW4iLCJpYXQiOjE2ODAxNDA3Mjd9.29YFUSPKpvqaIUdATe7OTiq25KEkTHLAU7mVNdkafgw"}


decode at jwt.io

{"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjoiYWRtaW4iLCJpYXQiOjE2ODAxNDEwMjZ9.hu7zwAE_Zz0RwE1778-jNLhgEhK4LL4WahKUQRYtkEs"}


curl -i localhost:3001/super-secure-resource --Header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjoiYWRtaW4iLCJpYXQiOjE2ODAxNDEwMjZ9.hu7zwAE_Zz0RwE1778-jNLhgEhK4LL4WahKUQRYtkEs'


$ curl -i localhost:3001/super-secure-resource --Header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjoiYWRtaW4iLCJpYXQiOjE2ODAxNDEwMjZ9.hu7zwAE_Zz0RwE1778-jNLhgEhK4LL4WahKUQRYtkEs'
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 75
ETag: W/"4b-Lg+7WB5KVI+TU7DOewT+Wm2MIYI"
Date: Thu, 30 Mar 2023 01:51:04 GMT
Connection: keep-alive
Keep-Alive: timeout=5

{"message":"Congrats admin! You can now accesss the super secret resource"}

