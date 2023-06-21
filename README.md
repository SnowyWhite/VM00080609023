# Malicious Attachment Reverse Engineering

This repository contains the results of the reverse engineering analysis performed on a malicious mail attachment. 
The objective was to understand the behavior and functionality of the attachment in order to assess its potential risks and implications.

## Reverse Engineering Process

The reverse engineering process involved careful analysis and deobfuscation of the attachment's code.
It was aimed at identifying the various stages and uncovering the underlying functionality.
The code was thoroughly examined to understand its purpose, potential vulnerabilities, and any potential impact on the host system.
The discovered infrastructure of the threat actor used to receive harvested user credentials was examined and reported to the relevant parties.

## Repository Structure

## Assets

This folder contains some additional files that can be helpful in understanding the reverse engineering process and the threat actor's infrastructure:

- `attachment.eml`: Email attachment containing the malicious code.
- `Fake_MS_Login_Page.png`: Screenshot of the fake Microsoft login page used by the threat actor to harvest user credentials.
- `virustotal_1.png`: Screenshot of the [VirusTotal analysis](https://www.virustotal.com/gui/url/866e34a14911dcce6596eb433627ee1b24d18c9c6f5417874909bc6680a2640c) of the first domain used by the threat actor.
- `virustotal_2.png`: Screenshot of the [VirusTotal analysis](https://www.virustotal.com/gui/url/82183a6eea46d61cd5c16e765decbd307884219734ce5af86415e179b8c94cb4) of the second domain used by the threat actor.
- `httpx.sh`: Bash script used to retrieve details about the threat actor's infrastructure.
- `httpx.json`: JSON output of the `httpx.sh` script.
- `urls.txt`: List of URLs used by the malicious code.

## Stages

The repository is organized into the following folders, each representing a different stage of the attachment's code:

### Example
- `index.html`: HTML file that shows the fake Microsoft login page without the JavaScript code that would send the harvested credentials to the threat actor's infrastructure.

### Stage 1
- `obfuscated.html`: Obfuscated code of the initial stage.
- `deobfuscated.html`: Deobfuscated version of the initial stage.

### Stage 2
- `obfuscated.js`: Obfuscated code of the second stage.
- `deobfuscated.js`: Deobfuscated version of the second stage.
- `stage_3_request.http`: HTTP request sent by the second stage in order to retrieve the third stage.
- `stage_3_response.http`: HTTP response containing the third stage in form of a JSON array.

### Stage 3
- `obfuscated.js`: Obfuscated code of the final stage.
- `deobfuscated.js`: Deobfuscated version of the final stage.
- `request_ip_api.http`: HTTP request sent by the final stage to an [IP Geolocation API](https://pro.ip-api.com).
- `response_ip_api.http`: HTTP response containing geo-location information of the host system.

## Usage and Disclaimers

This repository is intended for educational and research purposes only. 
It is meant to serve as a reference for understanding the reverse engineering process undertaken to analyze the malicious attachment. 

Please exercise caution and use the information responsibly. 
The repository is provided "as is," without any warranties or guarantees regarding its accuracy or fitness for any particular purpose.
The owner and contributors of this repository shall not be held responsible for any misuse or damages resulting from the use of the information or code provided.

The hosting provider (https://www.cloudflare.com/) as well as the Domain Registrar (https://www.hostinger.com/) received an abuse report.

## Contributing

Contributions to this repository are not accepted as it is a static representation of the reverse engineering analysis.
However, if you have any suggestions or feedback, feel free to open an issue.

