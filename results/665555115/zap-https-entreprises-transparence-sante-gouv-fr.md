
# ZAP Scanning Report

Generated on Thu, 18 Mar 2021 19:26:06


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 5 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 5 | 
| Reverse Tabnabbing | Medium | 1 | 
| Vulnerable JS Library | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 9 | 
| Cookie Without SameSite Attribute | Low | 6 | 
| Dangerous JS Functions | Low | 3 | 
| Feature Policy Header Not Set | Low | 8 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Base64 Disclosure | Informational | 6 | 
| Information Disclosure - Suspicious Comments | Informational | 10 | 
| Modern Web Application | Informational | 8 | 
| Non-Storable Content | Informational | 8 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 7 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 1 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1](https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://www.legifrance.gouv.fr/affichCodeArticle.do;jsessionid=045FFB6CF33D1C3F68F82C26D2ED3709.tpdila07v_3?idArticle=LEGIARTI000033219005&amp;cidTexte=LEGITEXT000006072665&amp;categorieLien=id&amp;dateTexte=">https://www.legifrance.gouv.fr/affichCodeArticle.do;jsessionid=045FFB6CF33D1C3F68F82C26D2ED3709.tpdila07v_3?idArticle=LEGIARTI000033219005&amp;cidTexte=LEGITEXT000006072665&amp;categorieLien=id&amp;dateTexte=</a>`
  
  
  
  
Instances: 1
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library jquery, version 1.8.3 is vulnerable.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `* jQuery JavaScript Library v1.8.3`
  
  
  
  
Instances: 1
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p>CVE-2015-9251</p><p>CVE-2019-11358</p><p>CVE-2012-6708</p><p></p>
  
### Reference
* https://nvd.nist.gov/vuln/detail/CVE-2012-6708
* https://github.com/jquery/jquery/issues/2432
* http://research.insecurelabs.org/jquery/test/
* http://blog.jquery.com/2016/01/08/jquery-2-2-and-1-12-released/
* http://bugs.jquery.com/ticket/11290
* https://blog.jquery.com/2019/04/10/jquery-3-4-0-released/
* https://nvd.nist.gov/vuln/detail/CVE-2019-11358
* https://nvd.nist.gov/vuln/detail/CVE-2015-9251
* https://github.com/jquery/jquery/commit/753d591aea698e57d6db58c9f722cd0808619b1b
* https://bugs.jquery.com/ticket/11974
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="general_growl_form" name="general_growl_form" method="post" action="/flow/WEB-INF/info_faq.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="j_idt298" name="j_idt298" method="post" action="/flow/WEB-INF/info_faq.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="general_growl_form" name="general_growl_form" method="post" action="/flow/WEB-INF/login.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="j_idt22" name="j_idt22" method="post" action="/flow/WEB-INF/info_contact.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form name="form" class="login-page" action="/flow/loginProcess" method="post">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="j_idt38" name="j_idt38" method="post" action="/flow/WEB-INF/login.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="j_idt35" name="j_idt35" method="post" action="/flow/WEB-INF/info_contact.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="general_growl_form" name="general_growl_form" method="post" action="/flow/WEB-INF/info_contact.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="j_idt22" name="j_idt22" method="post" action="/flow/WEB-INF/info_faq.xhtml" enctype="application/x-www-form-urlencoded">`
  
  
  
  
Instances: 9
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "general_growl_form" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr](https://entreprises-transparence.sante.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/](https://entreprises-transparence.sante.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/](https://entreprises-transparence.sante.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `BIGipServerpool-dgs-ts.cegedim.cloud-HTTP`
  
  
  * Evidence: `Set-Cookie: BIGipServerpool-dgs-ts.cegedim.cloud-HTTP`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/robots.txt](https://entreprises-transparence.sante.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/robots.txt](https://entreprises-transparence.sante.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `BIGipServerpool-dgs-ts.cegedim.cloud-HTTP`
  
  
  * Evidence: `Set-Cookie: BIGipServerpool-dgs-ts.cegedim.cloud-HTTP`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr](https://entreprises-transparence.sante.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `BIGipServerpool-dgs-ts.cegedim.cloud-HTTP`
  
  
  * Evidence: `Set-Cookie: BIGipServerpool-dgs-ts.cegedim.cloud-HTTP`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1](https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1](https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/theme.css?ln=primefaces-aristo](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/theme.css?ln=primefaces-aristo)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/theme/css/styles.css](https://entreprises-transparence.sante.gouv.fr/theme/css/styles.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/theme/css/base.css](https://entreprises-transparence.sante.gouv.fr/theme/css/base.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.css?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.css?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/theme/css/ie8.css](https://entreprises-transparence.sante.gouv.fr/theme/css/ie8.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/theme/css/ie9.css](https://entreprises-transparence.sante.gouv.fr/theme/css/ie9.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `D27CDB6E-AE6D-11cf-96B8-444553540000`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/](https://entreprises-transparence.sante.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `3o2kpt2xV21FPhgqJlLL3fNyljz02bbIr4BF3gKu9Kqo3+CDNreBi6nEyhDwVqf/8hW0dEBQ+qXMfBmuZWzR/kfGaeo=`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/fr-fr/excel-help/activer-ou-desactiver-les-macros-dans-les-fichiers-office-HA010354316`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/theme/css/base.css](https://entreprises-transparence.sante.gouv.fr/theme/css/base.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4gPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGRlZnM+PGxpbmVhckdyYWRpZW50IGlkPSJncmFkIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSIgeDE9IjUwJSIgeTE9IjAlIiB4Mj0iNTAlIiB5Mj0iMTAwJSI+PHN0b3Agb2Zmc2V0PSIwJSIgc3RvcC1jb2xvcj0iIzUzNTM1MyIvPjxzdG9wIG9mZnNldD0iMTAwJSIgc3RvcC1jb2xvcj0iIzJlMmUyZSIvPjwvbGluZWFyR3JhZGllbnQ+PC9kZWZzPjxyZWN0IHg9IjAiIHk9IjAiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIGZpbGw9InVybCgjZ3JhZCkiIC8+PC9zdmc+IA==`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr](https://entreprises-transparence.sante.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `5U8H4ioW6hEQzUwqJlLL3fNyljz02XMN7YxHsPMJ7T41pNy7SEwCp1iECWMawjx8uieROyFNBweubcCadzhsvHRot/M=`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/robots.txt](https://entreprises-transparence.sante.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `QHFcrAHorM6NbH0qJlLL3fNyljz02bN+oRUFVpKutZX3MRwgetXEZfygROP5FBemhzfLtkdva62l1aUpgERKEvoxFWk=`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x000fn�\x000c\x001e��\x0001:\x000f�uq���\x001f>�9�~x�M4</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 10
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "PrimeFaces.widget.PickList=PrimeFaces.widget.BaseWidget.extend({init:function(a){this._super(a);this.sourceList=this.jq.find("ul", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="logo-name"> <img src="/theme/images/header/logo-sunshine.png" alt="Transparence Santé : Espace entreprises" />
					</a>`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml?login_erreur=true)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="logo-name"> <img src="/theme/images/header/logo-sunshine.png" alt="Transparence Santé : Espace entreprises" />
					</a>`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1](https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="logo-name"> <img src="/theme/images/header/logo-sunshine.png" alt="Transparence Santé : Espace entreprises" />
					</a>`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_contact.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="logo-name"> <img src="/theme/images/header/logo-sunshine.png" alt="Transparence Santé : Espace entreprises" />
					</a>`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>").outerWidth(1).jquery){a.each(["Width","Height"],function(g,e){var f=e==="Width"?["Left","Right"]:["Top","Bottom"],h=e.toLowerCase(),k={innerWidth:a.fn.innerWidth,innerHeight:a.fn.innerHeight,outerWidth:a.fn.outerWidth,outerHeight:a.fn.outerHeight};function j(m,l,i,n){a.each(f,function(){l-=parseFloat(a.curCSS(m,"padding"+this,true))||0;if(i){l-=parseFloat(a.curCSS(m,"border"+this+"Width",true))||0}if(n){l-=parseFloat(a.curCSS(m,"margin"+this,true))||0}});return l}a.fn["inner"+e]=function(i){if(i===d){return k["inner"+e].call(this)}return this.each(function(){a(this).css(h,j(this,i)+"px")})};a.fn["outer"+e]=function(i,l){if(typeof i!=="number"){return k["outer"+e].call(this,i)}return this.each(function(){a(this).css(h,j(this,i,true,l)+"px")})}})}function c(g,e){var j=g.nodeName.toLowerCase();if("area"===j){var i=g.parentNode,h=i.name,f;if(!g.href||!h||i.nodeName.toLowerCase()!=="map"){return false}f=a("img[usemap=#"+h+"]")[0];return !!f&&b(f)}return(/input|select|textarea|button|object/.test(j)?!g.disabled:"a"==j?g.href||e:e)&&b(g)}function b(e){return !a(e).parents().andSelf().filter(function(){return a.curCSS(this,"visibility")==="hidden"||a.expr.filters.hidden(this)}).length}a.extend(a.expr[":"],{data:a.expr.createPseudo?a.expr.createPseudo(function(e){return function(f){return !!a.data(f,e)}}):function(g,f,e){return !!a.data(g,e[3])},focusable:function(e){return c(e,!isNaN(a.attr(e,"tabindex")))},tabbable:function(g){var e=a.attr(g,"tabindex"),f=isNaN(e);return(f||e>=0)&&c(g,!f)}});a(function(){var e=document.body,f=e.appendChild(f=document.createElement("div"));f.offsetHeight;a.extend(f.style,{minHeight:"100px",height:"auto",padding:0,borderWidth:0});a.support.minHeight=f.offsetHeight===100;a.support.selectstart="onselectstart" in f;e.removeChild(f).style.display="none"});if(!a.curCSS){a.curCSS=a.css}a.extend(a.ui,{plugin:{add:function(f,g,j){var h=a.ui[f].prototype;for(var e in j){h.plugins[e]=h.plugins[e]||[];h.plugins[e].push([g,j[e]])}},call:function(e,g,f){var j=e.plugins[g];if(!j||!e.element[0].parentNode){return}for(var h=0;h<j.length;h++){if(e.options[j[h][0]]){j[h][1].apply(e.element,f)}}}},contains:function(f,e){return document.compareDocumentPosition?f.compareDocumentPosition(e)&16:f!==e&&f.contains(e)},hasScroll:function(h,f){if(a(h).css("overflow")==="hidden"){return false}var e=(f&&f==="left")?"scrollLeft":"scrollTop",g=false;if(h[e]>0){return true}h[e]=1;g=(h[e]>0);h[e]=0;return g},isOverAxis:function(f,e,g){return(f>e)&&(f<(e+g))},isOver:function(j,f,i,h,e,g){return a.ui.isOverAxis(j,i,e)&&a.ui.isOverAxis(f,h,g)}})})(jQuery);
/*
 * jQuery UI Widget 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Widget
 */
(function(b,d){if(b.cleanData){var c=b.cleanData;b.cleanData=function(f){for(var g=0,h;(h=f[g])!=null;g++){try{b(h).triggerHandler("remove")}catch(j){}}c(f)}}else{var a=b.fn.remove;b.fn.remove=function(e,f){return this.each(function(){if(!f){if(!e||b.filter(e,[this]).length){b("*",this).add([this]).each(function(){try{b(this).triggerHandler("remove")}catch(g){}})}}return a.call(b(this),e,f)})}}b.widget=function(f,h,e){var g=f.split(".")[0],j;f=f.split(".")[1];j=g+"-"+f;if(!e){e=h;h=b.Widget}b.expr[":"][j]=function(k){return !!b.data(k,f)};b[g]=b[g]||{};b[g][f]=function(k,l){if(arguments.length){this._createWidget(k,l)}};var i=new h();i.options=b.extend(true,{},i.options);b[g][f].prototype=b.extend(true,i,{namespace:g,widgetName:f,widgetEventPrefix:b[g][f].prototype.widgetEventPrefix||f,widgetBaseClass:j},e);b.widget.bridge(f,b[g][f])};b.widget.bridge=function(f,e){b.fn[f]=function(i){var g=typeof i==="string",h=Array.prototype.slice.call(arguments,1),j=this;i=!g&&h.length?b.extend.apply(null,[true,i].concat(h)):i;if(g&&i.charAt(0)==="_"){return j}if(g){this.each(function(){var k=b.data(this,f),l=k&&b.isFunction(k[i])?k[i].apply(k,h):k;if(l!==k&&l!==d){j=l;return false}})}else{this.each(function(){var k=b.data(this,f);if(k){k.option(i||{})._init()}else{b.data(this,f,new e(i,this))}})}return j}};b.Widget=function(e,f){if(arguments.length){this._createWidget(e,f)}};b.Widget.prototype={widgetName:"widget",widgetEventPrefix:"",options:{disabled:false},_createWidget:function(f,g){b.data(g,this.widgetName,this);this.element=b(g);this.options=b.extend(true,{},this.options,this._getCreateOptions(),f);var e=this;this.element.bind("remove."+this.widgetName,function(){e.destroy()});this._create();this._trigger("create");this._init()},_getCreateOptions:function(){return b.metadata&&b.metadata.get(this.element[0])[this.widgetName]},_create:function(){},_init:function(){},destroy:function(){this.element.unbind("."+this.widgetName).removeData(this.widgetName);this.widget().unbind("."+this.widgetName).removeAttr("aria-disabled").removeClass(this.widgetBaseClass+"-disabled ui-state-disabled")},widget:function(){return this.element},option:function(f,g){var e=f;if(arguments.length===0){return b.extend({},this.options)}if(typeof f==="string"){if(g===d){return this.options[f]}e={};e[f]=g}this._setOptions(e);return this},_setOptions:function(f){var e=this;b.each(f,function(g,h){e._setOption(g,h)});return this},_setOption:function(e,f){this.options[e]=f;if(e==="disabled"){this.widget()[f?"addClass":"removeClass"](this.widgetBaseClass+"-disabled ui-state-disabled").attr("aria-disabled",f)}return this},enable:function(){return this._setOption("disabled",false)},disable:function(){return this._setOption("disabled",true)},_trigger:function(e,f,g){var j,i,h=this.options[e];g=g||{};f=b.Event(f);f.type=(e===this.widgetEventPrefix?e:this.widgetEventPrefix+e).toLowerCase();f.target=this.element[0];i=f.originalEvent;if(i){for(j in i){if(!(j in f)){f[j]=i[j]}}}this.element.trigger(f,g);return !(b.isFunction(h)&&h.call(this.element[0],f,g)===false||f.isDefaultPrevented())}}})(jQuery);
/*
 * jQuery UI Mouse 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Mouse
 *
 * Depends:
 *	jquery.ui.widget.js
 */
(function(b,c){var a=false;b(document).mouseup(function(d){a=false});b.widget("ui.mouse",{options:{cancel:":input,option",distance:1,delay:0},_mouseInit:function(){var d=this;this.element.bind("mousedown."+this.widgetName,function(e){return d._mouseDown(e)}).bind("click."+this.widgetName,function(e){if(true===b.data(e.target,d.widgetName+".preventClickEvent")){b.removeData(e.target,d.widgetName+".preventClickEvent");e.stopImmediatePropagation();return false}});this.started=false},_mouseDestroy:function(){this.element.unbind("."+this.widgetName);if(this._mouseMoveDelegate){b(document).unbind("mousemove."+this.widgetName,this._mouseMoveDelegate).unbind("mouseup."+this.widgetName,this._mouseUpDelegate)}},_mouseDown:function(f){if(a){return}(this._mouseStarted&&this._mouseUp(f));this._mouseDownEvent=f;var e=this,g=(f.which==1),d=(typeof this.options.cancel=="string"&&f.target.nodeName?b(f.target).closest(this.options.cancel).length:false);if(!g||d||!this._mouseCapture(f)){return true}this.mouseDelayMet=!this.options.delay;if(!this.mouseDelayMet){this._mouseDelayTimer=setTimeout(function(){e.mouseDelayMet=true},this.options.delay)}if(this._mouseDistanceMet(f)&&this._mouseDelayMet(f)){this._mouseStarted=(this._mouseStart(f)!==false);if(!this._mouseStarted){f.preventDefault();return true}}if(true===b.data(f.target,this.widgetName+".preventClickEvent")){b.removeData(f.target,this.widgetName+".preventClickEvent")}this._mouseMoveDelegate=function(h){return e._mouseMove(h)};this._mouseUpDelegate=function(h){return e._mouseUp(h)};b(document).bind("mousemove."+this.widgetName,this._mouseMoveDelegate).bind("mouseup."+this.widgetName,this._mouseUpDelegate);f.preventDefault();a=true;return true},_mouseMove:function(d){if(b.browser.msie&&!(document.documentMode>=9)&&!d.button){return this._mouseUp(d)}if(this._mouseStarted){this._mouseDrag(d);return d.preventDefault()}if(this._mouseDistanceMet(d)&&this._mouseDelayMet(d)){this._mouseStarted=(this._mouseStart(this._mouseDownEvent,d)!==false);(this._mouseStarted?this._mouseDrag(d):this._mouseUp(d))}return !this._mouseStarted},_mouseUp:function(d){b(document).unbind("mousemove."+this.widgetName,this._mouseMoveDelegate).unbind("mouseup."+this.widgetName,this._mouseUpDelegate);if(this._mouseStarted){this._mouseStarted=false;if(d.target==this._mouseDownEvent.target){b.data(d.target,this.widgetName+".preventClickEvent",true)}this._mouseStop(d)}return false},_mouseDistanceMet:function(d){return(Math.max(Math.abs(this._mouseDownEvent.pageX-d.pageX),Math.abs(this._mouseDownEvent.pageY-d.pageY))>=this.options.distance)},_mouseDelayMet:function(d){return this.mouseDelayMet},_mouseStart:function(d){},_mouseDrag:function(d){},_mouseStop:function(d){},_mouseCapture:function(d){return true}})})(jQuery);
/*
 * jQuery UI Position 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Position
 */
(function(g,h){g.ui=g.ui||{};var d=/left|center|right/,e=/top|center|bottom/,a="center",f={},b=g.fn.position,c=g.fn.offset;g.fn.position=function(j){if(!j||!j.of){return b.apply(this,arguments)}j=g.extend({},j);var n=g(j.of),m=n[0],p=(j.collision||"flip").split(" "),o=j.offset?j.offset.split(" "):[0,0],l,i,k;if(m.nodeType===9){l=n.width();i=n.height();k={top:0,left:0}}else{if(m.setTimeout){l=n.width();i=n.height();k={top:n.scrollTop(),left:n.scrollLeft()}}else{if(m.preventDefault){j.at="left top";l=i=0;k={top:j.of.pageY,left:j.of.pageX}}else{l=n.outerWidth();i=n.outerHeight();k=n.offset()}}}g.each(["my","at"],function(){var q=(j[this]||"").split(" ");if(q.length===1){q=d.test(q[0])?q.concat([a]):e.test(q[0])?[a].concat(q):[a,a]}q[0]=d.test(q[0])?q[0]:a;q[1]=e.test(q[1])?q[1]:a;j[this]=q});if(p.length===1){p[1]=p[0]}o[0]=parseInt(o[0],10)||0;if(o.length===1){o[1]=o[0]}o[1]=parseInt(o[1],10)||0;if(j.at[0]==="right"){k.left+=l}else{if(j.at[0]===a){k.left+=l/2}}if(j.at[1]==="bottom"){k.top+=i}else{if(j.at[1]===a){k.top+=i/2}}k.left+=o[0];k.top+=o[1];return this.each(function(){var t=g(this),v=t.outerWidth(),s=t.outerHeight(),u=parseInt(g.curCSS(this,"marginLeft",true))||0,r=parseInt(g.curCSS(this,"marginTop",true))||0,x=v+u+(parseInt(g.curCSS(this,"marginRight",true))||0),y=s+r+(parseInt(g.curCSS(this,"marginBottom",true))||0),w=g.extend({},k),q;if(j.my[0]==="right"){w.left-=v}else{if(j.my[0]===a){w.left-=v/2}}if(j.my[1]==="bottom"){w.top-=s}else{if(j.my[1]===a){w.top-=s/2}}if(!f.fractions){w.left=Math.round(w.left);w.top=Math.round(w.top)}q={left:w.left-u,top:w.top-r};g.each(["left","top"],function(A,z){if(g.ui.position[p[A]]){g.ui.position[p[A]][z](w,{targetWidth:l,targetHeight:i,elemWidth:v,elemHeight:s,collisionPosition:q,collisionWidth:x,collisionHeight:y,offset:o,my:j.my,at:j.at})}});if(g.fn.bgiframe){t.bgiframe()}t.offset(g.extend(w,{using:j.using}))})};g.ui.position={fit:{left:function(i,j){var l=g(window),k=j.collisionPosition.left+j.collisionWidth-l.width()-l.scrollLeft();i.left=k>0?i.left-k:Math.max(i.left-j.collisionPosition.left,i.left)},top:function(i,j){var l=g(window),k=j.collisionPosition.top+j.collisionHeight-l.height()-l.scrollTop();i.top=k>0?i.top-k:Math.max(i.top-j.collisionPosition.top,i.top)}},flip:{left:function(j,l){if(l.at[0]===a){return}var n=g(window),m=l.collisionPosition.left+l.collisionWidth-n.width()-n.scrollLeft(),i=l.my[0]==="left"?-l.elemWidth:l.my[0]==="right"?l.elemWidth:0,k=l.at[0]==="left"?l.targetWidth:-l.targetWidth,o=-2*l.offset[0];j.left+=l.collisionPosition.left<0?i+k+o:m>0?i+k+o:0},top:function(j,l){if(l.at[1]===a){return}var n=g(window),m=l.collisionPosition.top+l.collisionHeight-n.height()-n.scrollTop(),i=l.my[1]==="top"?-l.elemHeight:l.my[1]==="bottom"?l.elemHeight:0,k=l.at[1]==="top"?l.targetHeight:-l.targetHeight,o=-2*l.offset[1];j.top+=l.collisionPosition.top<0?i+k+o:m>0?i+k+o:0}}};if(!g.offset.setOffset){g.offset.setOffset=function(m,j){if(/static/.test(g.curCSS(m,"position"))){m.style.position="relative"}var l=g(m),o=l.offset(),i=parseInt(g.curCSS(m,"top",true),10)||0,n=parseInt(g.curCSS(m,"left",true),10)||0,k={top:(j.top-o.top)+i,left:(j.left-o.left)+n};if("using" in j){j.using.call(m,k)}else{l.css(k)}};g.fn.offset=function(i){var j=this[0];if(!j||!j.ownerDocument){return null}if(i){if(g.isFunction(i)){return this.each(function(k){g(this).offset(i.call(this,k,g(this).offset()))})}return this.each(function(){g.offset.setOffset(this,i)})}return c.call(this)}}if(!g.curCSS){g.curCSS=g.css}(function(){var j=document.getElementsByTagName("body")[0],q=document.createElement("div"),n,p,k,o,m;n=document.createElement(j?"div":"body");k={visibility:"hidden",width:0,height:0,border:0,margin:0,background:"none"};if(j){g.extend(k,{position:"absolute",left:"-1000px",top:"-1000px"})}for(var l in k){n.style[l]=k[l]}n.appendChild(q);p=j||document.documentElement;p.insertBefore(n,p.firstChild);q.style.cssText="position: absolute; left: 10.7432222px; top: 10.432325px; height: 30px; width: 201px;";o=g(q).offset(function(i,r){return r}).offset();n.innerHTML="";p.removeChild(n);m=o.top+o.left+(j?2000:0);f.fractions=m>21&&m<22})()}(jQuery));
/*
 * jQuery UI Draggable 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Draggables
 *
 * Depends:
 *	jquery.ui.core.js
 *	jquery.ui.mouse.js
 *	jquery.ui.widget.js
 */
(function(a,b){a.widget("ui.draggable",a.ui.mouse,{widgetEventPrefix:"drag",options:{addClasses:true,appendTo:"parent",axis:false,connectToSortable:false,containment:false,cursor:"auto",cursorAt:false,grid:false,handle:false,helper:"original",iframeFix:false,opacity:false,refreshPositions:false,revert:false,revertDuration:500,scope:"default",scroll:true,scrollSensitivity:20,scrollSpeed:20,snap:false,snapMode:"both",snapTolerance:20,stack:false,zIndex:false},_create:function(){if(this.options.helper=="original"&&!(/^(?:r|a|f)/).test(this.element.css("position"))){this.element[0].style.position="relative"}(this.options.addClasses&&this.element.addClass("ui-draggable"));(this.options.disabled&&this.element.addClass("ui-draggable-disabled"));this._mouseInit()},destroy:function(){if(!this.element.data("draggable")){return}this.element.removeData("draggable").unbind(".draggable").removeClass("ui-draggable ui-draggable-dragging ui-draggable-disabled");this._mouseDestroy();return this},_mouseCapture:function(c){var d=this.options;if(this.helper||d.disabled||a(c.target).is(".ui-resizable-handle")){return false}this.handle=this._getHandle(c);if(!this.handle){return false}if(d.iframeFix){a(d.iframeFix===true?"iframe":d.iframeFix).each(function(){a('<div class="ui-draggable-iframeFix" style="background: #fff;"></div>').css({width:this.offsetWidth+"px",height:this.offsetHeight+"px",position:"absolute",opacity:"0.001",zIndex:1000}).css(a(this).offset()).appendTo("body")})}return true},_mouseStart:function(c){var d=this.options;this.helper=this._createHelper(c);this.helper.addClass("ui-draggable-dragging");this._cacheHelperProportions();if(a.ui.ddmanager){a.ui.ddmanager.current=this}this._cacheMargins();this.cssPosition=this.helper.css("position");this.scrollParent=this.helper.scrollParent();this.offset=this.positionAbs=this.element.offset();this.offset={top:this.offset.top-this.margins.top,left:this.offset.left-this.margins.left};a.extend(this.offset,{click:{left:c.pageX-this.offset.left,top:c.pageY-this.offset.top},parent:this._getParentOffset(),relative:this._getRelativeOffset()});this.originalPosition=this.position=this._generatePosition(c);this.originalPageX=c.pageX;this.originalPageY=c.pageY;(d.cursorAt&&this._adjustOffsetFromHelper(d.cursorAt));if(d.containment){this._setContainment()}if(this._trigger("start",c)===false){this._clear();return false}this._cacheHelperProportions();if(a.ui.ddmanager&&!d.dropBehaviour){a.ui.ddmanager.prepareOffsets(this,c)}this._mouseDrag(c,true);if(a.ui.ddmanager){a.ui.ddmanager.dragStart(this,c)}return true},_mouseDrag:function(c,e){this.position=this._generatePosition(c);this.positionAbs=this._convertPositionTo("absolute");if(!e){var d=this._uiHash();if(this._trigger("drag",c,d)===false){this._mouseUp({});return false}this.position=d.position}if(!this.options.axis||this.options.axis!="y"){this.helper[0].style.left=this.position.left+"px"}if(!this.options.axis||this.options.axis!="x"){this.helper[0].style.top=this.position.top+"px"}if(a.ui.ddmanager){a.ui.ddmanager.drag(this,c)}return false},_mouseStop:function(e){var g=false;if(a.ui.ddmanager&&!this.options.dropBehaviour){g=a.ui.ddmanager.drop(this,e)}if(this.dropped){g=this.dropped;this.dropped=false}var d=this.element[0],f=false;while(d&&(d=d.parentNode)){if(d==document){f=true}}if(!f&&this.options.helper==="original"){return false}if((this.options.revert=="invalid"&&!g)||(this.options.revert=="valid"&&g)||this.options.revert===true||(a.isFunction(this.options.revert)&&this.options.revert.call(this.element,g))){var c=this;a(this.helper).animate(this.originalPosition,parseInt(this.options.revertDuration,10),function(){if(c._trigger("stop",e)!==false){c._clear()}})}else{if(this._trigger("stop",e)!==false){this._clear()}}return false},_mouseUp:function(c){if(this.options.iframeFix===true){a("div.ui-draggable-iframeFix").each(function(){this.parentNode.removeChild(this)})}if(a.ui.ddmanager){a.ui.ddmanager.dragStop(this,c)}return a.ui.mouse.prototype._mouseUp.call(this,c)},cancel:function(){if(this.helper.is(".ui-draggable-dragging")){this._mouseUp({})}else{this._clear()}return this},_getHandle:function(c){var d=!this.options.handle||!a(this.options.handle,this.element).length?true:false;a(this.options.handle,this.element).find("*").andSelf().each(function(){if(this==c.target){d=true}});return d},_createHelper:function(d){var e=this.options;var c=a.isFunction(e.helper)?a(e.helper.apply(this.element[0],[d])):(e.helper=="clone"?this.element.clone().removeAttr("id"):this.element);if(!c.parents("body").length){c.appendTo((e.appendTo=="parent"?this.element[0].parentNode:e.appendTo))}if(c[0]!=this.element[0]&&!(/(fixed|absolute)/).test(c.css("position"))){c.css("position","absolute")}return c},_adjustOffsetFromHelper:function(c){if(typeof c=="string"){c=c.split(" ")}if(a.isArray(c)){c={left:+c[0],top:+c[1]||0}}if("left" in c){this.offset.click.left=c.left+this.margins.left}if("right" in c){this.offset.click.left=this.helperProportions.width-c.right+this.margins.left}if("top" in c){this.offset.click.top=c.top+this.margins.top}if("bottom" in c){this.offset.click.top=this.helperProportions.height-c.bottom+this.margins.top}},_getParentOffset:function(){this.offsetParent=this.helper.offsetParent();var c=this.offsetParent.offset();if(this.cssPosition=="absolute"&&this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0])){c.left+=this.scrollParent.scrollLeft();c.top+=this.scrollParent.scrollTop()}if((this.offsetParent[0]==document.body)||(this.offsetParent[0].tagName&&this.offsetParent[0].tagName.toLowerCase()=="html"&&a.browser.msie)){c={top:0,left:0}}return{top:c.top+(parseInt(this.offsetParent.css("borderTopWidth"),10)||0),left:c.left+(parseInt(this.offsetParent.css("borderLeftWidth"),10)||0)}},_getRelativeOffset:function(){if(this.cssPosition=="relative"){var c=this.element.position();return{top:c.top-(parseInt(this.helper.css("top"),10)||0)+this.scrollParent.scrollTop(),left:c.left-(parseInt(this.helper.css("left"),10)||0)+this.scrollParent.scrollLeft()}}else{return{top:0,left:0}}},_cacheMargins:function(){this.margins={left:(parseInt(this.element.css("marginLeft"),10)||0),top:(parseInt(this.element.css("marginTop"),10)||0),right:(parseInt(this.element.css("marginRight"),10)||0),bottom:(parseInt(this.element.css("marginBottom"),10)||0)}},_cacheHelperProportions:function(){this.helperProportions={width:this.helper.outerWidth(),height:this.helper.outerHeight()}},_setContainment:function(){var g=this.options;if(g.containment=="parent"){g.containment=this.helper[0].parentNode}if(g.containment=="document"||g.containment=="window"){this.containment=[g.containment=="document"?0:a(window).scrollLeft()-this.offset.relative.left-this.offset.parent.left,g.containment=="document"?0:a(window).scrollTop()-this.offset.relative.top-this.offset.parent.top,(g.containment=="document"?0:a(window).scrollLeft())+a(g.containment=="document"?document:window).width()-this.helperProportions.width-this.margins.left,(g.containment=="document"?0:a(window).scrollTop())+(a(g.containment=="document"?document:window).height()||document.body.parentNode.scrollHeight)-this.helperProportions.height-this.margins.top]}if(!(/^(document|window|parent)$/).test(g.containment)&&g.containment.constructor!=Array){var h=a(g.containment);var e=h[0];if(!e){return}var f=h.offset();var d=(a(e).css("overflow")!="hidden");this.containment=[(parseInt(a(e).css("borderLeftWidth"),10)||0)+(parseInt(a(e).css("paddingLeft"),10)||0),(parseInt(a(e).css("borderTopWidth"),10)||0)+(parseInt(a(e).css("paddingTop"),10)||0),(d?Math.max(e.scrollWidth,e.offsetWidth):e.offsetWidth)-(parseInt(a(e).css("borderLeftWidth"),10)||0)-(parseInt(a(e).css("paddingRight"),10)||0)-this.helperProportions.width-this.margins.left-this.margins.right,(d?Math.max(e.scrollHeight,e.offsetHeight):e.offsetHeight)-(parseInt(a(e).css("borderTopWidth"),10)||0)-(parseInt(a(e).css("paddingBottom"),10)||0)-this.helperProportions.height-this.margins.top-this.margins.bottom];this.relative_container=h}else{if(g.containment.constructor==Array){this.containment=g.containment}}},_convertPositionTo:function(g,i){if(!i){i=this.position}var e=g=="absolute"?1:-1;var f=this.options,c=this.cssPosition=="absolute"&&!(this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,h=(/(html|body)/i).test(c[0].tagName);return{top:(i.top+this.offset.relative.top*e+this.offset.parent.top*e-(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollTop():(h?0:c.scrollTop()))*e)),left:(i.left+this.offset.relative.left*e+this.offset.parent.left*e-(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():h?0:c.scrollLeft())*e))}},_generatePosition:function(d){var e=this.options,l=this.cssPosition=="absolute"&&!(this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,i=(/(html|body)/i).test(l[0].tagName);var h=d.pageX;var g=d.pageY;if(this.originalPosition){var c;if(this.containment){if(this.relative_container){var k=this.relative_container.offset();c=[this.containment[0]+k.left,this.containment[1]+k.top,this.containment[2]+k.left,this.containment[3]+k.top]}else{c=this.containment}if(d.pageX-this.offset.click.left<c[0]){h=c[0]+this.offset.click.left}if(d.pageY-this.offset.click.top<c[1]){g=c[1]+this.offset.click.top}if(d.pageX-this.offset.click.left>c[2]){h=c[2]+this.offset.click.left}if(d.pageY-this.offset.click.top>c[3]){g=c[3]+this.offset.click.top}}if(e.grid){var j=e.grid[1]?this.originalPageY+Math.round((g-this.originalPageY)/e.grid[1])*e.grid[1]:this.originalPageY;g=c?(!(j-this.offset.click.top<c[1]||j-this.offset.click.top>c[3])?j:(!(j-this.offset.click.top<c[1])?j-e.grid[1]:j+e.grid[1])):j;var f=e.grid[0]?this.originalPageX+Math.round((h-this.originalPageX)/e.grid[0])*e.grid[0]:this.originalPageX;h=c?(!(f-this.offset.click.left<c[0]||f-this.offset.click.left>c[2])?f:(!(f-this.offset.click.left<c[0])?f-e.grid[0]:f+e.grid[0])):f}}return{top:(g-this.offset.click.top-this.offset.relative.top-this.offset.parent.top+(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollTop():(i?0:l.scrollTop())))),left:(h-this.offset.click.left-this.offset.relative.left-this.offset.parent.left+(a.browser.safari&&a.browser.version<526&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():i?0:l.scrollLeft())))}},_clear:function(){this.helper.removeClass("ui-draggable-dragging");if(this.helper[0]!=this.element[0]&&!this.cancelHelperRemoval){this.helper.remove()}this.helper=null;this.cancelHelperRemoval=false},_trigger:function(c,d,e){e=e||this._uiHash();a.ui.plugin.call(this,c,[d,e]);if(c=="drag"){this.positionAbs=this._convertPositionTo("absolute")}return a.Widget.prototype._trigger.call(this,c,d,e)},plugins:{},_uiHash:function(c){return{helper:this.helper,position:this.position,originalPosition:this.originalPosition,offset:this.positionAbs}}});a.extend(a.ui.draggable,{version:"1.8.23"});a.ui.plugin.add("draggable","connectToSortable",{start:function(d,f){var e=a(this).data("draggable"),g=e.options,c=a.extend({},f,{item:e.element});e.sortables=[];a(g.connectToSortable).each(function(){var h=a.data(this,"sortable");if(h&&!h.options.disabled){e.sortables.push({instance:h,shouldRevert:h.options.revert});h.refreshPositions();h._trigger("activate",d,c)}})},stop:function(d,f){var e=a(this).data("draggable"),c=a.extend({},f,{item:e.element});a.each(e.sortables,function(){if(this.instance.isOver){this.instance.isOver=0;e.cancelHelperRemoval=true;this.instance.cancelHelperRemoval=false;if(this.shouldRevert){this.instance.options.revert=true}this.instance._mouseStop(d);this.instance.options.helper=this.instance.options._helper;if(e.options.helper=="original"){this.instance.currentItem.css({top:"auto",left:"auto"})}}else{this.instance.cancelHelperRemoval=false;this.instance._trigger("deactivate",d,c)}})},drag:function(d,g){var f=a(this).data("draggable"),c=this;var e=function(j){var p=this.offset.click.top,n=this.offset.click.left;var h=this.positionAbs.top,l=this.positionAbs.left;var k=j.height,m=j.width;var q=j.top,i=j.left;return a.ui.isOver(h+p,l+n,q,i,k,m)};a.each(f.sortables,function(h){this.instance.positionAbs=f.positionAbs;this.instance.helperProportions=f.helperProportions;this.instance.offset.click=f.offset.click;if(this.instance._intersectsWith(this.instance.containerCache)){if(!this.instance.isOver){this.instance.isOver=1;this.instance.currentItem=a(c).clone().removeAttr("id").appendTo(this.instance.element).data("sortable-item",true);this.instance.options._helper=this.instance.options.helper;this.instance.options.helper=function(){return g.helper[0]};d.target=this.instance.currentItem[0];this.instance._mouseCapture(d,true);this.instance._mouseStart(d,true,true);this.instance.offset.click.top=f.offset.click.top;this.instance.offset.click.left=f.offset.click.left;this.instance.offset.parent.left-=f.offset.parent.left-this.instance.offset.parent.left;this.instance.offset.parent.top-=f.offset.parent.top-this.instance.offset.parent.top;f._trigger("toSortable",d);f.dropped=this.instance.element;f.currentItem=f.element;this.instance.fromOutside=f}if(this.instance.currentItem){this.instance._mouseDrag(d)}}else{if(this.instance.isOver){this.instance.isOver=0;this.instance.cancelHelperRemoval=true;this.instance.options.revert=false;this.instance._trigger("out",d,this.instance._uiHash(this.instance));this.instance._mouseStop(d,true);this.instance.options.helper=this.instance.options._helper;this.instance.currentItem.remove();if(this.instance.placeholder){this.instance.placeholder.remove()}f._trigger("fromSortable",d);f.dropped=false}}})}});a.ui.plugin.add("draggable","cursor",{start:function(d,e){var c=a("body"),f=a(this).data("draggable").options;if(c.css("cursor")){f._cursor=c.css("cursor")}c.css("cursor",f.cursor)},stop:function(c,d){var e=a(this).data("draggable").options;if(e._cursor){a("body").css("cursor",e._cursor)}}});a.ui.plugin.add("draggable","opacity",{start:function(d,e){var c=a(e.helper),f=a(this).data("draggable").options;if(c.css("opacity")){f._opacity=c.css("opacity")}c.css("opacity",f.opacity)},stop:function(c,d){var e=a(this).data("draggable").options;if(e._opacity){a(d.helper).css("opacity",e._opacity)}}});a.ui.plugin.add("draggable","scroll",{start:function(d,e){var c=a(this).data("draggable");if(c.scrollParent[0]!=document&&c.scrollParent[0].tagName!="HTML"){c.overflowOffset=c.scrollParent.offset()}},drag:function(e,f){var d=a(this).data("draggable"),g=d.options,c=false;if(d.scrollParent[0]!=document&&d.scrollParent[0].tagName!="HTML"){if(!g.axis||g.axis!="x"){if((d.overflowOffset.top+d.scrollParent[0].offsetHeight)-e.pageY<g.scrollSensitivity){d.scrollParent[0].scrollTop=c=d.scrollParent[0].scrollTop+g.scrollSpeed}else{if(e.pageY-d.overflowOffset.top<g.scrollSensitivity){d.scrollParent[0].scrollTop=c=d.scrollParent[0].scrollTop-g.scrollSpeed}}}if(!g.axis||g.axis!="y"){if((d.overflowOffset.left+d.scrollParent[0].offsetWidth)-e.pageX<g.scrollSensitivity){d.scrollParent[0].scrollLeft=c=d.scrollParent[0].scrollLeft+g.scrollSpeed}else{if(e.pageX-d.overflowOffset.left<g.scrollSensitivity){d.scrollParent[0].scrollLeft=c=d.scrollParent[0].scrollLeft-g.scrollSpeed}}}}else{if(!g.axis||g.axis!="x"){if(e.pageY-a(document).scrollTop()<g.scrollSensitivity){c=a(document).scrollTop(a(document).scrollTop()-g.scrollSpeed)}else{if(a(window).height()-(e.pageY-a(document).scrollTop())<g.scrollSensitivity){c=a(document).scrollTop(a(document).scrollTop()+g.scrollSpeed)}}}if(!g.axis||g.axis!="y"){if(e.pageX-a(document).scrollLeft()<g.scrollSensitivity){c=a(document).scrollLeft(a(document).scrollLeft()-g.scrollSpeed)}else{if(a(window).width()-(e.pageX-a(document).scrollLeft())<g.scrollSensitivity){c=a(document).scrollLeft(a(document).scrollLeft()+g.scrollSpeed)}}}}if(c!==false&&a.ui.ddmanager&&!g.dropBehaviour){a.ui.ddmanager.prepareOffsets(d,e)}}});a.ui.plugin.add("draggable","snap",{start:function(d,e){var c=a(this).data("draggable"),f=c.options;c.snapElements=[];a(f.snap.constructor!=String?(f.snap.items||":data(draggable)"):f.snap).each(function(){var h=a(this);var g=h.offset();if(this!=c.element[0]){c.snapElements.push({item:this,width:h.outerWidth(),height:h.outerHeight(),top:g.top,left:g.left})}})},drag:function(u,p){var g=a(this).data("draggable"),q=g.options;var y=q.snapTolerance;var x=p.offset.left,w=x+g.helperProportions.width,f=p.offset.top,e=f+g.helperProportions.height;for(var v=g.snapElements.length-1;v>=0;v--){var s=g.snapElements[v].left,n=s+g.snapElements[v].width,m=g.snapElements[v].top,A=m+g.snapElements[v].height;if(!((s-y<x&&x<n+y&&m-y<f&&f<A+y)||(s-y<x&&x<n+y&&m-y<e&&e<A+y)||(s-y<w&&w<n+y&&m-y<f&&f<A+y)||(s-y<w&&w<n+y&&m-y<e&&e<A+y))){if(g.snapElements[v].snapping){(g.options.snap.release&&g.options.snap.release.call(g.element,u,a.extend(g._uiHash(),{snapItem:g.snapElements[v].item})))}g.snapElements[v].snapping=false;continue}if(q.snapMode!="inner"){var c=Math.abs(m-e)<=y;var z=Math.abs(A-f)<=y;var j=Math.abs(s-w)<=y;var k=Math.abs(n-x)<=y;if(c){p.position.top=g._convertPositionTo("relative",{top:m-g.helperProportions.height,left:0}).top-g.margins.top}if(z){p.position.top=g._convertPositionTo("relative",{top:A,left:0}).top-g.margins.top}if(j){p.position.left=g._convertPositionTo("relative",{top:0,left:s-g.helperProportions.width}).left-g.margins.left}if(k){p.position.left=g._convertPositionTo("relative",{top:0,left:n}).left-g.margins.left}}var h=(c||z||j||k);if(q.snapMode!="outer"){var c=Math.abs(m-f)<=y;var z=Math.abs(A-e)<=y;var j=Math.abs(s-x)<=y;var k=Math.abs(n-w)<=y;if(c){p.position.top=g._convertPositionTo("relative",{top:m,left:0}).top-g.margins.top}if(z){p.position.top=g._convertPositionTo("relative",{top:A-g.helperProportions.height,left:0}).top-g.margins.top}if(j){p.position.left=g._convertPositionTo("relative",{top:0,left:s}).left-g.margins.left}if(k){p.position.left=g._convertPositionTo("relative",{top:0,left:n-g.helperProportions.width}).left-g.margins.left}}if(!g.snapElements[v].snapping&&(c||z||j||k||h)){(g.options.snap.snap&&g.options.snap.snap.call(g.element,u,a.extend(g._uiHash(),{snapItem:g.snapElements[v].item})))}g.snapElements[v].snapping=(c||z||j||k||h)}}});a.ui.plugin.add("draggable","stack",{start:function(d,e){var g=a(this).data("draggable").options;var f=a.makeArray(a(g.stack)).sort(function(i,h){return(parseInt(a(i).css("zIndex"),10)||0)-(parseInt(a(h).css("zIndex"),10)||0)});if(!f.length){return}var c=parseInt(f[0].style.zIndex)||0;a(f).each(function(h){this.style.zIndex=c+h});this[0].style.zIndex=c+f.length}});a.ui.plugin.add("draggable","zIndex",{start:function(d,e){var c=a(e.helper),f=a(this).data("draggable").options;if(c.css("zIndex")){f._zIndex=c.css("zIndex")}c.css("zIndex",f.zIndex)},stop:function(c,d){var e=a(this).data("draggable").options;if(e._zIndex){a(d.helper).css("zIndex",e._zIndex)}}})})(jQuery);
/*
 * jQuery UI Droppable 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Droppables
 *
 * Depends:
 *	jquery.ui.core.js
 *	jquery.ui.widget.js
 *	jquery.ui.mouse.js
 *	jquery.ui.draggable.js
 */
