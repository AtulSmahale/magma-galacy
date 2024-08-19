# Deploy Magma Orchestrator

Create an Ubuntu VM, take reference from [multipass](docs/multipass.md) docs.

Quick Install:
```bash
sudo bash -c "$(curl -sL https://github.com/AtulSmahale/magma-galacy/raw/master/deploy-orc8r.sh)"
```

Switch to `magma` user after deployment has finsished:
```bash
sudo su - magma
```

Once all pods are ready, setup NMS login:
```bash
cd ~/magma-galacy
ansible-playbook config-orc8r.yml
```

You can get your `rootCA.pem` file from the following location:
```bash
cat ~/magma-galacy/secrets/rootCA.pem
```
