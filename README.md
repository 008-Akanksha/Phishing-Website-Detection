A phishing website is a common social engineering method that mimics trustful uniform resource locators (URLs) and webpages. The objective of this project is to train machine learning models and deep neural nets on the dataset created to predict phishing websites.
Here’s a summary of the features and how they are implemented in your project:

1. Address Bar Based Features:
These features are extracted directly from the URL and address bar.

Domain of the URL: Extracts the domain part of the URL. Phishers sometimes use strange or misleading domain names.

IP Address in URL: If the URL uses an IP address instead of a domain name, it might be phishing.

"@" Symbol in URL: Phishers may use the "@" symbol to hide the real domain behind a user-friendly URL.

Length of URL: Long URLs often hide phishing content. A URL longer than 54 characters is often suspicious.

Depth of URL: The number of subdirectories in the URL. Phishers may create deep URLs to confuse users.

Redirection "//" in URL: Suspicious if "//" is used beyond the standard position in the URL (i.e., after the protocol).

http/https in Domain name: Phishers sometimes include "http" or "https" in the domain to mislead users into thinking the site is secure.

Using URL Shortening Services: Shortened URLs often obscure the destination, which is common in phishing attempts.

Prefix or Suffix "-" in Domain: Phishers sometimes add dashes in the domain name to make it look similar to a legitimate site.

2. Domain Based Features:
These features focus on the domain and its properties.

DNS Record: Phishing websites often lack proper DNS records.

Web Traffic: Legitimate websites usually have traffic data. Phishing sites, however, are often new or have no traffic.

Age of Domain: New domains are often phishing sites because they tend to have a shorter lifespan.

End Period of Domain: Domains expiring soon can indicate a phishing site, as legitimate sites usually have a longer registration period.

3. HTML & JavaScript Based Features:
These features are extracted from the website’s HTML or JavaScript code.

IFrame Redirection: Phishers may hide content behind an invisible iframe.

Status Bar Customization: JavaScript can be used to modify the status bar, which is a sign of phishing.

Disabling Right Click: Phishers often disable the right-click functionality to prevent users from viewing the page source.

These features are extracted using various Python libraries like urllib, whois, requests, BeautifulSoup, and others. Each of these features can help classify URLs as phishing or legitimate by inspecting their structure, domain, and behavior.