(function(a,b){a.widget("ui.droppable",{widgetEventPrefix:"drop",options:{accept:"*",activeClass:false,addClasses:true,greedy:false,hoverClass:false,scope:"default",tolerance:"intersect"},_create:function(){var d=this.options,c=d.accept;this.isover=0;this.isout=1;this.accept=a.isFunction(c)?c:function(e){return e.is(c)};this.proportions={width:this.element[0].offsetWidth,height:this.element[0].offsetHeight};a.ui.ddmanager.droppables[d.scope]=a.ui.ddmanager.droppables[d.scope]||[];a.ui.ddmanager.droppables[d.scope].push(this);(d.addClasses&&this.element.addClass("ui-droppable"))},destroy:function(){var c=a.ui.ddmanager.droppables[this.options.scope];for(var d=0;d<c.length;d++){if(c[d]==this){c.splice(d,1)}}this.element.removeClass("ui-droppable ui-droppable-disabled").removeData("droppable").unbind(".droppable");return this},_setOption:function(c,d){if(c=="accept"){this.accept=a.isFunction(d)?d:function(e){return e.is(d)}}a.Widget.prototype._setOption.apply(this,arguments)},_activate:function(d){var c=a.ui.ddmanager.current;if(this.options.activeClass){this.element.addClass(this.options.activeClass)}(c&&this._trigger("activate",d,this.ui(c)))},_deactivate:function(d){var c=a.ui.ddmanager.current;if(this.options.activeClass){this.element.removeClass(this.options.activeClass)}(c&&this._trigger("deactivate",d,this.ui(c)))},_over:function(d){var c=a.ui.ddmanager.current;if(!c||(c.currentItem||c.element)[0]==this.element[0]){return}if(this.accept.call(this.element[0],(c.currentItem||c.element))){if(this.options.hoverClass){this.element.addClass(this.options.hoverClass)}this._trigger("over",d,this.ui(c))}},_out:function(d){var c=a.ui.ddmanager.current;if(!c||(c.currentItem||c.element)[0]==this.element[0]){return}if(this.accept.call(this.element[0],(c.currentItem||c.element))){if(this.options.hoverClass){this.element.removeClass(this.options.hoverClass)}this._trigger("out",d,this.ui(c))}},_drop:function(d,e){var c=e||a.ui.ddmanager.current;if(!c||(c.currentItem||c.element)[0]==this.element[0]){return false}var f=false;this.element.find(":data(droppable)").not(".ui-draggable-dragging").each(function(){var g=a.data(this,"droppable");if(g.options.greedy&&!g.options.disabled&&g.options.scope==c.options.scope&&g.accept.call(g.element[0],(c.currentItem||c.element))&&a.ui.intersect(c,a.extend(g,{offset:g.element.offset()}),g.options.tolerance)){f=true;return false}});if(f){return false}if(this.accept.call(this.element[0],(c.currentItem||c.element))){if(this.options.activeClass){this.element.removeClass(this.options.activeClass)}if(this.options.hoverClass){this.element.removeClass(this.options.hoverClass)}this._trigger("drop",d,this.ui(c));return this.element}return false},ui:function(d){return{draggable:(d.currentItem||d.element),helper:d.helper,position:d.position,offset:d.positionAbs}}});a.extend(a.ui.droppable,{version:"1.8.23"});a.ui.intersect=function(q,j,o){if(!j.offset){return false}var e=(q.positionAbs||q.position.absolute).left,d=e+q.helperProportions.width,n=(q.positionAbs||q.position.absolute).top,m=n+q.helperProportions.height;var g=j.offset.left,c=g+j.proportions.width,p=j.offset.top,k=p+j.proportions.height;switch(o){case"fit":return(g<=e&&d<=c&&p<=n&&m<=k);break;case"intersect":return(g<e+(q.helperProportions.width/2)&&d-(q.helperProportions.width/2)<c&&p<n+(q.helperProportions.height/2)&&m-(q.helperProportions.height/2)<k);break;case"pointer":var h=((q.positionAbs||q.position.absolute).left+(q.clickOffset||q.offset.click).left),i=((q.positionAbs||q.position.absolute).top+(q.clickOffset||q.offset.click).top),f=a.ui.isOver(i,h,p,g,j.proportions.height,j.proportions.width);return f;break;case"touch":return((n>=p&&n<=k)||(m>=p&&m<=k)||(n<p&&m>k))&&((e>=g&&e<=c)||(d>=g&&d<=c)||(e<g&&d>c));break;default:return false;break}};a.ui.ddmanager={current:null,droppables:{"default":[]},prepareOffsets:function(f,h){var c=a.ui.ddmanager.droppables[f.options.scope]||[];var g=h?h.type:null;var k=(f.currentItem||f.element).find(":data(droppable)").andSelf();droppablesLoop:for(var e=0;e<c.length;e++){if(c[e].options.disabled||(f&&!c[e].accept.call(c[e].element[0],(f.currentItem||f.element)))){continue}for(var d=0;d<k.length;d++){if(k[d]==c[e].element[0]){c[e].proportions.height=0;continue droppablesLoop}}c[e].visible=c[e].element.css("display")!="none";if(!c[e].visible){continue}if(g=="mousedown"){c[e]._activate.call(c[e],h)}c[e].offset=c[e].element.offset();c[e].proportions={width:c[e].element[0].offsetWidth,height:c[e].element[0].offsetHeight}}},drop:function(c,d){var e=false;a.each(a.ui.ddmanager.droppables[c.options.scope]||[],function(){if(!this.options){return}if(!this.options.disabled&&this.visible&&a.ui.intersect(c,this,this.options.tolerance)){e=this._drop.call(this,d)||e}if(!this.options.disabled&&this.visible&&this.accept.call(this.element[0],(c.currentItem||c.element))){this.isout=1;this.isover=0;this._deactivate.call(this,d)}});return e},dragStart:function(c,d){c.element.parents(":not(body,html)").bind("scroll.droppable",function(){if(!c.options.refreshPositions){a.ui.ddmanager.prepareOffsets(c,d)}})},drag:function(c,d){if(c.options.refreshPositions){a.ui.ddmanager.prepareOffsets(c,d)}a.each(a.ui.ddmanager.droppables[c.options.scope]||[],function(){if(this.options.disabled||this.greedyChild||!this.visible){return}var f=a.ui.intersect(c,this,this.options.tolerance);var h=!f&&this.isover==1?"isout":(f&&this.isover==0?"isover":null);if(!h){return}var g;if(this.options.greedy){var e=this.element.parents(":data(droppable):eq(0)");if(e.length){g=a.data(e[0],"droppable");g.greedyChild=(h=="isover"?1:0)}}if(g&&h=="isover"){g.isover=0;g.isout=1;g._out.call(g,d)}this[h]=1;this[h=="isout"?"isover":"isout"]=0;this[h=="isover"?"_over":"_out"].call(this,d);if(g&&h=="isout"){g.isout=0;g.isover=1;g._over.call(g,d)}})},dragStop:function(c,d){c.element.parents(":not(body,html)").unbind("scroll.droppable");if(!c.options.refreshPositions){a.ui.ddmanager.prepareOffsets(c,d)}}}})(jQuery);
/*
 * jQuery UI Resizable 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Resizables
 *
 * Depends:
 *	jquery.ui.core.js
 *	jquery.ui.mouse.js
 *	jquery.ui.widget.js
 */
