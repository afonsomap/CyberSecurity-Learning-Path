# grep

### 1. Definition
A command-line utility used to filter and search through text line by line, displaying only the lines that match a specific pattern.

---

### 2. Basic Syntax
```bash
grep [options] "search_pattern" [file]
```

---

### 3. Tactical Flags (options)

| Flag | Name | Utility |
| :--- | :--- | :--- |
| -i | Ignore Case | Performs a case-insensitive search. |
| -v | Invert Match | Displays only the lines that do NOT match the pattern (noise reduction). |
| -r | Recursive | Searches through all files in a directory and its subdirectories. |
| -n | Line Number | Displays the specific line number where the match was found. |
| -c | Count | Returns only the number of matching lines (does not display the lines). |
| -l | Files with matches | Returns only the names of the files containing a match. |
| -E | Extended Regex | Enables extended regular expressions (supports symbols like |, +, ?). |

---

### 4. The Power of Pipes (|)
In security, grep is most powerful when used to filter output from other commands:

* **Filter network results:**
```bash
ss -tulpn | grep "80"
```

* **Filter logs in real-time:**
```bash
tail -f /var/log/apache2/access.log | grep "POST"
```

* **Clean up Dirb results:**
```bash
dirb http://target | grep "DIRECTORY"
```

### 5. Real-World SOC / Blue Team Scenarios

**1. Detect Brute Force (Log Analysis)**
Search for failed login attempts in Linux systems:
```bash
grep "Failed password" /var/log/auth.log
```

**2. Find Sensitive Configuration Files**
Search for the keywords "password" or "config" within the /etc directory:
```bash
grep -ri "password" /etc/ 2>/dev/null
```

**3. Extract Unique IPs from a Log**
```bash
grep -oE "[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}" log.txt | sort -u
```

### Shell Operators

| Symbol/Operator | Description |
| :--- | :--- |
| & | This operator allows you to run commands in the background of your terminal. | 
| && | This operator allows you to combine multiple commands together in one line of your terminal. |
| > | This operator is a redirector - meaning that we can take the output from a command (such as using cat to output a file) and direct it elsewhere. |
| >> | This operator does the same function of the > operator but appends the output rather than replacing (meaning nothing is overwritten). |
