# Nmap Cheat Sheet by Prime

## Introduction

This cheat sheet provides a quick reference guide for using Nmap, a powerful network scanning tool. Use this guide to quickly understand and execute common Nmap commands, including vulnerability scanning.

## Table of Contents

1. [Installation](#installation)
2. [Basic Usage](#basic-usage)
3. [Host Discovery](#host-discovery)
4. [Port Scanning](#port-scanning)
5. [Service Version Detection](#service-version-detection)
6. [OS Fingerprinting](#os-fingerprinting)
7. [Scripting](#scripting)
8. [Vulnerability Scanning](#vulnerability-scanning)
9. [Output Formats](#output-formats)
10. [Miscellaneous](#miscellaneous)

## Installation

Ensure that Nmap is installed on your system. You can download it from [https://nmap.org/download.html](https://nmap.org/download.html).

## Basic Usage

- Scan a target: `nmap target`
- Scan multiple targets: `nmap target1 target2`
- Specify a range: `nmap 192.168.1.1-50`

## Host Discovery

- Ping Scan: `nmap -sn target`
- TCP SYN Ping: `nmap -PS target`
- Disable DNS resolution: `nmap -n target`

## Port Scanning

- Scan specific ports: `nmap -p 80,443 target`
- Scan a range of ports: `nmap -p 1-100 target`
- Scan top N ports: `nmap --top-ports N target`
- Scan all 65535 ports: `nmap -p- target`

## Service Version Detection

- Detect service versions: `nmap -sV target`
- Aggressive service detection: `nmap -A target`

## OS Fingerprinting

- Guess OS: `nmap -O target`
- More aggressive OS detection: `nmap -O --osscan-guess target`

## Scripting

- Run a script: `nmap --script scriptname target`
- Run multiple scripts: `nmap --script script1,script2 target`
- Run scripts by category: `nmap --script default target`

## Vulnerability Scanning

- Scan for vulnerabilities: `nmap --script vuln target`
- Scan for CVEs: `nmap --script vuln,exploit target`

## Output Formats

- Save output to file: `nmap -oN output.txt target`
- Output in XML format: `nmap -oX output.xml target`
- Grepable output: `nmap -oG output.grep target`

## Miscellaneous

- Show host interfaces and routes: `nmap --iflist`
- Scan using a decoy: `nmap -D decoy1,decoy2,target`

## Contributing

Feel free to contribute by opening issues or creating pull requests. Your feedback is highly appreciated!

## License

This cheat sheet is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