(function(c,d){c.widget("ui.resizable",c.ui.mouse,{widgetEventPrefix:"resize",options:{alsoResize:false,animate:false,animateDuration:"slow",animateEasing:"swing",aspectRatio:false,autoHide:false,containment:false,ghost:false,grid:false,handles:"e,s,se",helper:false,maxHeight:null,maxWidth:null,minHeight:10,minWidth:10,zIndex:1000},_create:function(){var f=this,k=this.options;this.element.addClass("ui-resizable");c.extend(this,{_aspectRatio:!!(k.aspectRatio),aspectRatio:k.aspectRatio,originalElement:this.element,_proportionallyResizeElements:[],_helper:k.helper||k.ghost||k.animate?k.helper||"ui-resizable-helper":null});if(this.element[0].nodeName.match(/canvas|textarea|input|select|button|img/i)){this.element.wrap(c('<div class="ui-wrapper" style="overflow: hidden;"></div>').css({position:this.element.css("position"),width:this.element.outerWidth(),height:this.element.outerHeight(),top:this.element.css("top"),left:this.element.css("left")}));this.element=this.element.parent().data("resizable",this.element.data("resizable"));this.elementIsWrapper=true;this.element.css({marginLeft:this.originalElement.css("marginLeft"),marginTop:this.originalElement.css("marginTop"),marginRight:this.originalElement.css("marginRight"),marginBottom:this.originalElement.css("marginBottom")});this.originalElement.css({marginLeft:0,marginTop:0,marginRight:0,marginBottom:0});this.originalResizeStyle=this.originalElement.css("resize");this.originalElement.css("resize","none");this._proportionallyResizeElements.push(this.originalElement.css({position:"static",zoom:1,display:"block"}));this.originalElement.css({margin:this.originalElement.css("margin")});this._proportionallyResize()}this.handles=k.handles||(!c(".ui-resizable-handle",this.element).length?"e,s,se":{n:".ui-resizable-n",e:".ui-resizable-e",s:".ui-resizable-s",w:".ui-resizable-w",se:".ui-resizable-se",sw:".ui-resizable-sw",ne:".ui-resizable-ne",nw:".ui-resizable-nw"});if(this.handles.constructor==String){if(this.handles=="all"){this.handles="n,e,s,w,se,sw,ne,nw"}var l=this.handles.split(",");this.handles={};for(var g=0;g<l.length;g++){var j=c.trim(l[g]),e="ui-resizable-"+j;var h=c('<div class="ui-resizable-handle '+e+'"></div>');h.css({zIndex:k.zIndex});if("se"==j){h.addClass("ui-icon ui-icon-gripsmall-diagonal-se")}this.handles[j]=".ui-resizable-"+j;this.element.append(h)}}this._renderAxis=function(q){q=q||this.element;for(var n in this.handles){if(this.handles[n].constructor==String){this.handles[n]=c(this.handles[n],this.element).show()}if(this.elementIsWrapper&&this.originalElement[0].nodeName.match(/textarea|input|select|button/i)){var o=c(this.handles[n],this.element),p=0;p=/sw|ne|nw|se|n|s/.test(n)?o.outerHeight():o.outerWidth();var m=["padding",/ne|nw|n/.test(n)?"Top":/se|sw|s/.test(n)?"Bottom":/^e$/.test(n)?"Right":"Left"].join("");q.css(m,p);this._proportionallyResize()}if(!c(this.handles[n]).length){continue}}};this._renderAxis(this.element);this._handles=c(".ui-resizable-handle",this.element).disableSelection();this._handles.mouseover(function(){if(!f.resizing){if(this.className){var i=this.className.match(/ui-resizable-(se|sw|ne|nw|n|e|s|w)/i)}f.axis=i&&i[1]?i[1]:"se"}});if(k.autoHide){this._handles.hide();c(this.element).addClass("ui-resizable-autohide").hover(function(){if(k.disabled){return}c(this).removeClass("ui-resizable-autohide");f._handles.show()},function(){if(k.disabled){return}if(!f.resizing){c(this).addClass("ui-resizable-autohide");f._handles.hide()}})}this._mouseInit()},destroy:function(){this._mouseDestroy();var e=function(g){c(g).removeClass("ui-resizable ui-resizable-disabled ui-resizable-resizing").removeData("resizable").unbind(".resizable").find(".ui-resizable-handle").remove()};if(this.elementIsWrapper){e(this.element);var f=this.element;f.after(this.originalElement.css({position:f.css("position"),width:f.outerWidth(),height:f.outerHeight(),top:f.css("top"),left:f.css("left")})).remove()}this.originalElement.css("resize",this.originalResizeStyle);e(this.originalElement);return this},_mouseCapture:function(f){var g=false;for(var e in this.handles){if(c(this.handles[e])[0]==f.target){g=true}}return !this.options.disabled&&g},_mouseStart:function(g){var j=this.options,f=this.element.position(),e=this.element;this.resizing=true;this.documentScroll={top:c(document).scrollTop(),left:c(document).scrollLeft()};if(e.is(".ui-draggable")||(/absolute/).test(e.css("position"))){e.css({position:"absolute",top:f.top,left:f.left})}this._renderProxy();var k=b(this.helper.css("left")),h=b(this.helper.css("top"));if(j.containment){k+=c(j.containment).scrollLeft()||0;h+=c(j.containment).scrollTop()||0}this.offset=this.helper.offset();this.position={left:k,top:h};this.size=this._helper?{width:e.outerWidth(),height:e.outerHeight()}:{width:e.width(),height:e.height()};this.originalSize=this._helper?{width:e.outerWidth(),height:e.outerHeight()}:{width:e.width(),height:e.height()};this.originalPosition={left:k,top:h};this.sizeDiff={width:e.outerWidth()-e.width(),height:e.outerHeight()-e.height()};this.originalMousePosition={left:g.pageX,top:g.pageY};this.aspectRatio=(typeof j.aspectRatio=="number")?j.aspectRatio:((this.originalSize.width/this.originalSize.height)||1);var i=c(".ui-resizable-"+this.axis).css("cursor");c("body").css("cursor",i=="auto"?this.axis+"-resize":i);e.addClass("ui-resizable-resizing");this._propagate("start",g);return true},_mouseDrag:function(e){var h=this.helper,g=this.options,m={},q=this,j=this.originalMousePosition,n=this.axis;var r=(e.pageX-j.left)||0,p=(e.pageY-j.top)||0;var i=this._change[n];if(!i){return false}var l=i.apply(this,[e,r,p]),k=c.browser.msie&&c.browser.version<7,f=this.sizeDiff;this._updateVirtualBoundaries(e.shiftKey);if(this._aspectRatio||e.shiftKey){l=this._updateRatio(l,e)}l=this._respectSize(l,e);this._propagate("resize",e);h.css({top:this.position.top+"px",left:this.position.left+"px",width:this.size.width+"px",height:this.size.height+"px"});if(!this._helper&&this._proportionallyResizeElements.length){this._proportionallyResize()}this._updateCache(l);this._trigger("resize",e,this.ui());return false},_mouseStop:function(h){this.resizing=false;var i=this.options,m=this;if(this._helper){var g=this._proportionallyResizeElements,e=g.length&&(/textarea/i).test(g[0].nodeName),f=e&&c.ui.hasScroll(g[0],"left")?0:m.sizeDiff.height,k=e?0:m.sizeDiff.width;var n={width:(m.helper.width()-k),height:(m.helper.height()-f)},j=(parseInt(m.element.css("left"),10)+(m.position.left-m.originalPosition.left))||null,l=(parseInt(m.element.css("top"),10)+(m.position.top-m.originalPosition.top))||null;if(!i.animate){this.element.css(c.extend(n,{top:l,left:j}))}m.helper.height(m.size.height);m.helper.width(m.size.width);if(this._helper&&!i.animate){this._proportionallyResize()}}c("body").css("cursor","auto");this.element.removeClass("ui-resizable-resizing");this._propagate("stop",h);if(this._helper){this.helper.remove()}return false},_updateVirtualBoundaries:function(g){var j=this.options,i,h,f,k,e;e={minWidth:a(j.minWidth)?j.minWidth:0,maxWidth:a(j.maxWidth)?j.maxWidth:Infinity,minHeight:a(j.minHeight)?j.minHeight:0,maxHeight:a(j.maxHeight)?j.maxHeight:Infinity};if(this._aspectRatio||g){i=e.minHeight*this.aspectRatio;f=e.minWidth/this.aspectRatio;h=e.maxHeight*this.aspectRatio;k=e.maxWidth/this.aspectRatio;if(i>e.minWidth){e.minWidth=i}if(f>e.minHeight){e.minHeight=f}if(h<e.maxWidth){e.maxWidth=h}if(k<e.maxHeight){e.maxHeight=k}}this._vBoundaries=e},_updateCache:function(e){var f=this.options;this.offset=this.helper.offset();if(a(e.left)){this.position.left=e.left}if(a(e.top)){this.position.top=e.top}if(a(e.height)){this.size.height=e.height}if(a(e.width)){this.size.width=e.width}},_updateRatio:function(h,g){var i=this.options,j=this.position,f=this.size,e=this.axis;if(a(h.height)){h.width=(h.height*this.aspectRatio)}else{if(a(h.width)){h.height=(h.width/this.aspectRatio)}}if(e=="sw"){h.left=j.left+(f.width-h.width);h.top=null}if(e=="nw"){h.top=j.top+(f.height-h.height);h.left=j.left+(f.width-h.width)}return h},_respectSize:function(l,g){var j=this.helper,i=this._vBoundaries,r=this._aspectRatio||g.shiftKey,q=this.axis,t=a(l.width)&&i.maxWidth&&(i.maxWidth<l.width),m=a(l.height)&&i.maxHeight&&(i.maxHeight<l.height),h=a(l.width)&&i.minWidth&&(i.minWidth>l.width),s=a(l.height)&&i.minHeight&&(i.minHeight>l.height);if(h){l.width=i.minWidth}if(s){l.height=i.minHeight}if(t){l.width=i.maxWidth}if(m){l.height=i.maxHeight}var f=this.originalPosition.left+this.originalSize.width,p=this.position.top+this.size.height;var k=/sw|nw|w/.test(q),e=/nw|ne|n/.test(q);if(h&&k){l.left=f-i.minWidth}if(t&&k){l.left=f-i.maxWidth}if(s&&e){l.top=p-i.minHeight}if(m&&e){l.top=p-i.maxHeight}var n=!l.width&&!l.height;if(n&&!l.left&&l.top){l.top=null}else{if(n&&!l.top&&l.left){l.left=null}}return l},_proportionallyResize:function(){var k=this.options;if(!this._proportionallyResizeElements.length){return}var g=this.helper||this.element;for(var f=0;f<this._proportionallyResizeElements.length;f++){var h=this._proportionallyResizeElements[f];if(!this.borderDif){var e=[h.css("borderTopWidth"),h.css("borderRightWidth"),h.css("borderBottomWidth"),h.css("borderLeftWidth")],j=[h.css("paddingTop"),h.css("paddingRight"),h.css("paddingBottom"),h.css("paddingLeft")];this.borderDif=c.map(e,function(l,n){var m=parseInt(l,10)||0,o=parseInt(j[n],10)||0;return m+o})}if(c.browser.msie&&!(!(c(g).is(":hidden")||c(g).parents(":hidden").length))){continue}h.css({height:(g.height()-this.borderDif[0]-this.borderDif[2])||0,width:(g.width()-this.borderDif[1]-this.borderDif[3])||0})}},_renderProxy:function(){var f=this.element,i=this.options;this.elementOffset=f.offset();if(this._helper){this.helper=this.helper||c('<div style="overflow:hidden;"></div>');var e=c.browser.msie&&c.browser.version<7,g=(e?1:0),h=(e?2:-1);this.helper.addClass(this._helper).css({width:this.element.outerWidth()+h,height:this.element.outerHeight()+h,position:"absolute",left:this.elementOffset.left-g+"px",top:this.elementOffset.top-g+"px",zIndex:++i.zIndex});this.helper.appendTo("body").disableSelection()}else{this.helper=this.element}},_change:{e:function(g,f,e){return{width:this.originalSize.width+f}},w:function(h,f,e){var j=this.options,g=this.originalSize,i=this.originalPosition;return{left:i.left+f,width:g.width-f}},n:function(h,f,e){var j=this.options,g=this.originalSize,i=this.originalPosition;return{top:i.top+e,height:g.height-e}},s:function(g,f,e){return{height:this.originalSize.height+e}},se:function(g,f,e){return c.extend(this._change.s.apply(this,arguments),this._change.e.apply(this,[g,f,e]))},sw:function(g,f,e){return c.extend(this._change.s.apply(this,arguments),this._change.w.apply(this,[g,f,e]))},ne:function(g,f,e){return c.extend(this._change.n.apply(this,arguments),this._change.e.apply(this,[g,f,e]))},nw:function(g,f,e){return c.extend(this._change.n.apply(this,arguments),this._change.w.apply(this,[g,f,e]))}},_propagate:function(f,e){c.ui.plugin.call(this,f,[e,this.ui()]);(f!="resize"&&this._trigger(f,e,this.ui()))},plugins:{},ui:function(){return{originalElement:this.originalElement,element:this.element,helper:this.helper,position:this.position,size:this.size,originalSize:this.originalSize,originalPosition:this.originalPosition}}});c.extend(c.ui.resizable,{version:"1.8.23"});c.ui.plugin.add("resizable","alsoResize",{start:function(f,g){var e=c(this).data("resizable"),i=e.options;var h=function(j){c(j).each(function(){var k=c(this);k.data("resizable-alsoresize",{width:parseInt(k.width(),10),height:parseInt(k.height(),10),left:parseInt(k.css("left"),10),top:parseInt(k.css("top"),10)})})};if(typeof(i.alsoResize)=="object"&&!i.alsoResize.parentNode){if(i.alsoResize.length){i.alsoResize=i.alsoResize[0];h(i.alsoResize)}else{c.each(i.alsoResize,function(j){h(j)})}}else{h(i.alsoResize)}},resize:function(g,i){var f=c(this).data("resizable"),j=f.options,h=f.originalSize,l=f.originalPosition;var k={height:(f.size.height-h.height)||0,width:(f.size.width-h.width)||0,top:(f.position.top-l.top)||0,left:(f.position.left-l.left)||0},e=function(m,n){c(m).each(function(){var q=c(this),r=c(this).data("resizable-alsoresize"),p={},o=n&&n.length?n:q.parents(i.originalElement[0]).length?["width","height"]:["width","height","top","left"];c.each(o,function(s,u){var t=(r[u]||0)+(k[u]||0);if(t&&t>=0){p[u]=t||null}});q.css(p)})};if(typeof(j.alsoResize)=="object"&&!j.alsoResize.nodeType){c.each(j.alsoResize,function(m,n){e(m,n)})}else{e(j.alsoResize)}},stop:function(e,f){c(this).removeData("resizable-alsoresize")}});c.ui.plugin.add("resizable","animate",{stop:function(i,n){var p=c(this).data("resizable"),j=p.options;var h=p._proportionallyResizeElements,e=h.length&&(/textarea/i).test(h[0].nodeName),f=e&&c.ui.hasScroll(h[0],"left")?0:p.sizeDiff.height,l=e?0:p.sizeDiff.width;var g={width:(p.size.width-l),height:(p.size.height-f)},k=(parseInt(p.element.css("left"),10)+(p.position.left-p.originalPosition.left))||null,m=(parseInt(p.element.css("top"),10)+(p.position.top-p.originalPosition.top))||null;p.element.animate(c.extend(g,m&&k?{top:m,left:k}:{}),{duration:j.animateDuration,easing:j.animateEasing,step:function(){var o={width:parseInt(p.element.css("width"),10),height:parseInt(p.element.css("height"),10),top:parseInt(p.element.css("top"),10),left:parseInt(p.element.css("left"),10)};if(h&&h.length){c(h[0]).css({width:o.width,height:o.height})}p._updateCache(o);p._propagate("resize",i)}})}});c.ui.plugin.add("resizable","containment",{start:function(f,r){var t=c(this).data("resizable"),j=t.options,l=t.element;var g=j.containment,k=(g instanceof c)?g.get(0):(/parent/.test(g))?l.parent().get(0):g;if(!k){return}t.containerElement=c(k);if(/document/.test(g)||g==document){t.containerOffset={left:0,top:0};t.containerPosition={left:0,top:0};t.parentData={element:c(document),left:0,top:0,width:c(document).width(),height:c(document).height()||document.body.parentNode.scrollHeight}}else{var n=c(k),i=[];c(["Top","Right","Left","Bottom"]).each(function(p,o){i[p]=b(n.css("padding"+o))});t.containerOffset=n.offset();t.containerPosition=n.position();t.containerSize={height:(n.innerHeight()-i[3]),width:(n.innerWidth()-i[1])};var q=t.containerOffset,e=t.containerSize.height,m=t.containerSize.width,h=(c.ui.hasScroll(k,"left")?k.scrollWidth:m),s=(c.ui.hasScroll(k)?k.scrollHeight:e);t.parentData={element:k,left:q.left,top:q.top,width:h,height:s}}},resize:function(g,q){var t=c(this).data("resizable"),i=t.options,f=t.containerSize,p=t.containerOffset,m=t.size,n=t.position,r=t._aspectRatio||g.shiftKey,e={top:0,left:0},h=t.containerElement;if(h[0]!=document&&(/static/).test(h.css("position"))){e=p}if(n.left<(t._helper?p.left:0)){t.size.width=t.size.width+(t._helper?(t.position.left-p.left):(t.position.left-e.left));if(r){t.size.height=t.size.width/t.aspectRatio}t.position.left=i.helper?p.left:0}if(n.top<(t._helper?p.top:0)){t.size.height=t.size.height+(t._helper?(t.position.top-p.top):t.position.top);if(r){t.size.width=t.size.height*t.aspectRatio}t.position.top=t._helper?p.top:0}t.offset.left=t.parentData.left+t.position.left;t.offset.top=t.parentData.top+t.position.top;var l=Math.abs((t._helper?t.offset.left-e.left:(t.offset.left-e.left))+t.sizeDiff.width),s=Math.abs((t._helper?t.offset.top-e.top:(t.offset.top-p.top))+t.sizeDiff.height);var k=t.containerElement.get(0)==t.element.parent().get(0),j=/relative|absolute/.test(t.containerElement.css("position"));if(k&&j){l-=t.parentData.left}if(l+t.size.width>=t.parentData.width){t.size.width=t.parentData.width-l;if(r){t.size.height=t.size.width/t.aspectRatio}}if(s+t.size.height>=t.parentData.height){t.size.height=t.parentData.height-s;if(r){t.size.width=t.size.height*t.aspectRatio}}},stop:function(f,n){var q=c(this).data("resizable"),g=q.options,l=q.position,m=q.containerOffset,e=q.containerPosition,i=q.containerElement;var j=c(q.helper),r=j.offset(),p=j.outerWidth()-q.sizeDiff.width,k=j.outerHeight()-q.sizeDiff.height;if(q._helper&&!g.animate&&(/relative/).test(i.css("position"))){c(this).css({left:r.left-e.left-m.left,width:p,height:k})}if(q._helper&&!g.animate&&(/static/).test(i.css("position"))){c(this).css({left:r.left-e.left-m.left,width:p,height:k})}}});c.ui.plugin.add("resizable","ghost",{start:function(g,h){var e=c(this).data("resizable"),i=e.options,f=e.size;e.ghost=e.originalElement.clone();e.ghost.css({opacity:0.25,display:"block",position:"relative",height:f.height,width:f.width,margin:0,left:0,top:0}).addClass("ui-resizable-ghost").addClass(typeof i.ghost=="string"?i.ghost:"");e.ghost.appendTo(e.helper)},resize:function(f,g){var e=c(this).data("resizable"),h=e.options;if(e.ghost){e.ghost.css({position:"relative",height:e.size.height,width:e.size.width})}},stop:function(f,g){var e=c(this).data("resizable"),h=e.options;if(e.ghost&&e.helper){e.helper.get(0).removeChild(e.ghost.get(0))}}});c.ui.plugin.add("resizable","grid",{resize:function(e,m){var p=c(this).data("resizable"),h=p.options,k=p.size,i=p.originalSize,j=p.originalPosition,n=p.axis,l=h._aspectRatio||e.shiftKey;h.grid=typeof h.grid=="number"?[h.grid,h.grid]:h.grid;var g=Math.round((k.width-i.width)/(h.grid[0]||1))*(h.grid[0]||1),f=Math.round((k.height-i.height)/(h.grid[1]||1))*(h.grid[1]||1);if(/^(se|s|e)$/.test(n)){p.size.width=i.width+g;p.size.height=i.height+f}else{if(/^(ne)$/.test(n)){p.size.width=i.width+g;p.size.height=i.height+f;p.position.top=j.top-f}else{if(/^(sw)$/.test(n)){p.size.width=i.width+g;p.size.height=i.height+f;p.position.left=j.left-g}else{p.size.width=i.width+g;p.size.height=i.height+f;p.position.top=j.top-f;p.position.left=j.left-g}}}}});var b=function(e){return parseInt(e,10)||0};var a=function(e){return !isNaN(parseInt(e,10))}})(jQuery);
/*
 * jQuery UI Selectable 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Selectables
 *
 * Depends:
 *	jquery.ui.core.js
 *	jquery.ui.mouse.js
 *	jquery.ui.widget.js
 */
