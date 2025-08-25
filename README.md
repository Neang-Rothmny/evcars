# Basic Website Deployment with GitHub Actions  

This project demonstrates how to deploy a basic website using **GitHub Actions** and a **Virtual Machine (VM)** configured with **Nginx** and **HTTPS**.  

---

## 🚀 Setup Overview  

1. **VM Setup**  
   - Install and configure **Nginx** as the web server.  
   - Generate a **self-signed SSL certificate** to enable HTTPS.  

2. **Ngrok Integration**  
   - Install **ngrok** to reverse proxy port `22`, allowing GitHub Actions to connect to the VM via SSH.  

3. **GitHub Actions Deployment**  
   - A GitHub Actions workflow (`.yml` file) is used to:  
     - Remove old code from the VM.  
     - Deploy the latest code from the GitHub repository into the VM.  

---

## ⚙️ Workflow  

- Push code changes to the `main` branch.  
- GitHub Actions automatically connects to the VM through ngrok.  
- The VM updates the website by replacing old files with the new version from GitHub.  

---

## 📝 Notes  

- This setup is for **basic demonstration and learning purposes**.  
- Using a self-signed certificate is **not recommended for production**.  
- For real-world deployments, consider using a domain name and trusted SSL certificates (e.g., via **Let’s Encrypt**).  
