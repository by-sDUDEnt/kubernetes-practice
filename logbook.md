### day1
- created config files for book_service(which is still not books, tbd in future)
- created config file for postgress db with init.sql script to fill in new data. Will be changed to migrations in the future. Doesnt really needed because of persistent volume claims, but useful for starting and checking whether app works as intented

**challenges faced:**
- had to double check right syntax for deployments service configmaps etc.
- had to implement init.sql in postgress deployment, because before it was done with docker-compose. Decided not to approach custom docker file for postgress db. I think is a better way to handle this things. Although i dont know whether I should keep init sql scrip in postgres config map or in a seperate file, which would complicate file structure and volumes.

**todo**
- connect the app to the postgress insides k8s - need to think how to properly hand urls in app to postgress, without hardcoding