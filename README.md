## 🕴️ Jenkins CI/CD Pipeline with Linux VM.
### Using: Linux Virtual Machine, Docker, Dockerhub, Github & Python (Flask Application).
#### The Documentation of Building my Pipeline Excludes Installation of the Technologies Used for Simplicity (Installing VM, Docker, Python)
#### For a more Concise, Illustrated Documentation of my Pipeline - https://aidensprojects.github.io/project2.html

#### ㅤ
#### ❓ Why use a Virtual Machine:
#### - To Facilitate pushing/pulling of github repositories, which is easier on my native os, windows.
#### + Why not use a VM? ~ Oppose to running the pipeline strictly on windows, using a vm allows to further improve my linux skills


#### ㅤ
### 🔩 Building the Pipeline:
- **Building Docker Image - via Dockerfile**
- **Port Forwarding: Running Docker Image mapping port to localhost:5000 via docker run -d -p 5000:5000 mypyapp:0.1**
- **Allowing Jenkins Users to Access Docker Socket - Prevents Permission Denied Error**
- **(sudo usermod -aG docker jenkins) (sudo systemctl restart jenkins)**
#### ㅤ
- **Jenkins Plugins, Install:**
- **CloudBess Docker Build and Publish Plugin**
- **SSH Agent Plugin**
<br>
