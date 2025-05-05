### day1
- created config files for book_service(which is still not books, tbd in future)
- created config file for postgress db with init.sql script to fill in new data. Will be changed to migrations in the future. Doesnt really needed because of persistent volume claims, but useful for starting and checking whether app works as intented

**challenges faced:**
- had to double check right syntax for deployments service configmaps etc.
- had to implement init.sql in postgress deployment, because before it was done with docker-compose. Decided not to approach custom docker file for postgress db. I think is a better way to handle this things. Although i dont know whether I should keep init sql scrip in postgres config map or in a seperate file, which would complicate file structure and volumes.

**todo**
- connect the app to the postgress insides k8s - need to think how to properly hand urls in app to postgress, without hardcoding **done in day2**


### day2
- linked postgres service and db to work
- change image tag to :latest
- read a lot of documentation

**todo**
- make fronted hosted on nginx **done in day3**
- delpoy to k8s cluster  **done in day3&**
- make ingress files **done in day3**


### day3
- added simple frontend and nginx and ingress. It should work as a reverse proxy, but I have problems with routing requests from frontend to backend
- added ingres to backedn also

**challanges faced**
- i have to figure out proper routing on frontend links - it shouldnt work only with hardcoded http:localhost/users

**todo**
- proper handling through ingress - it have to work with /users!

### day4
- read docs, thats it

welp, I figured out how should frontend work. Basiclly, it would works as I made it, purely because it shoudnt even work that way. I was using minikube last time, and, it worked because url in minikube worked without any kubectl proxy and long links - which I havent hardcoded into front end. 
As far as I understood, it should work based on "proxy: url" config in nginx, which would redirect onto ingress in k8s cluster - that way i wont have any hardcoded links in front end (proper way) and handling url to backend would be done by nginx! proper way for reverse proxy, as intended!

**todo** 
- config ngixn with proper proxy setting
- make db migrations
- utilyze helm charts