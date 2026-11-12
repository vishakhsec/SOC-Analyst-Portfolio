# LetsDefend Event ID: 86 – SOC141: Phishing URL Detected


## 1. Alert Details

| Key | Value |
|---|---|
| Event ID | 86 |
| Event Time | March 22, 2021, 9:23 PM |
| Alert Name | SOC141 - Phishing URL Detected |
| Alert Level | Security Analyst |
| Source IP Address | 172.16.17.49 |
| Source Hostname | EmilyComp |
| Destination IP Address | 91.189.114.8 |
| Destination Hostname | mogagrocol.ru |
| Username | ellie |
| Request URL | `http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io` |
| User Agent | Chrome 79 on Windows 7 |
| Device Action | Allowed |


## Description

A phishing URL detection alert fired when the internal host EmilyComp (172.16.17.49), used by ellie, made an HTTP request to the external domain mogagrocol[.]ru. The URL carried the user’s email address (ellie@letsdefend.io) as a query parameter, and the firewall allowed the request through instead of blocking it.

What I needed to find out:

Is the destination actually malicious?,
Did the user interact with a phishing page?,
Were any credentials or other sensitive data exposed?


## 2. Investigation Timeline

| Date & Time | Activity | Observation |
|---|---|---|
| Mar 22, 2021, 9:23 PM | HTTP Request | EmilyComp accessed mogagrocol.ru. |
| Mar 22, 2021, 9:23 PM | Alert Generated | SOC141 - Phishing URL Detected. |
| Mar 22, 2021, 9:23 PM | Network Action | Request was Allowed. |


## 3. Investigation Steps

### Step 1: Reviewing the Alert

I started by reviewing the alert details in LetsDefend to understand what triggered the detection. I identified the source IP address, destination IP address, hostname, username, and suspicious URL involved in the activity.

I also checked the device action, which was recorded as **Allowed**, indicating that the request was permitted by the security device.

### Step 2: Investigating the Suspicious URL

Next, I focused on the suspicious URL and destination domain (`mogagrocol.ru`). I examined the URL structure and noticed that the user's email address was included as a query parameter.

I wanted to determine whether the domain or URL was associated with phishing activities or other malicious behaviour.

### Step 3: Checking Threat Intelligence

I identified the available Indicators of Compromise (IOCs), including the destination IP address, domain, and complete URL.

I used VirusTotal to examine the reputation of the URL and domain and review available security vendor detections. I also used AbuseIPDB to investigate the reputation of the destination IP address.

### Step 4: Reviewing Network and Email Activity

I reviewed the available network and email logs to understand how the user reached the suspicious website.

I focused on identifying related email activity, previous requests to the domain, and any additional suspicious connections associated with the affected device.

### Step 5: Checking User and Endpoint Activity

Finally, I focused on the activities associated with the affected user (`ellie`) and hostname (`EmilyComp`).

I looked for possible suspicious file downloads, unusual process execution, and other activities that could indicate further compromise.

I also considered whether there was any evidence of credential submission or additional communication with suspicious external destinations. 


## 4. MITRE ATT&CK Mapping


| Tactic | Technique | Technique ID | Evidence |
|---|---|---|---|
| Initial Access | Phishing: Spearphishing Link | T1566.002 | The affected device accessed a suspicious external URL. |


## 5. Indicators of Compromise (IOCs)

During the initial alert review, I identified the following indicators associated with the suspicious web request.

| IOC Type | Indicator | Description |
|---|---|---|
| Source IP | `172.16.17.49` | Internal IP address that made the request |
| Hostname | `EmilyComp` | Hostname of the affected device |
| Username | `ellie` | User associated with the activity |
| Destination IP | `91.189.114.8` | External IP address contacted by the device |
| Domain | `mogagrocol.ru` | Suspicious destination domain |
| URL | `http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io` | URL requested by the internal device |


## 6. Verdict

Based on my initial investigation, I identified a suspicious web request from the internal device `EmilyComp` (`172.16.17.49`) to the external domain `mogagrocol.ru`.

The request was associated with the user `ellie`, and the security device recorded the action as **Allowed**, meaning the connection was not blocked.

The URL also contained the user's email address as a parameter, which is worth investigating further.

At this stage, I cannot confirm whether the activity resulted in a successful phishing attack or compromised the user's system. Further analysis of threat intelligence results, network logs, and endpoint activity is required.

**Final Status:** Suspicious Activity – Further Investigation Required.


## 7. Containment & Recommendations

Based on my investigation, I recommend the following actions:

1. **Block the domain:** Block `mogagrocol.ru` if it is confirmed to be malicious.
2. **Check the device:** Review `EmilyComp` for suspicious files, downloads, or unusual processes.
3. **Check user activity:** Find out whether the user clicked the link or entered any login details.
4. **Monitor network traffic:** Check for any further connections to the suspicious domain or IP address.
5. **Reset the password:** If the user entered their credentials on a malicious website, reset their password.
6. **Create user awareness:** Remind users not to open suspicious links or emails.

These steps can help prevent further suspicious activity and protect the system.


## 8. Closure

I completed the initial investigation of this alert and identified the suspicious URL, destination IP, affected device, and user involved.

The connection was allowed, so further checks are needed to understand whether the user was affected. I have also included recommendations to help prevent similar activity in the future.

**Final Status:** Suspicious Activity – Further Investigation Required.
