## STEPS TO FOLLOW



## 1.) Installing some basic requiements....

```
sudo apt install git curl make

```

## 2.) Cloning the Openstack repositories

```
git clone https://opendev.org/openstack/openstack-helm-infra.git
git clone https://opendev.org/openstack/openstack-helm.git

```

## 3.) Copy the following command in the /etc/hosts file

```
net.bridge.bridge-nf-call-iptables = 1

```


## 4.) Run the following commands as superuser

```
modprobe br_netfilter
sysctl -p /etc/sysctl.conf

```


## 5.) Move into the Openstack-helm-infra folder and run the 3  commands given below

```
cd /openstack-helm-infra

```


```

sudo -H pip3 install --ignore-installed PyYAML
make dev-deploy setup-host
make dev-deploy k8s


```

Note: If the anyone of the 2 make commands give an error then just add sudo before running the command.

