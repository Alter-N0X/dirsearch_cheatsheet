
# dirsearch Usage Examples by Scan Type

### 1. Basic Path Discovery
- **Command**: Scan for default paths using built-in wordlist
  ```bash
  dirsearch -u http://example.com
  ```

---

### 2. Custom Extensions
- **Command**: Limit scan to files like PHP, HTML, JS
  ```bash
  dirsearch -u http://example.com -e php,html,js
  ```

---

### 3. Custom Wordlist
- **Command**: Use your own list of paths
  ```bash
  dirsearch -u http://example.com -w /path/to/wordlist.txt
  ```

---

### 4. Recursive Directory Bruteforce
- **Command**: Explore discovered directories recursively
  ```bash
  dirsearch -u http://example.com -r
  ```

---

### 5. Include or Exclude HTTP Status Codes
- **Command**: Only show results with HTTP 403
  ```bash
  dirsearch -u http://target.com -i 403
  ```
- **Command**: Exclude HTTP 403
  ```bash
  dirsearch -u http://target.com -x 403
  ```

---

### 6. File Extension Suffix Filter
- **Command**: Find only `.php` endpoints
  ```bash
  python3 dirsearch -u http://testphp.vulnweb.com --suffix .php
  ```

---

### 7. Save Report in Simple Text Format
- **Command**: Save output to a simple report file
  ```bash
  ./dirsearch -u http://testphp.vulnweb.com/ --simple-report=report.txt
  ```

---

### 8. Report in JSON or XML Format
- **JSON**:
  ```bash
  ./dirsearch -u http://testphp.vulnweb.com/ --json-report=report.json
  ```
- **XML**:
  ```bash
  ./dirsearch -u http://testphp.vulnweb.com/ --xml-report=report.xml
  ```

---

### 9. Force Extensions to All Wordlist Entries
- **Command**: Append extensions even if not using `%EXT%`
  ```bash
  dirsearch -u http://example.com -w list.txt -f -e php,html
  ```

---

### 10. Prefixes & Suffixes
- **Command**: Add custom prefixes or suffixes to wordlist entries
  ```bash
  dirsearch -u http://example.com --prefixes admin,secret --suffixes .bak,~
  ```

---

## Quick Example Summary

| Scan Type                   | Example Command                                                                 |
|----------------------------|----------------------------------------------------------------------------------|
| Basic discovery             | `dirsearch -u http://example.com`                                            |
| Specific extensions         | `-e php,html,js`                                                                |
| Custom wordlist             | `-w /path/to/wordlist.txt`                                                     |
| Recursive scan              | `-r`                                                                           |
| Include status codes        | `-i 403`                                                                       |
| Suffix filter               | `--suffix .php`                                                                |
| Save report (simple)        | `--simple-report=report.txt`                                                   |
| Force extensions            | `-f -e php,html`                                                               |
| Prefixes & suffixes         | `--prefixes admin --suffixes .bak`                                             |
