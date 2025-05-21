

# 🚀 BLOCKCAST NODE IS LIVE! 



---


🔹 **Step 1: Update the System**

```bash
sudo apt update -y && sudo apt upgrade -y
````

---

🔹 **Step 2: Install Docker**

```bash
# Remove old Docker versions if any
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

# Add Docker repository
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Install Docker Engine
sudo apt-get update
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Start and enable Docker
sudo systemctl start docker
sudo systemctl enable docker
```

---

🔹 **Step 3: Clone the Blockcast Repository**

```bash
git clone https://github.com/Blockcast/beacon-docker-compose.git
cd beacon-docker-compose
```

---

🔹 **Step 4: Pull Docker Images and Start the Node**

```bash
docker compose pull
docker compose up -d
```

---

🔹 **Step 5: Register the Node**

Run the following command to get your node’s registration details:

```bash
docker compose exec blockcastd blockcastd init
```

You will receive the following output — copy and save it:

* Hardware ID
* Challenge Key
* Registration URL

---

✅ **Register Your Node**

Open the registration page:

👉 [https://app.blockcast.network?referral-code=8zQUoz](https://app.blockcast.network?referral-code=8zQUoz)

Then follow these steps:
![c3fa3074ea6eae9cf3e0acec941e4c9d](https://github.com/user-attachments/assets/be2b85ff-63b8-44fc-82ae-3fb04dd59a53)

* Connect your Solana wallet
* Link your Twitter and Discord accounts
* Navigate to the "Manage Nodes" section
* Click on "Register Node"
* Paste the copied Hardware ID and Challenge Key
![Screenshot_1](https://github.com/user-attachments/assets/dc3c71da-c70e-429c-b0e1-03418867b6b2)
![Screenshot_2](https://github.com/user-attachments/assets/b2c8b358-e7a6-463d-aaad-e1bf572c9324)
![Screenshot_3](https://github.com/user-attachments/assets/5e7470a8-8261-411b-b7a2-03e34572c6fe)

💡 OR you can use the Registration URL shown in the terminal to register your node automatically on the website.

---



# ⚠️  **Backup**

Make sure to back up your private key:



**.blockcast/certs/gw\_challenge.key**


---

📢 **Follow for Updates:**
- Twitter: [https://x.com/Reza_Cryptoo](https://x.com/Reza_Cryptoo)
- Telegram: [https://t.me/Rezaa_Cryptoo](https://t.me/Rezaa_Cryptoo)





