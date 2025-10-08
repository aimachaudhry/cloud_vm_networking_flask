# Flask on Cloud VM (Assignment 2)

## Student Info
- Name: Aima Chaudhry
- Cloud Provider: Google Cloud (GCP)

## Video recording: 
- Zoom: 

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
- Click on the SSH to update the operating system
- Enter in the code:
- ```bash
   sudo apt update && sudo apt upgrade -y
   ```
- Intsall git, python3, and pip by entering in the code: 
   ```bash
   sudo apt install git python3 python3-pip python3.13-venv -y
   ```  
<img width="560" height="116" alt="Screen Shot 2025-10-08 at 3 52 39 PM" src="https://github.com/user-attachments/assets/07b11761-556e-4d9d-90e7-8c02972185fb" />

<img width="618" height="128" alt="Screen Shot 2025-10-08 at 3 54 29 PM" src="https://github.com/user-attachments/assets/b8947e33-8cd6-421a-9935-5ee3a6d971bc" />

### 4. Flask App Running
- After installing python, copy the flask template:
```'bash
   git clone https://github.com/hantswilliams/HHA-504-2025-FlaskStarter.git
   cd HHA-504-2025-FlaskStarter/
   ```
-  Create a new virutal environment: 
    ````
    python3 -m venv venv
- Activate the virtual environment:
  ```'bash
  source venv/bin/activate
- Install the requirements:
    ```'bash
    pip install -r requirements.txt
- Run the app on port 5003
  ```'bash
  python3 app.py

- The flask application is now running
  
  <img width="822" height="408" alt="Screen Shot 2025-10-08 at 4 05 29 PM" src="https://github.com/user-attachments/assets/d84b835d-6e8f-4df2-abed-7b1ac38c8d51" />

  

### 5. Public IP Access
URL: http://XX.XX.XXX.XXX:5003  
[screenshot]
