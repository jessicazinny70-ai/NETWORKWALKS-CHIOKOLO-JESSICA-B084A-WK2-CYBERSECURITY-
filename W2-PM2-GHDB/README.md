
# 📋 PENETRATION TESTING REPORT

## Google Dorking, Maltego & Network Scanning Phases

### W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS

| Field | Details |
|---|---|
| Pentester Name (Cybersecurity Professional) | Jessica Chiokolo |
| Program/Batch | B084 - Networkwalks |
| Date | 13 November 2026 |
| Modules Completed | W2-PM2 (Google Dorking) |
| | W2-PM3 (Maltego) |
| | W2-PM5 (Zenmap Scanning) |
| Client/Target | Authorized educational exercises and approved lab targets |

---

# 1. LIABILITY DISCLAIMER

This penetration testing report was prepared as part of the Networkwalks cybersecurity internship for educational purposes.

All activities were conducted using authorized targets, approved demonstrations and publicly available information. No unauthorized access or exploitation was performed.

The findings documented in this report are intended for educational and security awareness purposes.

---

# 2. INTRODUCTION

## 2.1 Project Overview

This project covers three cybersecurity practical modules: Google Hacking Database (GHDB) footprinting, Maltego-based footprinting and Zenmap network scanning.

The purpose of the project is to develop practical knowledge of information gathering, open-source intelligence (OSINT), relationship mapping and network discovery.

## 2.2 Project Objectives

- Understand Google Dorking and its applications.
- Identify publicly indexed information using GHDB.
- Perform footprinting and relationship mapping with Maltego.
- Discover hosts and examine network information using Zenmap.
- Document observations and security recommendations.

---

# 3. TOOLS USED

| No. | Tool | Purpose |
|---|---|---|
| 1 | Google Search | Advanced search and information gathering |
| 2 | Google Hacking Database (GHDB) | Finding Google Dorks |
| 3 | Maltego | OSINT and relationship mapping |
| 4 | Zenmap | Network scanning and host discovery |
| 5 | Nmap | Network scanning engine |

---

# 4. ACTIVITIES PERFORMED

## 4.1 W2-PM2: GOOGLE HACKING DATABASE (GHDB)

### 4.1.1 Introduction

Google Dorking uses advanced Google search operators to locate information indexed by search engines. The Google Hacking Database provides examples of search queries known as Google Dorks.

### 4.1.2 Task 1: Camera Footprinting

**Objective:** The GHDB searches returned different publicly accessible camera-related pages. Some results displayed live camera images, while others showed camera login pages or directory listings. The results demonstrate how Google Dorks can identify information indexed by search engines.
Another result identified a publicly accessible panoramic webcam page for Table Mountain in South Africa. It displayed a panoramic view with location labels and viewing controls. No username or password was displayed.
The search identified a publicly published camera page on CameraFTP named “SRSA - BASE CAM.” The page displayed a live outdoor view of a snow-covered recreational area. The camera was accessible without a visible login prompt, and no username or password was displayed. This demonstrates how search engines can index publicly published camera pages.
Another result displayed a SupervisionCam Protocol page named “Configuration1.svc.” The page showed a camera image, stated that 2,000 images had been saved, and displayed a live-camera timestamp. No username or password was visible.


