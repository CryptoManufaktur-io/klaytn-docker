# klaytn-docker

Klaytn full node in docker compose

[Node deployment notes](https://docs.klaytn.foundation/installation-guide/deployment/endpoint-node/installation-guide) and [pruning notes](https://docs.klaytn.foundation/operation-guide/chaindata-migration)

Pruning benefits from 128GiB swap
```
sudo swapoff -a
sudo dd if=/dev/zero of=/swapfile bs=1M count=128K
sudo chmod 600 /swapfile
sudo mkswap /swapfile
echo '/swapfile none swap sw 0 0' | sudo tee --append /etc/fstab > /dev/null
echo 'vm.swappiness=1' | sudo tee --append /etc/sysctl.conf > /dev/null
sudo sysctl --load
```
