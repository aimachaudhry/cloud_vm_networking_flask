# Flask on Cloud VM (Assignment 2)

## Student Info
- Name: Aima Chaudhry
- Cloud Provider: Google Cloud (GCP)

## Video recording: 
- Zoom/Loom: 

## Steps
### 1. VM Creation
- Select **Create VM Instance**
- To create the smallest machine possible, select **E2-micro** as the machine type
- Change operating system from **Debian GNU/Linux** to **Ubuntu**
- Under **Networking** select **Allow HTTP Traffic** and **Allow HTTPS Traffic**
    - These open up Port 80 and Port 443, respectively
- Create Instance
<img width="802" height="191" alt="Screen Shot 2025-10-08 at 11 29 44 AM" src="https://github.com/user-attachments/assets/e07cff27-8195-4f37-823b-e6d190095868" />


### 2. Networking (Port 5003 Open)
- Create a new firewall rule to allow traffic to come into Port 5003
- Give the rule a name and a description
- For the **Target**, select **All instances in the network**
- For the Source IPv4 Range, enter the range **0.0.0.0/0**, which allows traffic from any external IP address to come in
- Under specified protocols and ports, selcect **TCP** and enter in **5003**
- Create the new rule and make sure it is active

 <img width="753" height="112" alt="Screen Shot 2025-10-08 at 2 42 14 PM" src="https://github.com/user-attachments/assets/cc9308c7-337f-44f5-a47f-441d11f291ce" />


### 3. OS Update + Python Install
[commands + screenshot]

### 4. Flask App Running
[screenshot of terminal + browser]

### 5. Public IP Access
URL: http://XX.XX.XXX.XXX:5003  
[screenshot]
