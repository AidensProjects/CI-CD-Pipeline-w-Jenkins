## 🕴️ Jenkins CI/CD Pipeline with Linux VM.
### Using: Linux Virtual Machine, Docker, Dockerhub, Github & Python (Flask Application).
#### The Documentation of Building my Pipeline Excludes Installation of the Technologies Used for Simplicity (Installing VM, Docker, Python)
#### For a more Concise, Illustrated Documentation of my Pipeline - https://aidensprojects.github.io/project2.html
#### Prerequisites, other than the Technologies listed before, you will also need a Docker Account, and to log into that account in the VM.

#### ㅤ
#### ❓ Why use a Virtual Machine:
#### - To Facilitate pushing/pulling of github repositories, which is easier on my native os, windows.
#### + Why not use a VM? ~ Oppose to running the pipeline strictly on windows, using a vm allows to further improve my linux skills


#### ㅤ
### 🔩 Building the Pipeline:
- **⚙️ Building Docker Image - via Dockerfile**
- **Port Forwarding: Running Docker Image mapping port to localhost:5000 via docker run -d -p 5000:5000 mypyapp:0.1**

#### ㅤ
- **✔️ Allowing Jenkins Users to Access Docker Socket - Prevents Permission Denied Error**
- **root@user:~# "sudo usermod -aG docker jenkins"**
- **root@user:~# "sudo systemctl restart jenkins"**

#### ㅤ
- **💻 Jenkins Plugins, Install:**
- **CloudBess Docker Build and Publish Plugin**
- **SSH Agent Plugin**

#### ㅤ
- **🔑 Generating SSH Key, Type in Console:**
- **root@user:~# "ssh-keygen"**
- **root@user:~# "cat id_rsa.pub >>authorized_keys"**
- **🔌 Jenkins: Add Credentials -> Add SSH Username and Private Key**
- your_ip:8080/job/ssh-keys-testing/pipeline-syntax/  -> Generate Pipeline Script  -> Copy
- your_ip:8080/job/ssh-keys-testing/configure  -> Paste  (where is says "// some block")

#### ㅤ
- **🔨 Pipeline Stages:**
- **Copy and Paste - From Repository (Pipeline-Script.txt\) to Pipeline Script (your_ip:8080/job/Python-Pipeline/configure)**
- **^^ The IP in Pipeline-Script.txt is a random ip, just for demonstration purposes.**
- ** Run the Pipeline**

#### ㅤ
- **🏆 Check if Pipeline has Pushed to Github:**
- **Go to your Github Repository (https://github.com/AidensProjects/CI-CD-Pipeline-w-Jenkins) and add a Dumby File, make sure to add text**
- **Go to your Pipeline (your_ip:8080/job/Python-Pipeline/) and a New Stage should be added showing that the Pipeline is working.**
