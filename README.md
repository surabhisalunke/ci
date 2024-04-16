# ci
docker run -d -p 5000:5000 -e PORT=5000 \

-e LOCATION URL=http://localhost:5001 \ dotnetcoreservices/teamservice:location

docker run -d -p 5001:5001 -e PORT=5001 dotnetcoreservices/locationservice:nodb

docker images

curl -H "Content-Type:application/json" -X POST -d \

'{"id":"e52baa63-d511-417e-9e54-7aab04286281", "name":"KC"}' http://localhost:5000/teams

curl http://localhost:5000/teams/e52baa63-d511-417e-9e54-7aab04286281

curl -H "Content-Type:application/json" -X POST -d \

'{"id":"63e7acf8-8fae-42ce-9349-3c8593ac8292","firstName":"surabhi", "lastName":"salunke"}' http://localhost:5000/teams/e52baa63-d511-417e-9e54-7aab04286281/members

 curl http://localhost:5000/teams/e52baa63-d511-417e-9e54-7aab04286281
