nour@nour-virtual-machine:~$ sudo su 
[sudo] password for nour: 
root@nour-virtual-machine:/home/nour# kubectl get nodes 
E0808 05:03:26.667059    3048 memcache.go:265] couldn't get current server API group list: Get "https://10.2.1.31:8443/api?timeout=32s": dial tcp 10.2.1.31:8443: connect: connection refused
E0808 05:03:26.667810    3048 memcache.go:265] couldn't get current server API group list: Get "https://10.2.1.31:8443/api?timeout=32s": dial tcp 10.2.1.31:8443: connect: connection refused
E0808 05:03:26.669548    3048 memcache.go:265] couldn't get current server API group list: Get "https://10.2.1.31:8443/api?timeout=32s": dial tcp 10.2.1.31:8443: connect: connection refused
E0808 05:03:26.671333    3048 memcache.go:265] couldn't get current server API group list: Get "https://10.2.1.31:8443/api?timeout=32s": dial tcp 10.2.1.31:8443: connect: connection refused
E0808 05:03:26.673113    3048 memcache.go:265] couldn't get current server API group list: Get "https://10.2.1.31:8443/api?timeout=32s": dial tcp 10.2.1.31:8443: connect: connection refused
The connection to the server 10.2.1.31:8443 was refused - did you specify the right host or port?
root@nour-virtual-machine:/home/nour# minikube start --driver=docker 
😄  minikube v1.19.0 on Ubuntu 20.04
❗  Deleting existing cluster minikube with different driver none due to --delete-on-failure flag set by the user. 

💢  Exiting due to GUEST_DRIVER_MISMATCH: The existing "minikube" cluster was created using the "none" driver, which is incompatible with requested "docker" driver.
💡  Suggestion: Delete the existing 'minikube' cluster using: 'minikube delete', or start the existing 'minikube' cluster using: 'minikube start --driver=none'

