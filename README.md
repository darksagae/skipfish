# skipfish
**Skipfish** is a web application security scanner available in Kali Linux. It performs an active scan to identify vulnerabilities in web applications. Here’s how to use it, along with examples and expected output.

### Installation

Skipfish is typically pre-installed in Kali Linux. To check if it's available, run:

```bash
skipfish -V
```

If it’s not installed, you can install it using:

```bash
sudo apt update
sudo apt install skipfish
```

### Basic Usage

The basic syntax for using Skipfish is:

```bash
skipfish -o <output_dir> <URL>
```

- `-o <output_dir>`: Specifies the directory where the output files will be saved.
- `<URL>`: The target web application to scan.

### Example Command

To scan a web application, you can use the following command:

```bash
skipfish -o /path/to/output http://example.com/
```

### Detailed Example with Options

You can also specify additional options, such as user agents or dictionary files. Here’s an example:

```bash
skipfish -o /path/to/output -I -M 5 http://example.com/
```

- `-I`: Ignores SSL certificate warnings.
- `-M 5`: Sets the maximum number of concurrent requests.

### Expected Output

When you run Skipfish, you may see output similar to this:

```
[INFO] Starting scan at 2023-02-26 12:00:00
[INFO] Scanning http://example.com/
[INFO] Found links:
    - http://example.com/login
    - http://example.com/admin
    - http://example.com/api
...
[INFO] Scan complete: 200 URLs scanned, 50 issues found.
[INFO] Writing report to /path/to/output
```

### Report Generation

After the scan completes, Skipfish generates an HTML report in the specified output directory. You can open the report in a web browser to view detailed findings, including:

- Identified vulnerabilities (e.g., SQL injection, XSS)
- A summary of issues found
- A detailed breakdown of the scan results

### Conclusion

Skipfish is a powerful tool for assessing web application security. It automates the scanning process and provides a comprehensive report on potential vulnerabilities. Always ensure you have permission to test any web application to comply with ethical standards and legal requirements.




                       ALTERNATIVE
**Skipfish** is a web application security scanner included in Kali Linux. It is designed to perform active reconnaissance of web applications and identify potential vulnerabilities.

### Installation

Skipfish is typically pre-installed in Kali Linux. You can check if it's installed by running:

```bash
skipfish -h
```

### Basic Usage

The basic syntax for using Skipfish is:

```bash
skipfish -o <output_directory> <target_url>
```

- `-o <output_directory>`: Specifies the output directory for the scan results.
- `<target_url>`: The URL of the web application you want to scan.

### Example Usage

1. **Basic Scan**:

   To start a basic scan of a web application, use the following command:

   ```bash
   skipfish -o /path/to/output http://example.com
   ```

   Replace `/path/to/output` with your desired output directory and `http://example.com` with the target URL.

2. **Verbose Mode**:

   You can run Skipfish in verbose mode to get more detailed output during the scan:

   ```bash
   skipfish -o /path/to/output -v http://example.com
   ```

3. **Specify a Configuration File**:

   If you have a specific configuration file, you can use it like this:

   ```bash
   skipfish -o /path/to/output -c /path/to/config http://example.com
   ```

### Expected Output

Once the scan is complete, Skipfish will generate an HTML report in the specified output directory. The report includes:

- **Vulnerabilities Found**: A list of potential vulnerabilities identified during the scan, such as SQL injection, cross-site scripting (XSS), and more.
  
- **Site Map**: A visual representation of the web application’s structure, showing all URLs discovered during the scan.
  
- **Score**: A summary score indicating the overall security posture of the web application.

### Example Output Snippet

During the scanning process, you might see output like:

```
Starting scan on http://example.com
[INFO] Scanning...
[INFO] Discovered URL: http://example.com/login
[INFO] Discovered URL: http://example.com/dashboard
[WARNING] Potential XSS vulnerability found in http://example.com/login
[INFO] Scan complete. Generating report...
```

### Conclusion

Skipfish is an effective tool for quickly assessing the security of web applications. It provides comprehensive reports on vulnerabilities and helps security professionals identify areas for improvement. Always ensure you have permission to scan any web application to comply with ethical standards and legal requirements.



                           ALTERNATIVE
Skipfish is a web application scanner that is included in Kali Linux. It is used to identify vulnerabilities and weaknesses in web applications.

**Usage:**

The basic syntax for using Skipfish is:
```
skipfish [-h] [-f FORMAT] [-o OUTPUT] [-c CONFIG] [-v LEVEL] [-q] URL
```
**Options:**

* `-h`: Display help and exit.
* `-f FORMAT`: Specify the output format (html, xml, or text).
* `-o OUTPUT`: Specify the output file.
* `-c CONFIG`: Specify the configuration file.
* `-v LEVEL`: Specify the verbosity level (0-3).
* `-q`: Quiet mode (suppresses output).

**Example:**

To scan a web application, you can use the following command:
```
skipfish -o output.html https://example.com
```
This will scan the web application at `https://example.com` and save the results to an HTML file named `output.html`.

**Example Output:**

The output of Skipfish will vary depending on the scan results, but it typically includes information about:

* HTTP responses
* Cookies and sessions
* Input validation vulnerabilities
* SQL injection vulnerabilities
* Cross-site scripting (XSS) vulnerabilities
* Cross-site request forgery (CSRF) vulnerabilities
* File inclusion vulnerabilities
* Authentication and authorization issues

