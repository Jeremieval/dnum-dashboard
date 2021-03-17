
# ZAP Scanning Report

Generated on Wed, 17 Mar 2021 13:29:26


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 5 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| X-Frame-Options Header Not Set | Medium | 4 | 
| Dangerous JS Functions | Low | 4 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 5 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 4 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 6 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 14 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy
* https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html
* http://www.w3.org/TR/CSP/
* http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html
* http://www.html5rocks.com/en/tutorials/security/content-security-policy/
* http://caniuse.com/#feat=contentsecuritypolicy
* http://content-security-policy.com/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 4
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/29107295.4a7e3d3f6d26dca8b303.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/29107295.4a7e3d3f6d26dca8b303.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/b1542cc239bf56c8a14913c0a930efe682b5cf86.5b28865a839ba2eb3ce2.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/b1542cc239bf56c8a14913c0a930efe682b5cf86.5b28865a839ba2eb3ce2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/pages/index-30b939c7b034dd236b8e.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/pages/index-30b939c7b034dd236b8e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 4
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/b1542cc239bf56c8a14913c0a930efe682b5cf86.5b28865a839ba2eb3ce2.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/b1542cc239bf56c8a14913c0a930efe682b5cf86.5b28865a839ba2eb3ce2.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/pages/_app-8f6621bcddc236d84082.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/pages/_app-8f6621bcddc236d84082.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Feature-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control and Pragma HTTP Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css](https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 5
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/images/favicon.png](https://standup.fabrique.social.gouv.fr/images/favicon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css](https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.17.8`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/images/favicon.png](https://standup.fabrique.social.gouv.fr/images/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css](https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scan rule will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://owasp.org/www-community/Security_Headers

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `/_next/static/KfiyiVxL3ic3g8HCXNzzp/_buildManifest`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `/_next/static/KfiyiVxL3ic3g8HCXNzzp/_buildManifest`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `/_next/static/KfiyiVxL3ic3g8HCXNzzp/_buildManifest`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/_next/static/KfiyiVxL3ic3g8HCXNzzp/_buildManifest`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�����쵫bs�(�Ľ�sx<\x001c%��:�����\x001a�'޲</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/pages/_app-8f6621bcddc236d84082.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/pages/_app-8f6621bcddc236d84082.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/polyfills-4beebf4ac9054f0bf4e6.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/polyfills-4beebf4ac9054f0bf4e6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/b1542cc239bf56c8a14913c0a930efe682b5cf86.5b28865a839ba2eb3ce2.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/b1542cc239bf56c8a14913c0a930efe682b5cf86.5b28865a839ba2eb3ce2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/","query":{},"buildId":"KfiyiVxL3ic3g8HCXN", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/polyfills-4beebf4ac9054f0bf4e6.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/polyfills-4beebf4ac9054f0bf4e6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/","query":{},"buildId":"KfiyiVxL3ic3g8HCXNzzp","nextExport":true,"autoExport":true,"isFallback":false}</script>`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/","query":{},"buildId":"KfiyiVxL3ic3g8HCXNzzp","nextExport":true,"autoExport":true,"isFallback":false}</script>`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/","query":{},"buildId":"KfiyiVxL3ic3g8HCXNzzp","nextExport":true,"autoExport":true,"isFallback":false}</script>`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/","query":{},"buildId":"KfiyiVxL3ic3g8HCXNzzp","nextExport":true,"autoExport":true,"isFallback":false}</script>`
  
  
  
  
Instances: 6
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css](https://standup.fabrique.social.gouv.fr/_next/static/css/ddf986770e2d0a7da98f.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/main-feb12231265cc48339e4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/webpack-e067438c4cf4ef2ef178.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/3ef630e34cd10ba68f9d468ac363ff81c534e1e9.3ed3ef7b4c6addce4cce.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/images/favicon.png](https://standup.fabrique.social.gouv.fr/images/favicon.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/d86a96f142bf646bcaebe9400d46eb8bf1b755b3.519bd62ddf6e1bed25de.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Other information
<p>In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/](https://standup.fabrique.social.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741824`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/sitemap.xml](https://standup.fabrique.social.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `67108864`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62914560`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217727`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/robots.txt](https://standup.fabrique.social.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217728`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741825`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr](https://standup.fabrique.social.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js](https://standup.fabrique.social.gouv.fr/_next/static/chunks/framework.a3ab6d70963b928e4674.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `805306368`
  
  
  
  
Instances: 14
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>29107295, which evaluates to: 1970-12-03 21:21:35</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3