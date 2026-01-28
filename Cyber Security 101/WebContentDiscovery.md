# WebContentDiscovery

## dirb

### Description

A command-line tool used to find **hidden pages, directories, and files** within a web server.

### Logic

- It performs a **directory brute-force attack** by testing a list of common names (wordlist - roughly 4000 words) against a URL and analysing the **HTTP response codes**.
- There are many updated wordlists accessible on the internet that may be utilized as well.
- Dirb scans every directory or object of a website or server for the terms in its wordlist.

### Usage of dirb

```
# Basic scan using the default wordlist
dirb http://<target_ip_or_domain>/

# Scan using a specific wordlist
dirb http://<target_ip>/ /usr/share/wordlists/dirb/big.txt

# Scan a specific file extension
dirb http://<target_ip>/ -X .php
```

- It helps identify unlinked content, such as `/admin` panels, `/backup` files, or sensitive `/config` directories that are not visible to a regular user.

### HTTP Response Codes


| Code  | Meaning | Action | 
| ------------- | ------------- | ------------- |
| 200  | Success  | Found a live page. |
| 403  | Forbidden  | Directory exists but is protected.  |
| 301/2  | Redirect  | Page moved.  |