(function(a,b){a.widget("ui.selectable",a.ui.mouse,{options:{appendTo:"body",autoRefresh:true,distance:0,filter:"*",tolerance:"touch"},_create:function(){var c=this;this.element.addClass("ui-selectable");this.dragged=false;var d;this.refresh=function(){d=a(c.options.filter,c.element[0]);d.addClass("ui-selectee");d.each(function(){var e=a(this);var f=e.offset();a.data(this,"selectable-item",{element:this,$element:e,left:f.left,top:f.top,right:f.left+e.outerWidth(),bottom:f.top+e.outerHeight(),startselected:false,selected:e.hasClass("ui-selected"),selecting:e.hasClass("ui-selecting"),unselecting:e.hasClass("ui-unselecting")})})};this.refresh();this.selectees=d.addClass("ui-selectee");this._mouseInit();this.helper=a("<div class='ui-selectable-helper'></div>")},destroy:function(){this.selectees.removeClass("ui-selectee").removeData("selectable-item");this.element.removeClass("ui-selectable ui-selectable-disabled").removeData("selectable").unbind(".selectable");this._mouseDestroy();return this},_mouseStart:function(e){var c=this;this.opos=[e.pageX,e.pageY];if(this.options.disabled){return}var d=this.options;this.selectees=a(d.filter,this.element[0]);this._trigger("start",e);a(d.appendTo).append(this.helper);this.helper.css({left:e.clientX,top:e.clientY,width:0,height:0});if(d.autoRefresh){this.refresh()}this.selectees.filter(".ui-selected").each(function(){var f=a.data(this,"selectable-item");f.startselected=true;if(!e.metaKey&&!e.ctrlKey){f.$element.removeClass("ui-selected");f.selected=false;f.$element.addClass("ui-unselecting");f.unselecting=true;c._trigger("unselecting",e,{unselecting:f.element})}});a(e.target).parents().andSelf().each(function(){var g=a.data(this,"selectable-item");if(g){var f=(!e.metaKey&&!e.ctrlKey)||!g.$element.hasClass("ui-selected");g.$element.removeClass(f?"ui-unselecting":"ui-selected").addClass(f?"ui-selecting":"ui-unselecting");g.unselecting=!f;g.selecting=f;g.selected=f;if(f){c._trigger("selecting",e,{selecting:g.element})}else{c._trigger("unselecting",e,{unselecting:g.element})}return false}})},_mouseDrag:function(j){var d=this;this.dragged=true;if(this.options.disabled){return}var f=this.options;var e=this.opos[0],i=this.opos[1],c=j.pageX,h=j.pageY;if(e>c){var g=c;c=e;e=g}if(i>h){var g=h;h=i;i=g}this.helper.css({left:e,top:i,width:c-e,height:h-i});this.selectees.each(function(){var k=a.data(this,"selectable-item");if(!k||k.element==d.element[0]){return}var l=false;if(f.tolerance=="touch"){l=(!(k.left>c||k.right<e||k.top>h||k.bottom<i))}else{if(f.tolerance=="fit"){l=(k.left>e&&k.right<c&&k.top>i&&k.bottom<h)}}if(l){if(k.selected){k.$element.removeClass("ui-selected");k.selected=false}if(k.unselecting){k.$element.removeClass("ui-unselecting");k.unselecting=false}if(!k.selecting){k.$element.addClass("ui-selecting");k.selecting=true;d._trigger("selecting",j,{selecting:k.element})}}else{if(k.selecting){if((j.metaKey||j.ctrlKey)&&k.startselected){k.$element.removeClass("ui-selecting");k.selecting=false;k.$element.addClass("ui-selected");k.selected=true}else{k.$element.removeClass("ui-selecting");k.selecting=false;if(k.startselected){k.$element.addClass("ui-unselecting");k.unselecting=true}d._trigger("unselecting",j,{unselecting:k.element})}}if(k.selected){if(!j.metaKey&&!j.ctrlKey&&!k.startselected){k.$element.removeClass("ui-selected");k.selected=false;k.$element.addClass("ui-unselecting");k.unselecting=true;d._trigger("unselecting",j,{unselecting:k.element})}}}});return false},_mouseStop:function(e){var c=this;this.dragged=false;var d=this.options;a(".ui-unselecting",this.element[0]).each(function(){var f=a.data(this,"selectable-item");f.$element.removeClass("ui-unselecting");f.unselecting=false;f.startselected=false;c._trigger("unselected",e,{unselected:f.element})});a(".ui-selecting",this.element[0]).each(function(){var f=a.data(this,"selectable-item");f.$element.removeClass("ui-selecting").addClass("ui-selected");f.selecting=false;f.selected=true;f.startselected=true;c._trigger("selected",e,{selected:f.element})});this._trigger("stop",e);this.helper.remove();return false}});a.extend(a.ui.selectable,{version:"1.8.23"})})(jQuery);
/*
 * jQuery UI Sortable 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Sortables
 *
 * Depends:
 *	jquery.ui.core.js
 *	jquery.ui.mouse.js
 *	jquery.ui.widget.js
 */
