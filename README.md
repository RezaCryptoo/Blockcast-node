

# 🚀 BLOCKCAST NODE IS LIVE! 







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

* Connect your Solana wallet
* Link your Twitter and Discord accounts
* Navigate to the "Manage Nodes" section
* Click on "Register Node"
* Paste the copied Hardware ID and Challenge Key

💡 OR you can use the Registration URL shown in the terminal to register your node automatically on the website.

```


```markdown
---

# Backup Instructions

Make sure to back up your private key:

```

.blockcast/certs/gw\_challenge.key

```

Use Termius or a similar program to save this file securely on your system.
```