| No. | Link | Relevant Dork | Username/Password (if any) |
|---|---|---|---|
| 1 | https://www.lmc.edu/webcam.htm | `intitle:"Webcam" inurl:WebCam.htm` | Not provided |
| 2 | https://ranch-turini.com/webcam/ | `intitle:"Index of /webcam/"` | Not provided |
| 3 | https://www.skylinewebcams.com/ | `inurl:webcam site:skylinewebcams.com inurl:roma` | Not required |
| 4 | https://www.insecam.org/en/bytype/webcamxp/ | [`intitle:"webcamXP" inurl:8080`](https://www.exploit-db.com/ghdb/7697) | Public listing; credentials not provided |
| 5 | [Webcams in Genemuiden](http://bremannet2.dyndns.tv:51030/multi.html) | `intitle:"Index of" "DCIM/camera"` | Not displayed / Not required |
| 6 | `http://75.149.26.30:1024/mobile.html` | `intitle:"webcamXP" inurl:8080` | Not displayed |
| 7 | http://webcam.turboprop.com | [Enter the Google dork used] | Not provided |
| 8 | https://tablemountain.panomax.com | [Enter the Google dork used] | Not provided |
| 9 | https://camerаftp.com/cameraftp/publish/Camera.aspx/parentID224864296/sharedID13751043/modelive/nameBASE%20WEBCAM | [Enter the Google dork you used] | Not displayed |
| 10 | https://users.globalnet.co.uk/~castanea/camera1.htm | [Enter the Google dork you used] | Not displayed |

### 4.1.3 Task 2: Mathematics PDF Directory

**Objective:** Identify and document 10 relevant mathematics PDF listings.

| No. | Link | Relevant Dork | Username/Password (if any) |
|---|---|---|---|
|
| No. | Link | Relevant Dork Used |
|---|---|---|
| 1 | https://erewhon.superkuh.com/library/Math/ | `intitle:index.of "parent directory" mathematics pdf` |
| 2 | https://pegaso.changeip.org/DOCS-TECH/Math/ | `intitle:"index of" "DOCS-TECH" Math` |
| 3 | https://discrete.openmathbooks.org/pdfs/ | `intitle:"index of" discrete mathematics pdf` |
| 4 | https://netlib.org/math/docpdf/ | `intitle:"index of" math docpdf` |
| 5 | https://openstax.org/subjects/math | `intitle:"OpenStax" mathematics textbook PDF` |
| 6 | https://math.libretexts.org/ | `intitle:"LibreTexts Mathematics" textbook PDF` |
| 7 | https://open.umn.edu/opentextbooks/subjects/mathematics | `intitle:"Open Textbook Library" mathematics PDF` |
| 8 | https://ocw.mit.edu/courses/mathematics/ | `site:ocw.mit.edu mathematics filetype:pdf` |
| 9 | https://www.ams.org/amsmtgs/ | `site:ams.org mathematics notes filetype:pdf` |
| 10 | https://opentext.uleth.ca/courses.html | `site:opentext.uleth.ca mathematics textbooks` | Open Mathematics Textbooks |

### 4.1.4 Observation

The GHDB search exercise identified ten websites related to mathematics textbooks, learning materials, and PDF resources. All ten links were opened and reviewed to check their accessibility and relevance to the search.

The results included mathematics resource directories, open educational textbook platforms, university course materials, and mathematics learning resources. Some websites provided access to open textbooks and course materials, while others served as directories or resource pages.

This exercise demonstrated how Google search operators can help identify publicly accessible mathematics resources across different websites. It also showed the importance of opening and reviewing search results to confirm their relevance instead of relying only on search titles.

### 4.1.5 Evidence

![GHDB Search Screenshot](images/ghdb-search.png)

![GHDB Findings Screenshot](images/ghdb-findings.png)

---

## 4.2 W2-PM3: MALTEGO-BASED FOOTPRINTING

### 4.2.1 Introduction

Maltego is an OSINT tool used to gather and visualize information and relationships between different entities.

### 4.2.2 Objective

To use Maltego to perform footprinting and understand how information about a selected authorized target can be collected and visualized.

### 4.2.3 Tools Used

- Maltego
- Internet connection
- Authorized target/domain: [Insert target]

### 4.2.4 Activities Performed

**Step 1:** [Describe first activity.]

**Step 2:** [Describe second activity.]

**Step 3:** [Describe third activity.]

**Step 4:** [Describe fourth activity.]

### 4.2.5 Findings

| No. | Entity / Information | Result Obtained | Observation |
|---|---|---|---|
| 1 | [Insert entity] | [Insert result] | [Insert observation] |
| 2 | [Insert entity] | [Insert result] | [Insert observation] |
| 3 | [Insert entity] | [Insert result] | [Insert observation] |
| 4 | [Insert entity] | [Insert result] | [Insert observation] |
| 5 | [Insert entity] | [Insert result] | [Insert observation] |

### 4.2.6 Evidence

![Maltego Graph](images/maltego-graph.png)

![Maltego Results](images/maltego-results.png)

### 4.2.7 Observation

[Write what you learned and observed from the Maltego exercise.]

---

## 4.3 W2-PM5: ZENMAP-BASED NETWORK SCANNING

### 4.3.1 Introduction

Zenmap is the graphical user interface for Nmap. It is used to perform network discovery, identify active hosts and visualize network scan results.

For this exercise, I used Zenmap on my Windows computer to scan my local Wi-Fi network and identify the devices connected to it.

### 4.3.2 Objective

The objective of this exercise was to scan my own local Wi-Fi network using Zenmap, identify active hosts, record their IP and MAC addresses, count the discovered hosts and generate a network topology.

### 4.3.3 Network Configuration

| Field | Details |
|---|---|
| IPv4 Address | 192.168.1.179 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.1.1 |
| Network Range | 192.168.1.0/24 |
| Network Interface | Wi-Fi – Intel(R) Dual Band Wireless-AC 8265 |
| Computer Name | JESSIE-CLEMENT |

### 4.3.4 Scanning Activities

**Step 1: Identifying the Network Configuration**

I opened Windows Command Prompt and used the `ipconfig` command to identify my computer's network configuration. I recorded the IPv4 address, subnet mask and default gateway of my active Wi-Fi adapter.

The results showed that my computer's IPv4 address was `192.168.1.179`, with a subnet mask of `255.255.255.0` and default gateway of `192.168.1.1`.

**Step 2: Selecting the Network Target**

I opened Zenmap and entered `192.168.1.0/24` in the Target field. This represented the local network range I intended to scan.

**Step 3: Selecting the Scan Profile**

I selected the **Ping Scan** profile in Zenmap. This profile uses host discovery to identify devices that are active on the network.

**Step 4: Performing the Network Scan**

I started the scan using the command:

`nmap -sn 192.168.1.0/24`

The scan completed successfully in approximately 5.67 seconds. Zenmap checked 256 IP addresses within the specified network range.

**Step 5: Reviewing the Scan Results**

After the scan, I reviewed the Nmap output and identified two active hosts on the network:

- `192.168.1.1` – Default gateway/router.
- `192.168.1.179` – My Windows computer, identified by the hostname JESSIE-CLEMENT.

I also reviewed the host details and obtained the router's MAC address from the Zenmap scan. I used Windows `ipconfig /all` to obtain my computer's Wi-Fi MAC address.

### 4.3.5 Network Scan Findings

The scan identified two live hosts within the local network.

| No. | IP Address | Hostname / Device | Status | MAC Address |
|---|---|---|---|---|
| 1 | 192.168.1.1 | Router - Tozed Kangwei Tech | Up | 98:A9:42:88:FB:B7 |
| 2 | 192.168.1.179 | JESSIE-CLEMENT (My Computer) | Up | 0C-54-15-4A-A4-C0 |

**Scan Summary:**

- Network scanned: `192.168.1.0/24`
- Total IP addresses scanned: 256
- Total active hosts discovered: 2
- Scan type: Ping Scan
- Scan command: `nmap -sn 192.168.1.0/24`
- Scan duration: Approximately 5.67 seconds

**MAC Address Note:** The router's MAC address was obtained from Zenmap's scan results. My computer's MAC address was obtained separately through Windows `ipconfig /all`.

### 4.3.6 Network Topology

After completing the scan, I opened the Topology section in Zenmap to view the graphical representation of the discovered network hosts.

The topology displayed the network gateway and my computer as the two active hosts discovered during the scan. I enabled the topology legend and used the Save Graphic option to save the network topology in PDF format.

The file was saved as:

`W2-PM5-Network-Topology.pdf`

This provided a visual representation of the devices discovered during the network scanning exercise.

### 4.3.7 Evidence

The following evidence will be included to demonstrate the activities performed:

1. Windows network configuration screenshot showing the IP address and subnet information.
2. Zenmap scan output showing the two active hosts discovered.
3. Zenmap host details showing the discovered device information.
4. Saved network topology PDF.

**Evidence files to add to the repository:**

- `images/network-configuration.png`
- `images/zenmap-scan-results.png`
- `images/zenmap-host-details.png`
- `evidence/W2-PM5-Network-Topology.pdf`



---

# 5. RISK ANALYSIS / IMPACT

| No. | Finding / Observation | Potential Impact | Risk Level |
|---|---|---|---|
| 1 | [Insert finding] | [Insert impact] | [Low/Medium/High] |
| 2 | [Insert finding] | [Insert impact] | [Low/Medium/High] |
| 3 | [Insert finding] | [Insert impact] | [Low/Medium/High] |
| 4 | [Insert finding] | [Insert impact] | [Low/Medium/High] |

---

# 6. RECOMMENDATIONS

1. Avoid exposing sensitive devices and services unnecessarily to the internet.
2. Use strong passwords and secure authentication.
3. Regularly review publicly indexed information belonging to your organization.
4. Monitor network devices and investigate unfamiliar hosts.
5. Keep systems and applications updated.
6. Conduct regular security assessments with proper authorization.

---

# 7. CONCLUSION

The Week 2 cybersecurity project provided practical experience in Google Dorking, OSINT footprinting using Maltego and network scanning using Zenmap.

The exercises improved my understanding of information gathering, digital footprint analysis, relationship mapping and network discovery.

---

# 8. EVIDENCE COLLECTED

The following evidence will be included to demonstrate the activities performed during the project.

| No. | Evidence Description | Module |
|---|---|---|
| 1 | GHDB search results | W2-PM2 |
| 2 | Camera footprinting findings | W2-PM2 |
| 3 | Mathematics PDF findings | W2-PM2 |
| 4 | Maltego graph | W2-PM3 |
| 5 | Maltego results | W2-PM3 |
| 6 | Windows network configuration | W2-PM5 |
| 7 | Zenmap scan results | W2-PM5 |
| 8 | Zenmap network topology | W2-PM5 |

---

**Prepared by:** Jessica Chiokolo  
**Program:** Networkwalks Cybersecurity Internship  
**Batch:** B084