Here's an example of what the output might look like:
```
**Scan Results**

* HTTP Response Codes:
	+ 200 OK: 10 requests
	+ 404 Not Found: 2 requests
* Cookies and Sessions:
	+ Cookie "session_id" set by server
* Input Validation:
	+ Potential SQL injection vulnerability in parameter "id"
* XSS:
	+ Stored XSS vulnerability in parameter "username"
* CSRF:
	+ CSRF token not found
* File Inclusion:
	+ Potential file inclusion vulnerability in parameter "file"
* Authentication and Authorization:
	+ Authentication bypass vulnerability in login form
```
**Important Notes:**

* Skipfish should only be used with permission from the web application owner.
* Skipfish is a powerful tool that can potentially cause damage to a web application if used improperly.
* It's essential to review the scan results carefully and prioritize vulnerabilities based on their severity and impact.

I hope this helps! Let me know if you have any further questions.



                           ALTERNATIVE
Understood. I will provide information on using the Skipfish tool in Kali Linux without repeating the previous context.

Skipfish is a web application security reconnaissance tool included in Kali Linux. It can be used to gather information about a target website and identify potential vulnerabilities.

**Basic Usage**

The basic syntax for using Skipfish is:

```
skipfish [options] <target_url>
```

**Common Options**

- `-o <output_dir>`: Specify the output directory to save the crawl results.
- `-c <crawl_depth>`: Set the maximum crawl depth (default is 5).
- `-F`: Perform a forced directory-based crawl (ignores robots.txt).
- `-S <script_file>`: Specify a custom startup script.
- `-T <timeout>`: Set the request timeout in seconds (default is 10).
- `-v`: Increase the verbosity of the output.

**Example Usage**

1. **Basic Crawl**:
   ```
   skipfish -o output_dir http://example.com
   ```
   This command will perform a basic crawl of the `http://example.com` website and save the results in the `output_dir` directory.

2. **Forced Directory-based Crawl**:
   ```
   skipfish -F -o output_dir http://example.com
   ```
   This command will perform a forced directory-based crawl, ignoring the `robots.txt` file, and save the results in the `output_dir` directory.

3. **Custom Startup Script**:
   ```
   skipfish -S custom_script.txt -o output_dir http://example.com
   ```
   This command will use a custom startup script (`custom_script.txt`) during the crawl and save the results in the `output_dir` directory.

**Example Output**

The output of Skipfish will be saved in the specified output directory. The directory will contain several files, including:

- `/index.html`: The main crawl report, which includes a summary of the findings.
- `/sitemap_*.html`: Detailed sitemaps of the crawled website.
- `/signatures_*.txt`: Fingerprints of the identified web technologies.
- `/discovery_*.txt`: Lists of discovered URLs, forms, and other elements.

The report provides information about the target website, such as:

- Identified web technologies and versions
- Discovered pages and directories
- Forms and input fields
- Potential security issues and vulnerabilities

**Limitations and Considerations**

- Skipfish is a reconnaissance tool and does not exploit identified vulnerabilities.
- The effectiveness of Skipfish depends on the configuration and security measures of the target website.
- Always ensure you have permission to scan a website before using Skipfish, as unauthorized testing may be illegal.
- Refer to the Skipfish documentation and help output (`skipfish -h`) for the most up-to-date information and options.



                           ALTERNATIVE
**Skipfish** is an active web application security reconnaissance tool included in Kali Linux. It is designed to prepare an interactive sitemap for a targeted site by performing a recursive crawl and dictionary-based probes. The resulting map is annotated with the output from various active security checks, making it a valuable tool for penetration testing.

### How to Use Skipfish

1. **Installation**: Skipfish is typically pre-installed in Kali Linux. If you need to install it, you can do so with the following command:
   ```bash
   sudo apt install skipfish
   ```

2. **Basic Command Structure**:
   The basic syntax for running Skipfish is:
   ```bash
   skipfish -o <output_directory> -W <wordlist> <target_url>
   ```
   - `-o <output_directory>`: Specifies the directory where the output will be saved.
   - `-W <wordlist>`: Specifies the wordlist to use for the scan.
   - `<target_url>`: The URL of the web application you want to scan.

3. **Example Usage**:
   Here’s an example command to scan a WordPress site:
   ```bash
   skipfish -o /path/to/output -W /path/to/wordlist.txt http://192.168.1.202/wordpress
   ```

4. **Expected Output**:
   After running the command, Skipfish will provide a summary of the scan results. The output will include statistics such as:
   - Scan time
   - Number of HTTP requests made
   - Issues found categorized by severity (info, low, medium, high)
   - A report saved in the specified output directory

   An example output might look like this:
   ```
   Scan statistics:
   Scan time: 0:00:05.849
   HTTP requests: 2841 (485.6/s), 1601 kB in, 563 kB out (370.2 kB/s)
   Issues found: 10 info, 0 warn, 0 low, 8 medium, 0 high impact
   Report saved to '/path/to/output/index.html'.
   ```

### Conclusion

Skipfish is a powerful tool for web application security testing, providing detailed insights into potential vulnerabilities. By using a specified wordlist and output directory, users can effectively scan and analyze web applications for security weaknesses.

---
Learn more:
1. [Skipfish - Penetration Testing tool in Kali Linux - GeeksforGeeks](https://www.geeksforgeeks.org/skipfish-penetration-testing-tool-in-kali-linux/)
2. [skipfish | Kali Linux Tools](https://www.kali.org/tools/skipfish/)
3. [Skipfish - Penetration Testing tool in Kali Linux - kidnapshadow | by Kidnapshadow | Medium](https://medium.com/@kidnapshadow/skipfish-penetration-testing-tool-in-kali-linux-kidnapshadow-eceac38ba243)