(function(a,b){a.widget("ui.sortable",a.ui.mouse,{widgetEventPrefix:"sort",ready:false,options:{appendTo:"parent",axis:false,connectWith:false,containment:false,cursor:"auto",cursorAt:false,dropOnEmpty:true,forcePlaceholderSize:false,forceHelperSize:false,grid:false,handle:false,helper:"original",items:"> *",opacity:false,placeholder:false,revert:false,scroll:true,scrollSensitivity:20,scrollSpeed:20,scope:"default",tolerance:"intersect",zIndex:1000},_create:function(){var c=this.options;this.containerCache={};this.element.addClass("ui-sortable");this.refresh();this.floating=this.items.length?c.axis==="x"||(/left|right/).test(this.items[0].item.css("float"))||(/inline|table-cell/).test(this.items[0].item.css("display")):false;this.offset=this.element.offset();this._mouseInit();this.ready=true},destroy:function(){a.Widget.prototype.destroy.call(this);this.element.removeClass("ui-sortable ui-sortable-disabled");this._mouseDestroy();for(var c=this.items.length-1;c>=0;c--){this.items[c].item.removeData(this.widgetName+"-item")}return this},_setOption:function(c,d){if(c==="disabled"){this.options[c]=d;this.widget()[d?"addClass":"removeClass"]("ui-sortable-disabled")}else{a.Widget.prototype._setOption.apply(this,arguments)}},_mouseCapture:function(g,h){var f=this;if(this.reverting){return false}if(this.options.disabled||this.options.type=="static"){return false}this._refreshItems(g);var e=null,d=this,c=a(g.target).parents().each(function(){if(a.data(this,f.widgetName+"-item")==d){e=a(this);return false}});if(a.data(g.target,f.widgetName+"-item")==d){e=a(g.target)}if(!e){return false}if(this.options.handle&&!h){var i=false;a(this.options.handle,e).find("*").andSelf().each(function(){if(this==g.target){i=true}});if(!i){return false}}this.currentItem=e;this._removeCurrentsFromItems();return true},_mouseStart:function(f,g,c){var h=this.options,d=this;this.currentContainer=this;this.refreshPositions();this.helper=this._createHelper(f);this._cacheHelperProportions();this._cacheMargins();this.scrollParent=this.helper.scrollParent();this.offset=this.currentItem.offset();this.offset={top:this.offset.top-this.margins.top,left:this.offset.left-this.margins.left};a.extend(this.offset,{click:{left:f.pageX-this.offset.left,top:f.pageY-this.offset.top},parent:this._getParentOffset(),relative:this._getRelativeOffset()});this.helper.css("position","absolute");this.cssPosition=this.helper.css("position");this.originalPosition=this._generatePosition(f);this.originalPageX=f.pageX;this.originalPageY=f.pageY;(h.cursorAt&&this._adjustOffsetFromHelper(h.cursorAt));this.domPosition={prev:this.currentItem.prev()[0],parent:this.currentItem.parent()[0]};if(this.helper[0]!=this.currentItem[0]){this.currentItem.hide()}this._createPlaceholder();if(h.containment){this._setContainment()}if(h.cursor){if(a("body").css("cursor")){this._storedCursor=a("body").css("cursor")}a("body").css("cursor",h.cursor)}if(h.opacity){if(this.helper.css("opacity")){this._storedOpacity=this.helper.css("opacity")}this.helper.css("opacity",h.opacity)}if(h.zIndex){if(this.helper.css("zIndex")){this._storedZIndex=this.helper.css("zIndex")}this.helper.css("zIndex",h.zIndex)}if(this.scrollParent[0]!=document&&this.scrollParent[0].tagName!="HTML"){this.overflowOffset=this.scrollParent.offset()}this._trigger("start",f,this._uiHash());if(!this._preserveHelperProportions){this._cacheHelperProportions()}if(!c){for(var e=this.containers.length-1;e>=0;e--){this.containers[e]._trigger("activate",f,d._uiHash(this))}}if(a.ui.ddmanager){a.ui.ddmanager.current=this}if(a.ui.ddmanager&&!h.dropBehaviour){a.ui.ddmanager.prepareOffsets(this,f)}this.dragging=true;this.helper.addClass("ui-sortable-helper");this._mouseDrag(f);return true},_mouseDrag:function(g){this.position=this._generatePosition(g);this.positionAbs=this._convertPositionTo("absolute");if(!this.lastPositionAbs){this.lastPositionAbs=this.positionAbs}if(this.options.scroll){var h=this.options,c=false;if(this.scrollParent[0]!=document&&this.scrollParent[0].tagName!="HTML"){if((this.overflowOffset.top+this.scrollParent[0].offsetHeight)-g.pageY<h.scrollSensitivity){this.scrollParent[0].scrollTop=c=this.scrollParent[0].scrollTop+h.scrollSpeed}else{if(g.pageY-this.overflowOffset.top<h.scrollSensitivity){this.scrollParent[0].scrollTop=c=this.scrollParent[0].scrollTop-h.scrollSpeed}}if((this.overflowOffset.left+this.scrollParent[0].offsetWidth)-g.pageX<h.scrollSensitivity){this.scrollParent[0].scrollLeft=c=this.scrollParent[0].scrollLeft+h.scrollSpeed}else{if(g.pageX-this.overflowOffset.left<h.scrollSensitivity){this.scrollParent[0].scrollLeft=c=this.scrollParent[0].scrollLeft-h.scrollSpeed}}}else{if(g.pageY-a(document).scrollTop()<h.scrollSensitivity){c=a(document).scrollTop(a(document).scrollTop()-h.scrollSpeed)}else{if(a(window).height()-(g.pageY-a(document).scrollTop())<h.scrollSensitivity){c=a(document).scrollTop(a(document).scrollTop()+h.scrollSpeed)}}if(g.pageX-a(document).scrollLeft()<h.scrollSensitivity){c=a(document).scrollLeft(a(document).scrollLeft()-h.scrollSpeed)}else{if(a(window).width()-(g.pageX-a(document).scrollLeft())<h.scrollSensitivity){c=a(document).scrollLeft(a(document).scrollLeft()+h.scrollSpeed)}}}if(c!==false&&a.ui.ddmanager&&!h.dropBehaviour){a.ui.ddmanager.prepareOffsets(this,g)}}this.positionAbs=this._convertPositionTo("absolute");if(!this.options.axis||this.options.axis!="y"){this.helper[0].style.left=this.position.left+"px"}if(!this.options.axis||this.options.axis!="x"){this.helper[0].style.top=this.position.top+"px"}for(var e=this.items.length-1;e>=0;e--){var f=this.items[e],d=f.item[0],j=this._intersectsWithPointer(f);if(!j){continue}if(d!=this.currentItem[0]&&this.placeholder[j==1?"next":"prev"]()[0]!=d&&!a.ui.contains(this.placeholder[0],d)&&(this.options.type=="semi-dynamic"?!a.ui.contains(this.element[0],d):true)){this.direction=j==1?"down":"up";if(this.options.tolerance=="pointer"||this._intersectsWithSides(f)){this._rearrange(g,f)}else{break}this._trigger("change",g,this._uiHash());break}}this._contactContainers(g);if(a.ui.ddmanager){a.ui.ddmanager.drag(this,g)}this._trigger("sort",g,this._uiHash());this.lastPositionAbs=this.positionAbs;return false},_mouseStop:function(d,e){if(!d){return}if(a.ui.ddmanager&&!this.options.dropBehaviour){a.ui.ddmanager.drop(this,d)}if(this.options.revert){var c=this;var f=c.placeholder.offset();c.reverting=true;a(this.helper).animate({left:f.left-this.offset.parent.left-c.margins.left+(this.offsetParent[0]==document.body?0:this.offsetParent[0].scrollLeft),top:f.top-this.offset.parent.top-c.margins.top+(this.offsetParent[0]==document.body?0:this.offsetParent[0].scrollTop)},parseInt(this.options.revert,10)||500,function(){c._clear(d)})}else{this._clear(d,e)}return false},cancel:function(){var c=this;if(this.dragging){this._mouseUp({target:null});if(this.options.helper=="original"){this.currentItem.css(this._storedCSS).removeClass("ui-sortable-helper")}else{this.currentItem.show()}for(var d=this.containers.length-1;d>=0;d--){this.containers[d]._trigger("deactivate",null,c._uiHash(this));if(this.containers[d].containerCache.over){this.containers[d]._trigger("out",null,c._uiHash(this));this.containers[d].containerCache.over=0}}}if(this.placeholder){if(this.placeholder[0].parentNode){this.placeholder[0].parentNode.removeChild(this.placeholder[0])}if(this.options.helper!="original"&&this.helper&&this.helper[0].parentNode){this.helper.remove()}a.extend(this,{helper:null,dragging:false,reverting:false,_noFinalSort:null});if(this.domPosition.prev){a(this.domPosition.prev).after(this.currentItem)}else{a(this.domPosition.parent).prepend(this.currentItem)}}return this},serialize:function(e){var c=this._getItemsAsjQuery(e&&e.connected);var d=[];e=e||{};a(c).each(function(){var f=(a(e.item||this).attr(e.attribute||"id")||"").match(e.expression||(/(.+)[-=_](.+)/));if(f){d.push((e.key||f[1]+"[]")+"="+(e.key&&e.expression?f[1]:f[2]))}});if(!d.length&&e.key){d.push(e.key+"=")}return d.join("&")},toArray:function(e){var c=this._getItemsAsjQuery(e&&e.connected);var d=[];e=e||{};c.each(function(){d.push(a(e.item||this).attr(e.attribute||"id")||"")});return d},_intersectsWith:function(m){var e=this.positionAbs.left,d=e+this.helperProportions.width,k=this.positionAbs.top,j=k+this.helperProportions.height;var f=m.left,c=f+m.width,n=m.top,i=n+m.height;var o=this.offset.click.top,h=this.offset.click.left;var g=(k+o)>n&&(k+o)<i&&(e+h)>f&&(e+h)<c;if(this.options.tolerance=="pointer"||this.options.forcePointerForContainers||(this.options.tolerance!="pointer"&&this.helperProportions[this.floating?"width":"height"]>m[this.floating?"width":"height"])){return g}else{return(f<e+(this.helperProportions.width/2)&&d-(this.helperProportions.width/2)<c&&n<k+(this.helperProportions.height/2)&&j-(this.helperProportions.height/2)<i)}},_intersectsWithPointer:function(e){var f=(this.options.axis==="x")||a.ui.isOverAxis(this.positionAbs.top+this.offset.click.top,e.top,e.height),d=(this.options.axis==="y")||a.ui.isOverAxis(this.positionAbs.left+this.offset.click.left,e.left,e.width),h=f&&d,c=this._getDragVerticalDirection(),g=this._getDragHorizontalDirection();if(!h){return false}return this.floating?(((g&&g=="right")||c=="down")?2:1):(c&&(c=="down"?2:1))},_intersectsWithSides:function(f){var d=a.ui.isOverAxis(this.positionAbs.top+this.offset.click.top,f.top+(f.height/2),f.height),e=a.ui.isOverAxis(this.positionAbs.left+this.offset.click.left,f.left+(f.width/2),f.width),c=this._getDragVerticalDirection(),g=this._getDragHorizontalDirection();if(this.floating&&g){return((g=="right"&&e)||(g=="left"&&!e))}else{return c&&((c=="down"&&d)||(c=="up"&&!d))}},_getDragVerticalDirection:function(){var c=this.positionAbs.top-this.lastPositionAbs.top;return c!=0&&(c>0?"down":"up")},_getDragHorizontalDirection:function(){var c=this.positionAbs.left-this.lastPositionAbs.left;return c!=0&&(c>0?"right":"left")},refresh:function(c){this._refreshItems(c);this.refreshPositions();return this},_connectWith:function(){var c=this.options;return c.connectWith.constructor==String?[c.connectWith]:c.connectWith},_getItemsAsjQuery:function(c){var m=this;var h=[];var f=[];var k=this._connectWith();if(k&&c){for(var e=k.length-1;e>=0;e--){var l=a(k[e]);for(var d=l.length-1;d>=0;d--){var g=a.data(l[d],this.widgetName);if(g&&g!=this&&!g.options.disabled){f.push([a.isFunction(g.options.items)?g.options.items.call(g.element):a(g.options.items,g.element).not(".ui-sortable-helper").not(".ui-sortable-placeholder"),g])}}}}f.push([a.isFunction(this.options.items)?this.options.items.call(this.element,null,{options:this.options,item:this.currentItem}):a(this.options.items,this.element).not(".ui-sortable-helper").not(".ui-sortable-placeholder"),this]);for(var e=f.length-1;e>=0;e--){f[e][0].each(function(){h.push(this)})}return a(h)},_removeCurrentsFromItems:function(){var e=this.currentItem.find(":data("+this.widgetName+"-item)");for(var d=0;d<this.items.length;d++){for(var c=0;c<e.length;c++){if(e[c]==this.items[d].item[0]){this.items.splice(d,1)}}}},_refreshItems:function(c){this.items=[];this.containers=[this];var k=this.items;var q=this;var g=[[a.isFunction(this.options.items)?this.options.items.call(this.element[0],c,{item:this.currentItem}):a(this.options.items,this.element),this]];var m=this._connectWith();if(m&&this.ready){for(var f=m.length-1;f>=0;f--){var n=a(m[f]);for(var e=n.length-1;e>=0;e--){var h=a.data(n[e],this.widgetName);if(h&&h!=this&&!h.options.disabled){g.push([a.isFunction(h.options.items)?h.options.items.call(h.element[0],c,{item:this.currentItem}):a(h.options.items,h.element),h]);this.containers.push(h)}}}}for(var f=g.length-1;f>=0;f--){var l=g[f][1];var d=g[f][0];for(var e=0,o=d.length;e<o;e++){var p=a(d[e]);p.data(this.widgetName+"-item",l);k.push({item:p,instance:l,width:0,height:0,left:0,top:0})}}},refreshPositions:function(c){if(this.offsetParent&&this.helper){this.offset.parent=this._getParentOffset()}for(var e=this.items.length-1;e>=0;e--){var f=this.items[e];if(f.instance!=this.currentContainer&&this.currentContainer&&f.item[0]!=this.currentItem[0]){continue}var d=this.options.toleranceElement?a(this.options.toleranceElement,f.item):f.item;if(!c){f.width=d.outerWidth();f.height=d.outerHeight()}var g=d.offset();f.left=g.left;f.top=g.top}if(this.options.custom&&this.options.custom.refreshContainers){this.options.custom.refreshContainers.call(this)}else{for(var e=this.containers.length-1;e>=0;e--){var g=this.containers[e].element.offset();this.containers[e].containerCache.left=g.left;this.containers[e].containerCache.top=g.top;this.containers[e].containerCache.width=this.containers[e].element.outerWidth();this.containers[e].containerCache.height=this.containers[e].element.outerHeight()}}return this},_createPlaceholder:function(e){var c=e||this,f=c.options;if(!f.placeholder||f.placeholder.constructor==String){var d=f.placeholder;f.placeholder={element:function(){var g=a(document.createElement(c.currentItem[0].nodeName)).addClass(d||c.currentItem[0].className+" ui-sortable-placeholder").removeClass("ui-sortable-helper")[0];if(!d){g.style.visibility="hidden"}return g},update:function(g,h){if(d&&!f.forcePlaceholderSize){return}if(!h.height()){h.height(c.currentItem.innerHeight()-parseInt(c.currentItem.css("paddingTop")||0,10)-parseInt(c.currentItem.css("paddingBottom")||0,10))}if(!h.width()){h.width(c.currentItem.innerWidth()-parseInt(c.currentItem.css("paddingLeft")||0,10)-parseInt(c.currentItem.css("paddingRight")||0,10))}}}}c.placeholder=a(f.placeholder.element.call(c.element,c.currentItem));c.currentItem.after(c.placeholder);f.placeholder.update(c,c.placeholder)},_contactContainers:function(c){var e=null,l=null;for(var g=this.containers.length-1;g>=0;g--){if(a.ui.contains(this.currentItem[0],this.containers[g].element[0])){continue}if(this._intersectsWith(this.containers[g].containerCache)){if(e&&a.ui.contains(this.containers[g].element[0],e.element[0])){continue}e=this.containers[g];l=g}else{if(this.containers[g].containerCache.over){this.containers[g]._trigger("out",c,this._uiHash(this));this.containers[g].containerCache.over=0}}}if(!e){return}if(this.containers.length===1){this.containers[l]._trigger("over",c,this._uiHash(this));this.containers[l].containerCache.over=1}else{if(this.currentContainer!=this.containers[l]){var k=10000;var h=null;var d=this.positionAbs[this.containers[l].floating?"left":"top"];for(var f=this.items.length-1;f>=0;f--){if(!a.ui.contains(this.containers[l].element[0],this.items[f].item[0])){continue}var m=this.containers[l].floating?this.items[f].item.offset().left:this.items[f].item.offset().top;if(Math.abs(m-d)<k){k=Math.abs(m-d);h=this.items[f];this.direction=(m-d>0)?"down":"up"}}if(!h&&!this.options.dropOnEmpty){return}this.currentContainer=this.containers[l];h?this._rearrange(c,h,null,true):this._rearrange(c,null,this.containers[l].element,true);this._trigger("change",c,this._uiHash());this.containers[l]._trigger("change",c,this._uiHash(this));this.options.placeholder.update(this.currentContainer,this.placeholder);this.containers[l]._trigger("over",c,this._uiHash(this));this.containers[l].containerCache.over=1}}},_createHelper:function(d){var e=this.options;var c=a.isFunction(e.helper)?a(e.helper.apply(this.element[0],[d,this.currentItem])):(e.helper=="clone"?this.currentItem.clone():this.currentItem);if(!c.parents("body").length){a(e.appendTo!="parent"?e.appendTo:this.currentItem[0].parentNode)[0].appendChild(c[0])}if(c[0]==this.currentItem[0]){this._storedCSS={width:this.currentItem[0].style.width,height:this.currentItem[0].style.height,position:this.currentItem.css("position"),top:this.currentItem.css("top"),left:this.currentItem.css("left")}}if(c[0].style.width==""||e.forceHelperSize){c.width(this.currentItem.width())}if(c[0].style.height==""||e.forceHelperSize){c.height(this.currentItem.height())}return c},_adjustOffsetFromHelper:function(c){if(typeof c=="string"){c=c.split(" ")}if(a.isArray(c)){c={left:+c[0],top:+c[1]||0}}if("left" in c){this.offset.click.left=c.left+this.margins.left}if("right" in c){this.offset.click.left=this.helperProportions.width-c.right+this.margins.left}if("top" in c){this.offset.click.top=c.top+this.margins.top}if("bottom" in c){this.offset.click.top=this.helperProportions.height-c.bottom+this.margins.top}},_getParentOffset:function(){this.offsetParent=this.helper.offsetParent();var c=this.offsetParent.offset();if(this.cssPosition=="absolute"&&this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0])){c.left+=this.scrollParent.scrollLeft();c.top+=this.scrollParent.scrollTop()}if((this.offsetParent[0]==document.body)||(this.offsetParent[0].tagName&&this.offsetParent[0].tagName.toLowerCase()=="html"&&a.browser.msie)){c={top:0,left:0}}return{top:c.top+(parseInt(this.offsetParent.css("borderTopWidth"),10)||0),left:c.left+(parseInt(this.offsetParent.css("borderLeftWidth"),10)||0)}},_getRelativeOffset:function(){if(this.cssPosition=="relative"){var c=this.currentItem.position();return{top:c.top-(parseInt(this.helper.css("top"),10)||0)+this.scrollParent.scrollTop(),left:c.left-(parseInt(this.helper.css("left"),10)||0)+this.scrollParent.scrollLeft()}}else{return{top:0,left:0}}},_cacheMargins:function(){this.margins={left:(parseInt(this.currentItem.css("marginLeft"),10)||0),top:(parseInt(this.currentItem.css("marginTop"),10)||0)}},_cacheHelperProportions:function(){this.helperProportions={width:this.helper.outerWidth(),height:this.helper.outerHeight()}},_setContainment:function(){var f=this.options;if(f.containment=="parent"){f.containment=this.helper[0].parentNode}if(f.containment=="document"||f.containment=="window"){this.containment=[0-this.offset.relative.left-this.offset.parent.left,0-this.offset.relative.top-this.offset.parent.top,a(f.containment=="document"?document:window).width()-this.helperProportions.width-this.margins.left,(a(f.containment=="document"?document:window).height()||document.body.parentNode.scrollHeight)-this.helperProportions.height-this.margins.top]}if(!(/^(document|window|parent)$/).test(f.containment)){var d=a(f.containment)[0];var e=a(f.containment).offset();var c=(a(d).css("overflow")!="hidden");this.containment=[e.left+(parseInt(a(d).css("borderLeftWidth"),10)||0)+(parseInt(a(d).css("paddingLeft"),10)||0)-this.margins.left,e.top+(parseInt(a(d).css("borderTopWidth"),10)||0)+(parseInt(a(d).css("paddingTop"),10)||0)-this.margins.top,e.left+(c?Math.max(d.scrollWidth,d.offsetWidth):d.offsetWidth)-(parseInt(a(d).css("borderLeftWidth"),10)||0)-(parseInt(a(d).css("paddingRight"),10)||0)-this.helperProportions.width-this.margins.left,e.top+(c?Math.max(d.scrollHeight,d.offsetHeight):d.offsetHeight)-(parseInt(a(d).css("borderTopWidth"),10)||0)-(parseInt(a(d).css("paddingBottom"),10)||0)-this.helperProportions.height-this.margins.top]}},_convertPositionTo:function(g,i){if(!i){i=this.position}var e=g=="absolute"?1:-1;var f=this.options,c=this.cssPosition=="absolute"&&!(this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,h=(/(html|body)/i).test(c[0].tagName);return{top:(i.top+this.offset.relative.top*e+this.offset.parent.top*e-(a.browser.safari&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollTop():(h?0:c.scrollTop()))*e)),left:(i.left+this.offset.relative.left*e+this.offset.parent.left*e-(a.browser.safari&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():h?0:c.scrollLeft())*e))}},_generatePosition:function(f){var i=this.options,c=this.cssPosition=="absolute"&&!(this.scrollParent[0]!=document&&a.ui.contains(this.scrollParent[0],this.offsetParent[0]))?this.offsetParent:this.scrollParent,j=(/(html|body)/i).test(c[0].tagName);if(this.cssPosition=="relative"&&!(this.scrollParent[0]!=document&&this.scrollParent[0]!=this.offsetParent[0])){this.offset.relative=this._getRelativeOffset()}var e=f.pageX;var d=f.pageY;if(this.originalPosition){if(this.containment){if(f.pageX-this.offset.click.left<this.containment[0]){e=this.containment[0]+this.offset.click.left}if(f.pageY-this.offset.click.top<this.containment[1]){d=this.containment[1]+this.offset.click.top}if(f.pageX-this.offset.click.left>this.containment[2]){e=this.containment[2]+this.offset.click.left}if(f.pageY-this.offset.click.top>this.containment[3]){d=this.containment[3]+this.offset.click.top}}if(i.grid){var h=this.originalPageY+Math.round((d-this.originalPageY)/i.grid[1])*i.grid[1];d=this.containment?(!(h-this.offset.click.top<this.containment[1]||h-this.offset.click.top>this.containment[3])?h:(!(h-this.offset.click.top<this.containment[1])?h-i.grid[1]:h+i.grid[1])):h;var g=this.originalPageX+Math.round((e-this.originalPageX)/i.grid[0])*i.grid[0];e=this.containment?(!(g-this.offset.click.left<this.containment[0]||g-this.offset.click.left>this.containment[2])?g:(!(g-this.offset.click.left<this.containment[0])?g-i.grid[0]:g+i.grid[0])):g}}return{top:(d-this.offset.click.top-this.offset.relative.top-this.offset.parent.top+(a.browser.safari&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollTop():(j?0:c.scrollTop())))),left:(e-this.offset.click.left-this.offset.relative.left-this.offset.parent.left+(a.browser.safari&&this.cssPosition=="fixed"?0:(this.cssPosition=="fixed"?-this.scrollParent.scrollLeft():j?0:c.scrollLeft())))}},_rearrange:function(h,g,d,f){d?d[0].appendChild(this.placeholder[0]):g.item[0].parentNode.insertBefore(this.placeholder[0],(this.direction=="down"?g.item[0]:g.item[0].nextSibling));this.counter=this.counter?++this.counter:1;var e=this,c=this.counter;window.setTimeout(function(){if(c==e.counter){e.refreshPositions(!f)}},0)},_clear:function(e,f){this.reverting=false;var g=[],c=this;if(!this._noFinalSort&&this.currentItem.parent().length){this.placeholder.before(this.currentItem)}this._noFinalSort=null;if(this.helper[0]==this.currentItem[0]){for(var d in this._storedCSS){if(this._storedCSS[d]=="auto"||this._storedCSS[d]=="static"){this._storedCSS[d]=""}}this.currentItem.css(this._storedCSS).removeClass("ui-sortable-helper")}else{this.currentItem.show()}if(this.fromOutside&&!f){g.push(function(h){this._trigger("receive",h,this._uiHash(this.fromOutside))})}if((this.fromOutside||this.domPosition.prev!=this.currentItem.prev().not(".ui-sortable-helper")[0]||this.domPosition.parent!=this.currentItem.parent()[0])&&!f){g.push(function(h){this._trigger("update",h,this._uiHash())})}if(!a.ui.contains(this.element[0],this.currentItem[0])){if(!f){g.push(function(h){this._trigger("remove",h,this._uiHash())})}for(var d=this.containers.length-1;d>=0;d--){if(a.ui.contains(this.containers[d].element[0],this.currentItem[0])&&!f){g.push((function(h){return function(i){h._trigger("receive",i,this._uiHash(this))}}).call(this,this.containers[d]));g.push((function(h){return function(i){h._trigger("update",i,this._uiHash(this))}}).call(this,this.containers[d]))}}}for(var d=this.containers.length-1;d>=0;d--){if(!f){g.push((function(h){return function(i){h._trigger("deactivate",i,this._uiHash(this))}}).call(this,this.containers[d]))}if(this.containers[d].containerCache.over){g.push((function(h){return function(i){h._trigger("out",i,this._uiHash(this))}}).call(this,this.containers[d]));this.containers[d].containerCache.over=0}}if(this._storedCursor){a("body").css("cursor",this._storedCursor)}if(this._storedOpacity){this.helper.css("opacity",this._storedOpacity)}if(this._storedZIndex){this.helper.css("zIndex",this._storedZIndex=="auto"?"":this._storedZIndex)}this.dragging=false;if(this.cancelHelperRemoval){if(!f){this._trigger("beforeStop",e,this._uiHash());for(var d=0;d<g.length;d++){g[d].call(this,e)}this._trigger("stop",e,this._uiHash())}this.fromOutside=false;return false}if(!f){this._trigger("beforeStop",e,this._uiHash())}this.placeholder[0].parentNode.removeChild(this.placeholder[0]);if(this.helper[0]!=this.currentItem[0]){this.helper.remove()}this.helper=null;if(!f){for(var d=0;d<g.length;d++){g[d].call(this,e)}this._trigger("stop",e,this._uiHash())}this.fromOutside=false;return true},_trigger:function(){if(a.Widget.prototype._trigger.apply(this,arguments)===false){this.cancel()}},_uiHash:function(d){var c=d||this;return{helper:c.helper,placeholder:c.placeholder||a([]),position:c.position,originalPosition:c.originalPosition,offset:c.positionAbs,item:c.currentItem,sender:d?d.element:null}}});a.extend(a.ui.sortable,{version:"1.8.23"})})(jQuery);
/*
 * jQuery UI Slider 1.8.23
 *
 * Copyright 2012, AUTHORS.txt (http://jqueryui.com/about)
 * Dual licensed under the MIT or GPL Version 2 licenses.
 * http://jquery.org/license
 *
 * http://docs.jquery.com/UI/Slider
 *
 * Depends:
 *	jquery.ui.core.js
 *	jquery.ui.mouse.js
 *	jquery.ui.widget.js
 */
