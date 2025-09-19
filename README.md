# security-take-home-assignment

## What is in the project
- Kubernetes Cluster
- Database
- FastAPI Todo application

## What should be done
- [ ] Run the python app in GKE and then connect it to database
- [ ] Store credentials in a secure place like secret manager
- [ ] Audit current firewall rules and make sure only necessary ports are open
- [ ] Improve security of the cluster and database
- [ ] Fix security vulnerabilities in the application code

## How to run

the following will update terraform in google cloud shell and enable required services:

chmod +x setup.sh
./setup.sh

```
make kubernetes.init
make kubernetes.plan
make kubernetes.apply
make database.init
make database.plan
make database.apply
```


