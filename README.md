# sqliv


# SQLiv - Advanced SQL Injection Scanner

<div align="center">

*Fully Updated: July 2, 2026*

</div>

**SQLiv is a lightweight and fast SQL injection vulnerability scanner. It helps you quickly identify potential injection points in web applications through intelligent crawling and dork-based searching.**

> **Important: This tool is designed for detection and scanning only, not for exploitation. It serves as a rapid assessment tool to identify vulnerable parameters.**



##  Key Features

- **Python 3.13+ Fully Compatible**
- **Multiple Detection Methods**: Error-based, Boolean-based, Time-based, and Union-based
- **Advanced Crawling**: Detects AJAX requests, hidden forms, and encoded URLs (Base64, URL-encoded)
- **Parallel Processing**: Multi-threaded scanning for better performance
- **Multiple Search Engines**: Google, Bing, Yahoo support
- **WAF Bypass Techniques**: Intelligent payload variations
- **Database Fingerprinting**: Identifies MySQL, PostgreSQL, MSSQL, Oracle, SQLite, and more
- **JSON Export**: Structured output for further analysis
- **Color Output**: User-friendly colored terminal display


# Clone the repository


```
git clone https://github.com/Layer-6/sqliv.git
cd sqliv
unzip sqlivi.zip -d sqliv
rm -rf sqlivi.zip
```


# *Usage Guide*

# Basic Commands

# 1. Scan a Single Target

```
python3 sqliv.py -t example.com
```

# 2. Dork-based Search

```
python3 sqliv.py -d "inurl:index.php?id=" -e google -p 20
```

**· -d: Dork query (e.g., inurl:index.php?id=)
· -e: Search engine (google, bing, yahoo)
· -p: Number of pages to fetch**

# 3. Reverse IP Scan

```
python3 sqliv.py -t example.com -r
```

# 4. Save Results to JSON

```
python3 sqliv.py -t example.com -o result.json
```


# Advanced Options

**Option Description Default
--level Scan depth (1-3, higher = more thorough) 2
--threads Number of concurrent threads 10
--timeout HTTP request timeout (seconds) 10
--depth Crawling depth 2
--no-color Disable colored output False
-s Save results even if no vulnerabilities found False**

# Example with Advanced Options:

```
python3 sqliv.py -t example.com --level 3 --threads 20 --timeout 15 -o result.json
```


 *Crawling Configuration*

*The crawler can be configured through Crawler class parameters:*


# In crawler.py

**crawler = Crawler(**
    depth=3,        **#Crawl depth**
    timeout=15,     **#Request timeout**
    threads=10,     **#Concurrent threads**
    user_agent=None **#Custom User-Agent**

**By Red**
***Telegram:*** t.me/RedRootedGhosT