root@nour-virtual-machine:/home/nour# docker images 
REPOSITORY                                TAG        IMAGE ID       CREATED         SIZE
nourelhouda/ic-webapp                     v1.0       8327cef1eb6b   6 days ago      52.4MB
odoo                                      latest     ee2490ffb478   11 days ago     1.68GB
dpage/pgadmin4                            latest     9b6573409f3b   2 weeks ago     530MB
postgres                                  10         1cad456b3a24   13 months ago   202MB
gcr.io/k8s-minikube/storage-provisioner   v5         6e38f40d628d   2 years ago     31.5MB
k8s.gcr.io/kube-proxy                     v1.20.2    43154ddb57a8   2 years ago     118MB
k8s.gcr.io/kube-controller-manager        v1.20.2    a27166429d98   2 years ago     116MB
k8s.gcr.io/kube-apiserver                 v1.20.2    a8c2fdb8bf76   2 years ago     122MB
k8s.gcr.io/kube-scheduler                 v1.20.2    ed2c44fbdd78   2 years ago     46.4MB
k8s.gcr.io/etcd                           3.4.13-0   0369cf4303ff   2 years ago     253MB
k8s.gcr.io/coredns                        1.7.0      bfe3a36ebd25   3 years ago     45.2MB
k8s.gcr.io/pause                          3.2        80d28bedfe5d   3 years ago     683kB
root@nour-virtual-machine:/home/nour# history
    1  sudo apt-get update 
    2  sudo reboot
    3  grep -E --color 'vmx|svm' /proc/cpuinfo
    4  curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64   && chmod +x minikube
    5  apt  install curl
    6  curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64   && chmod +x minikube
    7  sudo mkdir -p /usr/local/bin/
    8  sudo install minikube /usr/local/bin/
    9  sudo apt-get install conntrack
   10  sudo apt-get install -y cri-tools
   11  curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
   12  sudo chmod +x minikube-linux-amd64
   13  sudo mv minikube-linux-amd64 /usr/local/bin/minikube
   14  minikube version
   15  curl -LO https://storage.googleapis.com/minikube/releases/v1.19.0/minikube-linux-amd64
   16  sudo chmod +x minikube-linux-amd64
   17  sudo mv minikube-linux-amd64 /usr/local/bin/minikube
   18  minikube version
   19  minikube start --driver=none
   20  minikube start --driver=none --force 
   21  sudo apt-get update
   22  sudo apt-get install ca-certificates curl gnupg
   23  sudo apt-get update
   24  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
   25  minikube start --driver=none 
   26  minikube start --driver=none --force 
   27  minikube start --driver=docker 
   28  systemctl status docker
   29  sudo apt update
   30  sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
   31  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   32  echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   33  sudo apt update
   34  sudo apt install -y docker-ce docker-ce-cli containerd.io
   35  sudo systemctl start docker
   36  sudo systemctl enable docker
   37  systemctl status docker
   38  minikube start --driver=docker 
   39  minikube start --driver=none --force 
   40  kubeclt get nodes 
   41  kubectl get nodes
   42  snap install kubectl
   43  kubectl get nodes
   44  sudo snap install kubectl --classic
   45  kubectl version --client
   46  kubectl get nodes
   47  git clone -b application  https://github.com/nourelhoudafdhila/cloudtemple.git applic
   48  ls
   49  docker images
   50  cd .. applic/
   51  ls
   52  cd applic
   53  ls
   54  cd app
   55  ls
   56  nano Dockerfile_v1.0
   57  docker build -f ./Dockerfile_v1.0 -t nourelhouda/ic-webapp:v1.0 .
   58  docker images 
   59  docker run -d --name ic-webapp-test -p 8000:8080 nourelhouda/ic-webapp:v1.0
   60  docker images 
   61  ls
   62  cd ..
   63  ls
   64  cd manifestes-k8s/
   65  ls
   66  cd ic-webapp/
   67  ls
   68  cd ..
   69  ls
   70  cd a
   71  ce app/
   72  cd app/
   73  ls
   74  docker ps -a | grep webapp
   75  clear
   76  docker ps -a | grep webapp
   77  ls
   78  cd ..
   79  ls
   80  cd manifestes-k8s/
   81  ls
   82  cd ic-webapp/
   83  ls
   84  nano ic-webapp-deployment.yml
   85  kubectl get ns
   86  ls
   87  kubectl create -f ic-webapp-namespace.yml
   88  kubectl get ns
   89  cd ..
   90  kubectl apply -f ./ic-webapp/
   91  kubectl get deploy -n ic-webapp
   92  kubectl get pods -n ic-webapp
   93  kubectl get svc -n ic-webapp
   94  kubectl describe  svc -n ic-webapp
   95  kubectl apply -f postgres/
   96  kubectl get svc -n ic-webapp
   97  kubectl get deploy  -n ic-webapp
   98  kubectl get sc  -n ic-webapp
   99  kubectl get secret  -n ic-webapp
  100  kubectl apply -f odoo/
  101  kubectl get secret  -n ic-webapp
  102  kubectl get deploy  -n ic-webapp
  103  kubectl get pv  -n ic-webapp
  104  kubectl get pvc  -n ic-webapp
  105  kubectl get svc  -n ic-webapp
  106  kubectl get deploy  -n ic-webapp
  107  kubectl get pods  -n ic-webapp
  108  cd /
  109  ll
  110  cd data_k8s/
  111  ll
  112  sudo mkdir -p /data_k8s/lib-odoo /data_k8s/pgadmin4 /data_k8s/postgres /data_k8s/addons /data_k8s/config
  113  sudo chmod 777 -R /data_k8s/lib-odoo /data_k8s/pgadmin4 /data_k8s/postgres /data_k8s/addons /data_k8s/config
  114  cd postgres/
  115  ll
  116  cd /data_k8s/lib-odoo/
  117  cd ..
  118  ls
  119  cd .. 
  120  ls
  121  kubectl get nodes 
  122  minikube start --driver=docker 
  123  docker images 
  124  history

