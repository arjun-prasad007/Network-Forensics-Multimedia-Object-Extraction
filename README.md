# Network Forensics: Multimedia Object Extraction 🕵️‍♂️📂

This project demonstrates the process of intercepting and recovering files (Images, HTML, etc.) from live network traffic using Wireshark. It highlights the security risks associated with unencrypted HTTP communication.
🎯 Project Overview
The goal was to perform a forensic analysis of a network session to reconstruct files that were transmitted in plain text.
🛠️ Methodology
Traffic Capture: Initiated a live packet capture on the Wi-Fi interface to monitor data flow.
Target Interaction: Accessed an unencrypted Apache default page (http://icio.us) to generate reconstructible HTTP traffic.
Object Identification: Utilized Wireshark’s Export Objects feature to analyze the HTTP stream and identify discrete files within the captured packets.
File Recovery: Successfully reassembled and extracted a .png image file directly from the captured network packets.
📊 Key Evidence
Captured Objects List
The following screenshot shows the list of objects identified by Wireshark from the network stream, including the ubuntu-logo.png file.
![](/assets/Website.png)
![](/assets/Export-data.png)

Recovered Artifact
Filename: ubuntu-logo.png
Content-Type: image/png
Status: Successfully reconstructed and saved to local storage.
⚠️ Security Insight
This experiment proves that any data (images, documents, or credentials) sent over HTTP can be easily intercepted and reconstructed by an attacker on the same network. This underscores the necessity of HTTPS/TLS encryption for all web communication.
