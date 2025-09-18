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

#tf version may be outdated on google cloud shell.  run below to update to 1.13.3

wget -O - https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(grep -oP '(?<=UBUNTU_CODENAME=).*' /etc/os-release || lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform

```
make kubernetes.init
make kubernetes.plan
make kubernetes.apply
make database.init
make database.plan
make database.apply
```
