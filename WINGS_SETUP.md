# 🦅 How to Connect Wings to your Panel

Once you have installed the Pterodactyl Panel and Wings using our toolkit, you need to connect them together. Follow these simple steps to configure your new Node.

## Step 1: Create a Location
1. Log in to your Pterodactyl Panel.
2. Click on the **Settings Gear (Admin)** in the top right corner.
3. On the left menu, go to **Locations**.
4. Click **Create New**. Give it a short code (e.g., `EU-1` or `US-East`) and a description.

---

## Step 2: Create the Node (Choose A or B)
Go to **Nodes** on the left menu and click **Create New**. 
*How you fill in this page depends on whether you want to use a Domain Name or an IP address.*

### Option A: Using a Domain Name with SSL (Recommended)
Use this option if you have linked a domain name (like `node1.yourdomain.com`) to your server IP.
* **Name:** Give your node a name (e.g., `Node-01`).
* **FQDN:** Enter the exact domain name of the server (e.g., `panel.yourdomain.com` or `node1.yourdomain.com`).
* **Communicate Over SSL:** `Use SSL Connection` *(Important: Browsers require this if your main panel uses HTTPS).*
* **Behind Proxy:** `Not Behind Proxy` (Unless you use Cloudflare, then select Behind Proxy).
* **Daemon Port:** `8080` (Do not change this).
* **Daemon SFTP Port:** `2022` (Do not change this).

### Option B: Using an IP Address (No SSL)
Use this option if you are running Wings on a remote machine and just want to connect via an IP address (e.g., `5.175.192.177`).
* **Name:** Give your node a name.
* **FQDN:** Enter the **IP Address** of your Wings server.
* **Communicate Over SSL:** `Use HTTP Connection`. *(Note: You will get a red warning if your main panel has SSL enabled, but it will still work).*
* **Daemon Port:** `8080` (Do not change this).
* **Daemon SFTP Port:** `2022` (Do not change this).

> ⚠️ **Important Note about Ports:**
> The Daemon Port (`8080`) is *only* used for the panel to talk to Wings. This is **not** the port players will use to join your game server! You will assign game ports in Step 3.

---

## Step 3: Assign IP & Game Ports (Allocations)
This is where you tell Pterodactyl which IP and Ports are available to assign to your game servers (like Minecraft or Rust).

1. Click on your newly created Node to open its settings.
2. Go to the **Allocation** tab.
3. Enter the IP address of your server.
4. Enter the ports you want to make available for your players. 
   * *Example for Minecraft:* Enter `25565-25575`.
   * *Example for a single port:* Enter `26652`.
5. Click **Submit**. 

---

## Step 4: Auto-Deploy Wings
1. Go to the **Configuration** tab of your Node.
2. You will see a block of code (starts with `cd /etc/pterodactyl && sudo wings configure...`). 
3. Click the **Generate Token** button to copy this command.
4. Open the SSH Terminal of the server where Wings is installed.
5. Paste the copied command and press Enter.

---

## Step 5: Start Wings
Once the configuration is applied, run the following command in your terminal to start the Wings service:

```bash
systemctl start wings
```
You can check if it's running smoothly by typing:
```Bash
systemctl status wings
```
Congratulations! Your node should now show a green heart icon in the Pterodactyl Panel, and you are ready to create servers using the ports you allocated!