(function(b,c){var a=5;b.widget("ui.slider",b.ui.mouse,{widgetEventPrefix:"slide",options:{animate:false,distance:0,max:100,min:0,orientation:"horizontal",range:false,step:1,value:0,values:null},_create:function(){var e=this,k=this.options,j=this.element.find(".ui-slider-handle").addClass("ui-state-default ui-corner-all"),h="`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/primefaces.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="ui-selectcheckboxmenu-close ui-corner-all" href="#"><span class="ui-icon ui-icon-circle-close"></span></a>`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="logo-name"> <img src="/theme/images/header/logo-sunshine.png" alt="Transparence Santé : Espace entreprises" />
					</a>`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#'></a>`
  
  
  
  
Instances: 8
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [http://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](http://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 1
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse](https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/](https://entreprises-transparence.sante.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow](https://entreprises-transparence.sante.gouv.fr/flow)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/robots.txt](https://entreprises-transparence.sante.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/sitemap.xml](https://entreprises-transparence.sante.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/main](https://entreprises-transparence.sante.gouv.fr/flow/main)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr](https://entreprises-transparence.sante.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 7
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/login.xhtml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `10000000`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/theme.css?ln=primefaces-aristo](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/theme.css?ln=primefaces-aristo)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000000`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml](https://entreprises-transparence.sante.gouv.fr/flow/info_faq.xhtml)
  
  
  * Method: `GET`
  
  
  * Evidence: `20170701`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `86400000`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/theme.css?ln=primefaces-aristo](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/theme.css?ln=primefaces-aristo)
  
  
  * Method: `GET`
  
  
  * Evidence: `33000000`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces](https://entreprises-transparence.sante.gouv.fr/flow/javax.faces.resource/jquery/jquery-plugins.js?ln=primefaces)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/theme/images/favicon.ico](https://entreprises-transparence.sante.gouv.fr/theme/images/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `44444444`
  
  
  
  
Instances: 7
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>10000000, which evaluates to: 1970-04-26 17:46:40</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1](https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1)
  
  
  * Method: `GET`
  
  
  * Parameter: `execution`
  
  
  
  
Instances: 1
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://entreprises-transparence.sante.gouv.fr/flow/recupMotPasse?execution=e1s1</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>execution=e1s1</p><p></p><p>The user-controlled value was:</p><p>e1s1</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3
