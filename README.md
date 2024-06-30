# SIEM-Lab-Setup

Join me on a fun and insightful journey as I set up an Elastic SIEM lab at home!

# The Beginning 📚

I’ve been itching to get hands-on with Elastic SIEM for a while. I decided to roll up my sleeves and build a home lab using the Elastic Stack and a Kali Linux VM. Here’s how it all went down.

# Step 1: Elastic Account 🧙‍♂️

First things first, I needed an Elastic account. I headed over to Elastic Cloud and signed up for a free trial. After logging in, I created a new deployment for Elasticsearch, picked a region, and waited for it to set up. Pretty straightforward so far!

# Step 2: Kali Linux VM 🐧

Next up was setting up the Kali VM. I grabbed the VM from the official Kali website. I used VirtualBox for this. Once the VM was up and running, I logged in with the default credentials (kali for both username and password). It felt like unlocking a new level in a game!

# Step 3: Installing the Elastic Agent 🕵️‍♀️

Now, I needed to get the Elastic Agent on my Kali VM. In the Elastic SIEM instance, I navigated to the Integrations page, found “Elastic Defend,” and followed the steps to install it. Pasting the command into the Kali terminal and watching it install was oddly satisfying. I verified the installation with sudo systemctl status elastic-agent.service and saw that it was running smoothly.

# Step 4: Stirring Up Some Security Events ⚔️

Time to generate some action! I used Nmap to run some scans on my VM. Commands like sudo nmap <vm-ip> and nmap -sS <ip address> did the trick. Watching those security events pop up felt like magic. I ran a few more scans to make sure I had plenty of data to play with.

# Step 5: Hunting for Events in Elastic SIEM 🔎

I couldn’t wait to see the results. I jumped back into the Elastic Deployment, navigated to the “Logs” tab under “Observability,” and entered queries like message: Endpoint Network event. Seeing the logs filter out my Nmap scans was super cool. It felt like being a detective in a cyber thriller!

![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/1b704bc9-77b4-4389-8990-6c0558153722)

Next, I clicked on one of the events and could see the Nmap scan being performed.

![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/e9ecaf96-9927-4efe-98e2-c6218866fa45)


![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/f0b6bb77-72d9-46a7-9d5a-78eff97f7414)

# Step 6: Building a Dashboard 📊

I wanted a visual representation of my data, so I decided to create a dashboard. In the Elastic web portal, I navigated to “Dashboards” under “Analytics” and created a new one. Adding visualizations like area and line charts to show event counts over time was both fun and insightful. It made me appreciate the power of visual data.

![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/1182e767-a04d-4a78-a17e-6022e00d100e)

# Step 7: Setting Up Alerts 🚨

What’s a SIEM without alerts? I set up an alert to notify me of any Nmap scans. In the Elastic SIEM, I navigated to “Alerts,” managed rules, and created a new custom query rule to detect Nmap scans. I set it to send me an email notification. The first time the alert triggered, it felt like a mini victory!

![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/18070345-3bf4-47e7-a7ab-5ad7cb9c9aeb)


![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/25c30544-c58b-4daf-bcca-29fc3365f12e)


![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/12242bbc-2687-457e-8664-ad81a6593f1d)


![image](https://github.com/chaitravimore/SIEM-Lab-Setup/assets/43516784/fc68b4f2-377a-4bd9-87d9-8ef1c7a2215f)

# Wrapping Up 🎯

Setting up this Elastic SIEM lab was a fantastic learning experience. It gave me hands-on practice with security monitoring and incident response. 

Thanks for coming along on this adventure with me! If you have any questions or want to share your own experiences, feel free to reach out. Happy exploring! 🕵️‍♀️🚀






