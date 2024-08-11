# Google Dorking Guide for Web Penetration Testing

## Table of Contents

- [General Reconnaissance](#general-reconnaissance)
- [Sensitive Information Exposure](#sensitive-information-exposure)
- [Vulnerability Identification](#vulnerability-identification)
- [Directory & File Exposure](#directory--file-exposure)
- [Specific Technology Searches](#specific-technology-searches)
- [Error Messages & Debug Information](#error-messages--debug-information)
- [Information Disclosure](#information-disclosure)

## General Reconnaissance

- **site:.com**  
  Search for all indexed pages on the target domain.  
  **Example:** `site:target.com`

- **inurl:.com**  
  Search for URLs containing "target.com".  
  **Example:** `inurl:target.com`

- **intitle:"keyword" site:.com**  
  Search for pages with a specific keyword in the title.  
  **Example:** `intitle:"login" site:target.com`

- **allinurl site:.com**  
  Search for URLs with "admin" in them.  
  **Example:** `allinurl:admin site:target.com`

## Sensitive Information Exposure

- **filetype:pdf site:.com**  
  Find PDF files on the target site.  
  **Example:** `filetype:pdf site:target.com`

- **filetype:xls site:.com**  
  Find Excel files on the target site.  
  **Example:** `filetype:xls site:target.com`

- **filetype:doc site:.com**  
  Find Word documents on the target site.  
  **Example:** `filetype:doc site:target.com`

- **filetype:sql site:.com**  
  Search for SQL database dumps.  
  **Example:** `filetype:sql site:target.com`

- **"password" filetype:log site:.com**  
  Search for exposed logs containing "password".  
  **Example:** `"password" filetype:log site:target.com`

## Vulnerability Identification

- **inurl:".php?id=" site:.com**  
  Look for potential SQL injection points.  
  **Example:** `inurl:".php?id=" site:target.com`

- **inurl:"/wp-content/plugins/" site:.com**  
  Search for WordPress plugins that might be vulnerable.  
  **Example:** `inurl:"/wp-content/plugins/" site:target.com`

- **inurl:".env" "DB_PASSWORD" site:.com**  
  Search for exposed environment files with database credentials.  
  **Example:** `inurl:".env" "DB_PASSWORD" site:target.com`

- **inurl:"/phpinfo.php" site:.com**  
  Look for PHP info pages.  
  **Example:** `inurl:"/phpinfo.php" site:target.com`

## Directory & File Exposure

- **intitle:"index of /" site:.com**  
  Find directory listings.  
  **Example:** `intitle:"index of /" site:target.com`

- **"Parent Directory" inurl:.com**  
  Search for open directories.  
  **Example:** `"Parent Directory" inurl:target.com`

- **"Index of /admin" site:.com**  
  Look for admin directories.  
  **Example:** `"Index of /admin" site:target.com`

- **"Index of /uploads" site:.com**  
  Search for uploads directories.  
  **Example:** `"Index of /uploads" site:target.com`

- **"Index of /password" site:.com**  
  Look for directories containing password files.  
  **Example:** `"Index of /password" site:target.com`

- **"Index of /" "database.sql" site:.com**  
  Search for database dumps.  
  **Example:** `"Index of /" "database.sql" site:target.com`

## Specific Technology Searches

- **inurl:".asp" site:.com**  
  Find ASP files that may reveal server-side code.  
  **Example:** `inurl:".asp" site:target.com`

- **inurl:".jsp" site:.com**  
  Search for JSP files.  
  **Example:** `inurl:".jsp" site:target.com`

- **"Powered by WordPress" site:.com**  
  Identify WordPress sites.  
  **Example:** `"Powered by WordPress" site:target.com`

- **"Apache/2.4.49" site:.com**  
  Search for servers running specific software versions.  
  **Example:** `"Apache/2.4.49" site:target.com`

## Error Messages & Debug Information

- **"PHP Parse error" site:.com**  
  Search for PHP parse errors.  
  **Example:** `"PHP Parse error" site:target.com`

- **"Fatal error" site:.com**  
  Search for fatal errors.  
  **Example:** `"Fatal error" site:target.com`

- **"Warning: require" site:.com**  
  Look for missing file warnings.  
  **Example:** `"Warning: require" site:target.com`

## Information Disclosure

- **"phpinfo()" site:.com**  
  Find pages displaying PHP configuration.  
  **Example:** `"phpinfo()" site:target.com`

- **"Server at" inurl:.com**  
  Search for default server messages.  
  **Example:** `"Server at" inurl:target.com`

- **"Private" "Key" filetype:.PEM site:.com**  
  Search for exposed private keys.  
  **Example:** `"Private" "Key" filetype:PEM site:target.com`

- **"DB_PASSWORD" filetype:env site:.com**  
  Look for environment files exposing database passwords.  
  **Example:** `"DB_PASSWORD" filetype:env site:target.com`
