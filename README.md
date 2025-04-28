A phishing website is a common social engineering method that mimics trustful uniform resource locators (URLs) and webpages. The objective of this project is to train machine learning models and deep neural nets on the dataset created to predict phishing websites.

Here’s a summary of the features. Each of these features can help classify URLs as phishing or legitimate by inspecting their structure, domain, and behavior:

--> Address Bar Based Features:These features are extracted directly from the URL and address bar.

1.Domain of the URL: Extracts the domain part of the URL. Phishers sometimes use strange or misleading domain names.

2.IP Address in URL: If the URL uses an IP address instead of a domain name, it might be phishing.

3."@" Symbol in URL: Phishers may use the "@" symbol to hide the real domain behind a user-friendly URL.

4.Length of URL: Long URLs often hide phishing content. A URL longer than 54 characters is often suspicious.

5.Depth of URL: The number of subdirectories in the URL. Phishers may create deep URLs to confuse users.

6.Redirection "//" in URL: Suspicious if "//" is used beyond the standard position in the URL (i.e., after the protocol).

7.http/https in Domain name: Phishers sometimes include "http" or "https" in the domain to mislead users into thinking the site is secure.

8.Using URL Shortening Services: Shortened URLs often obscure the destination, which is common in phishing attempts.

9.Prefix or Suffix "-" in Domain: Phishers sometimes add dashes in the domain name to make it look similar to a legitimate site.

 --> Domain Based Features:These features focus on the domain and its properties.

1.DNS Record: Phishing websites often lack proper DNS records.

2.Web Traffic: Legitimate websites usually have traffic data. Phishing sites, however, are often new or have no traffic.

3.Age of Domain: New domains are often phishing sites because they tend to have a shorter lifespan.

4.End Period of Domain: Domains expiring soon can indicate a phishing site, as legitimate sites usually have a longer registration period.

--> HTML & JavaScript Based Features: These features are extracted from the website’s HTML or JavaScript code.

1.IFrame Redirection: Phishers may hide content behind an invisible iframe.

2.Status Bar Customization: JavaScript can be used to modify the status bar, which is a sign of phishing.

3.Disabling Right Click: Phishers often disable the right-click functionality to prevent users from viewing the page source.

These features are extracted using various Python libraries like urllib, whois, requests, BeautifulSoup, and others. 
