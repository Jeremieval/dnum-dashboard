
# ZAP Scanning Report

Generated on Thu, 18 Mar 2021 20:11:57


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 5 |
| Low | 9 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 12 | 
| Source Code Disclosure - PHP | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| Vulnerable JS Library | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 9 | 
| Cookie Without SameSite Attribute | Low | 3 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 4 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Secure Pages Include Mixed Content | Low | 5 | 
| Strict-Transport-Security Header Not Set | Low | 9 | 
| Base64 Disclosure | Informational | 12 | 
| Content-Type Header Missing | Informational | 9 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 9 | 
| Storable but Non-Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 13 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 12 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/Point_Loi_ESS_-_Associations.pdf](https://www.associations.gouv.fr/IMG/pdf/Point_Loi_ESS_-_Associations.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `500296352296`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 500296</p><p>Brand: MAESTRO</p><p>Category: </p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/la-vie-associative.html](https://www.associations.gouv.fr/la-vie-associative.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/documentation.html](https://www.associations.gouv.fr/documentation.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/guide-juridique-et-fiscal.html](https://www.associations.gouv.fr/guide-juridique-et-fiscal.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/creer-votre-association.html](https://www.associations.gouv.fr/creer-votre-association.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/demarches.html](https://www.associations.gouv.fr/demarches.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/financer-votre-association.html](https://www.associations.gouv.fr/financer-votre-association.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html](https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.associations.gouv.fr/je-suis-actif.html](https://www.associations.gouv.fr/je-suis-actif.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.dailymotion.com/video/x14aza7_etre-benevole_news" target="_blank">&Ecirc;tre b&eacute;n&eacute;vole</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.dailymotion.com/video/x14aza7_etre-benevole_news" target="_blank">&Ecirc;tre b&eacute;n&eacute;vole</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/seuils-de-subventions-en-nature-ou-en-numeraire.html](https://www.associations.gouv.fr/seuils-de-subventions-en-nature-ou-en-numeraire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.legifrance.gouv.fr/affichTexte.do;jsessionid=?cidTexte=JORFTEXT000029313296&amp;dateTexte=&amp;oldAction=dernierJO&amp;categorieLien=id#JORFSCTA000029313461" title="nouvelle fenêtre vers legifrance" target="_blank">Article 59 de la loi  n&#176;2014-856 du 31 juillet 2014</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/existe-t-il-un-formulaire-unique-ou-commun-de-demande-de-subvention.html](https://www.associations.gouv.fr/existe-t-il-un-formulaire-unique-ou-commun-de-demande-de-subvention.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.formulaires.modernisation.gouv.fr/gf/cerfa_12156.do" target="_blank" title="nouvelle fenêtre vers le formulaire">Accéder au formulaire</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-suis-jeune.html](https://www.associations.gouv.fr/je-suis-jeune.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.dailymotion.com/video/x14aza7_etre-benevole_news" target="_blank">&Ecirc;tre b&eacute;n&eacute;vole</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-points-ressources.html](https://www.associations.gouv.fr/les-points-ressources.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.dailymotion.com/video/x14aza7_etre-benevole_news" target="_blank">&Ecirc;tre b&eacute;n&eacute;vole</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-suis-senior.html](https://www.associations.gouv.fr/je-suis-senior.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.dailymotion.com/video/x14aza7_etre-benevole_news" target="_blank">&Ecirc;tre b&eacute;n&eacute;vole</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/quelles-sont-les-procedures-de-resolution-de-difficultes-graves-au-sein-d-une-association.html](https://www.associations.gouv.fr/quelles-sont-les-procedures-de-resolution-de-difficultes-graves-au-sein-d-une-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.annuaires.justice.gouv.fr/lieux-dacces-aux-droits-10111/" target="_blank" title="lien vers le ministère de la justice et des libertés - nouvelle fenêtre">Les lieux d&#8217;accès aux droits</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/videos.html](https://www.associations.gouv.fr/videos.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.dailymotion.com/video/x49c585_projet-de-loi-egalite-citoyennete_school" target="_blank">Projet de loi &quot;Egalit&eacute; Citoyennet&eacute;&quot;</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/peut-on-transferer-une-association-etrangere-en-france.html](https://www.associations.gouv.fr/peut-on-transferer-une-association-etrangere-en-france.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.legifrance.gouv.fr/affichTexte.do?cidTexte=JORFTEXT000000497458&amp;fastPos=1&amp;fastReqId=646480853&amp;categorieLien=cid&amp;oldAction=rechTexte" target="_blank" title="nouvelle fenêtre vers legifrance">l&#8217;article 5 loi du 1er juillet 1901</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/quelles-sont-les-mesures-specifiques-pour-l-emploi-salarie-du-secteur-sportif.html](https://www.associations.gouv.fr/quelles-sont-les-mesures-specifiques-pour-l-emploi-salarie-du-secteur-sportif.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.urssaf.fr/profil/associations/documentation/guides,_chartes_et_conventions/guides_01.html" target="_blank" title="nouvelle fenêtre vers urssaf.fr">www.urssaf.fr</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/une-association-peut-elle-organiser-une-vente-au-deballage.html](https://www.associations.gouv.fr/une-association-peut-elle-organiser-une-vente-au-deballage.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.formulaires.modernisation.gouv.fr/gf/cerfa_13939.do" target="_blank" title="nouvelle fenêtre">déclaration</a>`
  
  
  
  
Instances: 12
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-vie-associative.html](https://www.associations.gouv.fr/la-vie-associative.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html](https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/DP_-_La_France_s_engage.pdf](https://www.associations.gouv.fr/IMG/pdf/DP_-_La_France_s_engage.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=³BONÏ/îx63ïoL´&eÀ\x0004%Û®wôF°ç\x0013QnD:û¡'
Ì
´©ÓæZETÏ`!¬ÿ\x0002º\x0003æut/µÁ^^^³O¼Dãáî%Ê]òV§|m3ÖBd³)òã1zUæi	ÉÈYÉ\x0004'õM\x000f(USaæâÚ\x0011ø¿SbX\x001bI¶\x001d¹\x0010½ »Vp[dâö"»q\x0016:3\¼\x000edÚ½P$¯2¹\x0004Ç(¬\x000bãr´\x0003Ë\x0002|þ z+séä32D
µ
Ú8ÜÍù}EkF\x00152\x000cEÝåÊ\x0008\x001efõ¨
UÕà*"T¨\x0011ê«ù\x0015y¼ü­JÀ\x001dÊº¡ênÙ5l¢'»'ØñDº¡2tÏ\x0000è¾zìÎ<ÀÃ\x000eÏµ!ÛjË\x000b\x0008â%Ï%ù²º\x00077ü÷ý^·\x00123f'\x0008(ánì\x001b¯GiÂð3¢ÏÅ>ÀG\x0016l'?çdë»8\x000cÉÖ\x001f>\x001cd\x0010|-Û\x000fg«³³ Å\x001f?~dNl\x0004P·¯\x001e.ûC\x0017îPìÇÁ\x001cÉa3\x0002w¾z>tç\x0003?ÅæÐ\x0013\x0015\x0000/ï\x00125Ð\x001f\x000eÅVÔÀ\x0014vÌ^\x000c<°ìýúº\x0005\x000bøêÿY\x0004ßé®+ÏÏÎ¾¬J¼×\x001f\x0003'Ì|tmÎrýF@R\x000cÊ®
«þþ×ù\x0019á(!\x000c±\x001f.R\x0007J\x001bHé\x000bÌvÁ6ðu^IzXp\x0006¤ö 
F\x0013l¹¸B|'5V¢\x001cÔ¶¶\x0001nëo\x001c\x0004Ô2¯´\sõ\x0012\x0018,\x0016AÆíaÑÍñ$\x0015ð¯¼ÓÂ&»{Z\x0016\x0018²EëJüÐEK5-\x0000ï\x0014@¾'\x0008P¯ºÚ$À.­¬\x0006b¨q³&Þ\x0000\x0008ê#Vëù\x0001­yÇì\x0011mhÀÙàoD!\x000fXX\x001dýÜõæúÚ¸\x000e:Nä¹\x000e\x00194\z;7­\x0015½\x0006¹æ\x0007­ÃëF×0¢6Oë\x0005ü1ë(Tö^×ö¨ú'\x0003\x0019êäÄ\x0004\x0002|î\x0003¼qp]×l[ëÌ­Ø\x0005ôç?ð\x0001Ýw­Þ@üWÏ5IÈä¸&I^Ufz³µ|ü¢ëê}~£.	*úüýüÝð\x0002P\x0006`2õC¨Ö@Wç\x001a»×ÉR3ÑÏ
\x0004½[Þ\x0003µ¯®Þ°x`­;Â`\x001a,ûÇû©aN÷¨Á»Z#«þ]\x0007ýUX\x000b#?
çÀÌµ\x0013J@ÙÝCéAâfÐ´TÜÞ
Â\x000e\x000f\x0006\x0011j\x0001\x0005G@ø óÊå\x001cd´È_öÒeUN*34y\x00141«\x0002@yp¿Cü\x000cÝÜ£\x0011)fñ,\x0006oÌX2\x000füù\x0002LZ,ü9´\x0018=Ð\x0000ö\x000cî3÷=ü×Of3¸f:
\x0019 ®?Ç3\x0005ßÏ\x0007ùÌ»úåí\x0006úeª§\x0008\x0006ØÍ,ß¸Ú0!ý\x000fÓþâbõ'è0=Ð_\x0013hÈ\x0010\x0012éýwµò\x0011§!Q\x000c\x0010­Û"à¢A´\x0006@\x0002\x0018îQ-Ñé÷ØÉV]+ãÇÄ´óJà)@f\x001aa°A\x0004Qf¸°ð\x001cGûT\x0002Ã\x0001æyËáJCQ 	 ç\x000f;((n0°aß;õØYÕi6\x0003¶§\x0000%{Ë5óë]èe£);ÜÍ¡É¾B9ÛB\x000fp½æMdÐ9±iô\x0018PÉÝ}vJ]Ô|[
w¹®¥Ò\_p\x0014PlFç\x000b§Csñbl!"S¢y±ÇáÀ\x0005øz/K\x0016\x0001\x000bè%U5íà\x000cE\x0001÷q¶¤\x0015;øÐ~Ð±ÛZiÍqHÈtXÕ`\x0012§Ö£0SO#~ìÌ{¢Ùã<\x001fúÏ}g;Ë(k\x001cÔµü>xå@õv,3¤ÍKä~ø¥­+7\x000e
Mb$¡¿ð°`Ê4fÙxÝB\x0012\x00144Ì('Öº=:ÐëP\x0016d]îæ=ºM&' ] %(\x0014lú¡\x0013\x001f;J\x001eª\x0007\x001eqbR¦\x0011}¢òz^¼vFS\x0002DÏVø°åû.\x000cÔ¥Åp$¥¦áíëL	ê\x0008ffv5Õ=;a7ë fLÇh\x0006È\x0012\x0005Ù\x0002@¹÷®ÛÄF)6ÝÈ\x001aR0è@\x001dÑ]a\x0010x'××·ç:3À;y\x001aöMN
.\x0012¡\x001f\x001b¶¶\x0000)²¼àFÚ¸-õ·ó"\x0014 ±×©\x0001;\x0004B0!²êïÌ¯V
¯[êí\x000bÂCMð3»\x0017ª¥Ò\x00110\x0015\x0005>ÜÉY\x0000W_¨¹ùå¼A0&\x0014uîªÍ\x0019&·°}­\x0008uÏ\x001cY3T\x0005GñEÝåÊhe³Á1
¸\x0008Åý\x0007[é¦\x001e3Æ$Ekúy@QÝZ\x001b¨¢t?\x0007\x0014÷ä
iÈIÝ\x0008òpnj\Ò³\x000fòeK>Ó\x0019\x00087lõ ¾½\x001ecø\x0015 &üLßÈ×Æ:a'¼Î ×Ö\@®{%?\x00032ÒýÅ§\x0005áÓÄìYb'\x0001g\x0010Lè¥Ò1Ã\x000b¢¾\x000e®Þí\x001a®¯¾¶÷áí¯~eP@OºÛ"
³`BëeÕò¢p\x0010L¤·w\x0013Â»þÝÚb\x0007\x0002ØÑI¨e;\x001a>\x0004Ä5ØWîB\x001c8µ@\x0017oä`¼ìûO\x0004m3\x000c¦)¨Ìä
03ÑPc"·AÑ«µ\x001bV{ÒK\x0016ûz\x0011×y%EÏ8\x001b[®5Ô^«\x0006îÐ]YÁñKX«]=P{\x000cõ` ÚHÊy­A#yYvÏLÇÏ|\x0000\x0008ñ!¦Ø+\x0010j¾\x0011uõ6\x0008ärSï}q\x0002DnÀxU9ÝU{·«'ßhg\x0003\x001a;àDpØM«\x001d\x0010Rû(±ï[þGj@\x000bø Æ,\x001f}\x001bý°aÛþÐ\x000fæSñ:Õh\x001eùÓY2Kã\x0005ê@[sz
çÁ\x001c\x001aÿ¬\x0018\x001d\x0017\x0001;­Fáï\x0002\x000c\x0000R\x0001I
endstream
endobj
142 0 obj
<</BitsPerComponent 8/ColorSpace 257 0 R/Filter/DCTDecode/Height 393/Intent/RelativeColorimetric/Length 993/Name/X/Subtype/Image/Type/XObject/Width 2>>stream
ÿØÿî\x0000\x000eAdobe\x0000d\x0000\x0000\x0000\x0000\x0001ÿÛ\x0000Å\x0000\x0012\x000e\x000e\x000e\x000e\x000e\x0015\x000e\x000e\x0015\x001b\x0012\x0012\x0012\x0014\x001a\x0019\x0016\x0016\x0019\x001a\x001e\x0017\x0019!!\x001c\x001e#\x001e#!,#\x001e#!.333.!>BBBB>DDDDDDDDDDDDDDD\x0001\x0014\x0011\x0011\x0015\x0011\x0014\x0013\x0011\x0015\x0019\x0018\x0013\x0014\x0013\x0016\x001d"\x001a\x001a\x001a\x001d!\x001b\x001d"\x001d\x001b!# #$$# #$$$$$$$,,,,,,44444====DDDDDD\x0002\x0014\x0011\x0011\x0015\x0011\x0014\x0013\x0011\x0015\x0019\x0018\x0013\x0014\x0013\x0016\x001d"\x001a\x001a\x001a\x001d!\x001b\x001d"\x001d\x001b!# #$$# #$$$$$$$,,,,,,44444====DDDDDDÿÝ\x0000\x0004\x0000\x0001ÿÀ\x0000\x0011\x0008\x0001\x0000\x0002\x0003\x0000"\x0000\x0001\x0011\x0001\x0002\x0011\x0002ÿÄ\x0001¢\x0000\x0001\x0000\x0001\x0005\x0000\x0002\x0003\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0006\x0001\x0002\x0003\x0004\x0005\x0007\x0008	
\x000b\x0001\x0000\x0003\x0000\x0002\x0000\x0007\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x000b\x0010\x0000\x0001\x0001\x0002\x0004\x0003\x0005\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0011Q\x0002\x0012\x0013\x0014\x0003\x0015R\x0004#a¡\x0005\x0006\x0007\x0008	
\x0016\x0017\x0018\x0019\x001a!"$%&'()*123456789:ABCDEFGHIJSTUVWXYZbcdefghijqrstuvwxyz¢£¤¥¦§¨©ª±²³´µ¶·¸¹ºÁÂÃÄÅÆÇÈÉÊÑÒÓÔÕÖ×ØÙÚáâãäåæçèéêðñòóôõö÷øùú\x0011\x0000\x0001\x0000\x0000\x0004\x0000\x0002\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0001\x0011\x0012!\x0013Q\x0002\x0003\x0004\x0005\x0006\x0007\x0008	
\x0014\x0015\x0016\x0017\x0018\x0019\x001a"#$%&'()*123456789:ABCDEFGHIJRSTUVWXYZabcdefghijqrstuvwxyz¡¢£¤¥¦§¨©ª±²³´µ¶·¸¹ºÁÂÃÄÅÆÇÈÉÊÑÒÓÔÕÖ×ØÙÚáâãäåæçèéêðñòóôõö÷øùúÿÚ\x0000\x000c\x0003\x0000\x0000\x0001\x0011\x0002\x0011\x0000?\x0000Ù¦P^)\x0017é²¸MÄ©-XÿÐÙ	Â$'\x001d9\x0001 R¡$\x0000ÿÑ\x0000\x0004\x0000ÿÒ\x0002 @\x0000ÿÓ\x0004\x0000ÿÔ\x0004\x0000ÿÕ\x0000\x0004\x0000ÿÖ\x0002FA\x0000ÿ×èÓ\x0018\x000f\x0014Æ\x0003È¼\x0019ê$èÏR\x0015\x0014¥\x0010ÿÐ¤	\x00142GA\x001d
uÍÿÑË$I\x000b%à¼KÁys2`ÿÒÒT¶h$àÕ-\x0018%UÂU\	 	¢\x0000ÿÓáN\x0012ÀN\x0012Àº»©µ\x0015ÝM¨ÀÿÔÆQ\x0019K#A\x0011 \x0000ÿÕÅQ\x0015I½(¬õ()Eg©BXD\x0018¤ÿÖèSZ\x0013ÐSZ\x0013Ð±\x0003\x0010)pÿ×ÎDäÔ\x0003H\x0000ÿÐ00É\x0015DU\x001a`\x0000ÿÑà1\x0003\x0010£CH(ÿÒÖPÿÓ´4èLUÂb®%!¦\x0000ÿÔÞ#Ù\x001ct" HÿÕ	\x0000ÿÖ00½$ÿ×\x0002d\x0000ÿÙ
endstream
endobj
143 0 obj
<</ArtBox[0.0 0.0 595.276 841.89]/BleedBox[0.0 0.0 595.276 841.89]/Contents 144 0 R/CropBox[0.0 0.0 595.276 841.89]/Group 153 0 R/MediaBox[0.0 0.0 595.276 841.89]/Parent 250 0 R/Resources<</ColorSpace<</CS0 257 0 R>>/ExtGState<</GS0 258 0 R/GS1 200 0 R/GS2 227 0 R/GS3 226 0 R>>/Font<</T1_0 219 0 R/T1_1 214 0 R>>/ProcSet[/PDF/Text/ImageC]/Properties<</MC0 146 0 R/MC1 148 0 R>>/XObject<</Fm0 224 0 R/Fm1 221 0 R/Im0 150 0 R/Im1 152 0 R>>>>/Rotate 0/TrimBox[0.0 0.0 595.276 841.89]/Type/Page>>
endobj
144 0 obj
<</Filter/FlateDecode/Length 1994>>stream
HÌW_oã6\x0012×§à£}\x0019\x0014)	X,°µã;\x001f6M6qÑúpÐJJ\x000b[r,)í~ûÎ%Ù½mïpgÃDó~3óâ]ÿýÑ'Ïw=ßødVz¼\x001fÞõ\x0014\x0016Ó0ó%UZtûìß>,.¼O}¸I½þJ\x0018#>|á\x0012R¦ a\x0014S\x0019I²Üx#\x0011_½¥÷â\x0001!øáA<\x0005åìÓXD@-\x0008\x0018þÐ²~!.cÊ\x0002? ¡­3n<|³ñ\x0018"\x0002^\x0007dª@á£]o\x001fí^&©à\x0011<
àJ8ü\x0012÷4P!á \x0001{Ï1
Â\x0010O9ú\x000b\x0008@U»\x0010R\x0005wÝ\x0002\x000fh¨\x0018áÊÀ,\x0008F#¡zL`!\x0008@
N\x0003_àBÀ©/%.iís\x0000g9%2'@\x000c\x0015\x0010BÞ³ÑÜ.\x0008 \x0015\x0011?R¬'Åq*­ä 4bXapÈÈÁ\x0004
¥"öjöDKT|k\x001e\x0011l@¾hé\x0000t\x0007®J#Ö\x0017ïÉF\x0010D®äq®\x0004.6 z.\x0000ñ.x)ªb\x001eP¢ö¾\x001ba\x0003\x00067\x0011\x0010õ6	Ùmú®\x001f·IñîÝõ´nõ2ÿ­~7¿Ï}_Iß\x000fÅû÷ïÉ\x000f³)ñF7&\x0014oñ¬¸\x0014+_(ü§2_ÜQ¹]tT¦gO\x001cN"\x0005åîYGåánþð¡#ôãô\x001fçQc\x0016\x0003¥Î#8Ó¡Bw\x001f{*ÍÎËÁ,üH\x0016pP\x0014bÆ.3oôañÐ\x0017¬5ô\x0002W­¤\x0010&2À`HÃÿ6XÞb\x001e\x0018\x0005:{Ø.6x\x0015/\x0010\x001b¿s¸?º\x001bÿkùÏ½/K/T:ÙïFVÃ«Dv\x0002\x0012De0Ñ'\x0013\x000eÙ\x0015å\x000cD¹ß9\x001fÛ²Êwd%\x0002dyE6:µë¼¨Í]¾µ"ovÕU·sïª²(àn%$[ú¹À\x001bxÎ\x001a²IÌ¡ô\x000b.Áv²^qÎÇ\x0001ÐÙlaï\x0015IÐ\x0012¯cáòt\x000c\x0001æG« °Â	\x000bP °Û¼!eC¶IÄ^ÀH\x001a|'Ód,)\x001bÕº,\x0015³|\x001a3 Yá¥Q¾õ:Ç+#tÖúU×c&G(YÕ¦H×FÒ¼\x0000Ñu+\x0018\x0017V[#»Þ$Ï9Éð¶)rò\x0004Üä()¬Ð{ü\x0018MÐ1}Ó³\x0010×\x0003%Ò/ºÊANjØÆ\dìS d\x0005.S\x0014µ]B.æ&/ª\x001cZÀ¡+Ò\x0014v}Sf@Á_»mH-EÅÊ¢ÜèÆ-;çÕÉçÖ\x000eíùªsA©w'<h»¿#éÌÚ}¸ÐwÖ±£ò\x001aÜ¿]ë\x0014ù\x0011xB5vÚ\ê¤0bîß\x001a»
øÒz\x0012Ã%\x0001_ïÖÞÒÆzÍn\x001cû#êBåtªöº>¾¿c\x0000\x0019\x0006B¾Ï5Ð) 
Ê\x0008è4º¿{è2oùgÒõ§\x000bÜà\x001ep^@½Ó¬ÎÃ­v>î\x000fA b\x0007&MÏ£mg%(Ùª\x0005×=5¨ÊA\x000b¹Ó\x000bæ\x0007à9ZÜõªÏ\x001fC8!1\x0016¡E±ÚÃ\\x0006\x0001ùq\x001cøV+(\x0013 &ÄR¦]&¸2y×Fß\x0016QCcf¹T0\x0005Ø0!Ûì\x0000\x001e¾â\x00051®J{ÁÜÈt\x00102oC\x0016\x000e\x0001ù|\x001cÓ\x0018Øé\x000còÐàVË¿HÖß0	«v!½'þ	t´i¿Ù&\x0016%U6èIb\H*Dm+ò×¼6Hº×ae¤*×:k±ÀHO	\x001a\x0012AË\x0012zÕÚ®2oA¡d»mc\x0005ùÚÁ\x0005ªÁÙ±ø\x0000HOÖ\x0011eYÕEW\x001ej\x000b\x001fU¾\x0001+\x000e%Ü£xë^r{Z¯ÇÁ©Å\x0001!®\x0006>Ü>.Vã+²÷ssÞMf\x001aÇ\x0016>b<V£C-;\x0001 ÔB ='Ï¦JQ25UÍAeU Sk4\x0004:\x0015CjÝ\x000bÙkaÀ84Â«N\x000cîB!¸pôåx\x000e\x0010uª·{/C§ÉV×ÉdIQ\x001dÇ\x000b9Ôë[[6ªÿ,h\x0007ÁQ³7\x0000íY¿Õû¸×{>,\x000e\x001b­ó\x0000¦z\x00006ÿ_àwD#\x001eýßá÷\x0005MN«¿¼pj6dxÛcøß0wUÓýJ0v9¤úUg^\x0018y\x0005Æ¾±ï\x0005óÎûMÏmµî¾¦óÜwWKÛN8§!ßQ.IbzÌ\x0003\x0000\x000b×¾æër»5]3tz®ó´Ý¶>%\x0006\x0000T
Á\x001b°£Ä\x0000ð`\x0018Éì\x0006Á\x0006Þ\x001aÆÊb\x0010\x001dck}qDÉã\x0007qýl¾³u½úc
¢ì©ÁtsËA\x001d´eÜ\x0005ë¶\x0007SÍ÷Ì4à\x0003,ËæÝ\x001bÆ¶C!ÿÍuýe;` ¶v¸4óUÖ\èó¢\x001e\x000ckLÇvïú\x001cËÞ\x0015	(\x001a«¼`Ê}-­ò¤éL½Ãq_±\x001aqé£k6I» «pïjÜZ\x0000BÈS\x0010òuljÚ~0h(ÑºÐµÂæ\x000eµÞtã¢\x0012\x0006Yæû+HJì¯ÀÃ5
¯Û^\x0004ô.Üc\x000eAýDíßh\x0017÷|-n(Y¬1\x000c]·¦íSõáðe\x0002è3Ò2Qj¢G\x0014êÙÓÒï\x0011M\x0007uÄØæ!L^\x000cM\x000c°~í\x000c6²uýfé]ß¯4Ïîgsr};õ-Xa1g{LâI\x0008R"V4G\x0000fìrïÉ{9ýâgRÀ+8+ðl\x0000§ä¡!7`×°\x0006\BMû\x0008&«\x0008ÖÓw½ØødVz,P\x000e%eVÒOã
\x001e
¥\x0003ñÎ¼\x001e
ÉÃÆæ\x0013:!CHxøÄ\x0008©¨T<"A&¡¤<d*\x000c¬'ã'ïw\x0001\x0006\x0000¼¬à8
endstream
endobj
145 0 obj
<</Length 707/Subtype/XML/Type/Metadata>>stream
<?xpacket begin="ï»¿" id="W5M0MpCehiHzreSzNTczkc9d"?>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/guide-juridique-et-fiscal.html](https://www.associations.gouv.fr/guide-juridique-et-fiscal.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/png/lfse-15laureats-2.png](https://www.associations.gouv.fr/IMG/png/lfse-15laureats-2.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=öÕ\x0008Ü;ÕSÉÞ´¦\x0004VcY\x0002¨:&5Z5\x000eY*õ-Ød¼6ØÇÆ\x0012;û\x0010Ì\x0010¨8\x0000à»Ä S¥Cx.°D¨\x0002ïì[£\x001e°[$>á\x000eC\x000b\x0008Ï\x001d5\x0000£dvNÙ(\x0004,ö!0[À!\x000102µ¬QìöÞ®G¢\x0012(¹\x0017¶97\x0007Ãd¦\x00081NþáÞÓ¥ÙÉ¹FG»­%ä)/®S¥\x0011rÞûTÔ93bV\x0018ý-á
wNZÙÐh{§xè]PÊ\x0013ÕL½¹-;¶J¯\x0019õ\x0014ûBÁ'B\x000e³á¼Õ\x0008?#JhA\x000exjôûÃ\x001füQùùüØ{Ã8AÈ«\x0011\x0008b\x0008I±\x001d"pÃÉ=ò
\x001d3ÒÆYnç°Â\x0005\x0007ª\x0013¤Û\x0010½À/\x0011°\x0010¼üþ¦ÚE
f¾²DY5¯âag~=Àå[é!`Å7â¬«ìðI7iGéÅsY¢3áýVØÙ\x000fö§\x001a\x000e\x000ffQÌ:e\x001fL\x000e¥oÜ]aNû±~*Hûo\x0008¿BÐ¯\x0005YæûàWI?Vlªô@G>\x0003\x001d=@>\x0006P¶\x0013Þ©w\x00020\x0018©\x000b"±'\x0004å\x0010Ù\x001f\x0015íH×V7|½BôRQÏÎ<EüÔ"ñ\x0006
e\x000e¡?Zkc¹YZk\x001båñ£g¦á8lD\x001eI\x001fZ\x0019Ó\x000böÓUÂ4·P\x0011\x001fÂ!t\x0018í^dQ~Ì'èÏê~Å74PñEÈ\x0012°h¯AO¶7``"¶ch\x0000\x000cëÛd
>_©¹Ç{;Õ\x0012!\x0019Jpêþ\x0013\x0006 Äë\x0005\x000fÿLÅ á\x0019\x000bÁ­\x0018fT¤:\ïíèT#/\x0010í:ó\x0017Si,'ÆE§1[\x0001\x0010Wª\x00111Ä¤»M6Wù\x0018çéa\x0015ù\x001d#9ÌÜ!\x0013î9¥y¥\x000e\x001caÂ{°\x0010°ØÅ/DL¤cü\x00189À\x0003\x0004\x0011e¯ò]³K¨#?c¿
ÔãH3z=?w@n0`ê\x0018\x0001kV\x0010\x001d+ûUx¶`¥¹\^½,¯¿ú²t$pJ>r-Ü ­³l$\x0001k ÁêRÊ¬\x0015V9víý!jhäÑ;\x001bñy&g^f?#AG¤×WRÜ{Å~.öÅà?òì>OM\x001eéDµ±à\x0005­È3W\x0014 ¯ªÉ!Xt ª3¹s©(:ËC-1õµ5\x000b,¥±Æ¸©êp\x001aþ&ñvÇ\x000fJyN\x001eë²°4[66WËc\x001e-ÝÙ\x0000Ù\x0014C\x0012\x0012ý\x000cÔ\x000eúvé2Ðhy/ã©\x0004
\x0004G:¥V£Q\x001aÂÃâ¼Ò\x0000\x0007²Ù\x001c°Dù(·2$ÁJ\x0002¤pÌ7\x00038É(¼\s\x0000\x0005ï:öBÀ\x0000ä\x001f¡=]\x0008W¤±²$¡Lé1£Çq~ßþ¬\x0002DQE\x0007¢\x0005ãQ?àÑ3Y¢SöÚñFV¥ý4ÓíÝ=	ä[[é\x0011°¸ªÁB\x0018f´\x0010fr\x0006\x000bA÷R\x0002\x001b{8O$¼\x000f.ÛJ7:o\x0002ð¨ªd\x001e×\x0004«\x001b1Á\x0005w\x0010ÐÀ\x0002\x0017»*ÿÞE\x0011°\c¾\x0000ç÷¸ú#Îzýcgþ¢<+x\x0007®¾y]
Ú\x001fïýì§?)ø¯þ |ùÅg^¥^¸Ù+/\x000bVÂ\x0008\x000f'\x0000\x001f2 Æ¡{óO)\x0007q³P£zcÖ\x000cH?ìÝÂÍ\x0002Â\x0006_\x000eÈeÁRáüÐ¸Ì\x0000yÈ¼\x0000Ð>KI	ëÔÃtÀù\x000cNÆéº\x0008ø¯ÜäG^¨²tOHûI0~îqûºð«~;Ü÷o~Ä\x0002W¶2*ê
`da q^Ç­4\x0004õI î<-è\x0007ìU¿\x0008EÔ#³ãðOfx½\x0001º§nÍ[P¯O2Ä·yµâm\x000fomm«ÙSüÌ*é.aò\x001b\x0018å}\x0004é\x0007=U\x0002ü½\x0016\x000f\x0003&ñ1\x000eµÂmJaÆ+nì]e9ðøèÐ\x0013AÌPÍ©Ì?ÞÖ$\x0004FÔD`)<£×TµDXÏ\x0014IIsOGÂÑ¨°\x001cë$\x0014Ë\x0017Ø¨=»Ñ7º¸êHÅ¯+3\x0017Fo}ötqßN»íQ<\x001bm#\x000e6&ç¨.Òô\x0019EË\x0010ÊL\x0010\x0015~Þ¦B©o9\x0011!f f\x001b\x000cGJ\x001d9K'\x0012(Ø?\x0016£ªL
÷~PY2¯Q%ÖªÛ×#Íõ°©§[ÝÿÛ NÝ\7Ódcí¬\x0018vu\x0012JY\x000bfwv··JK
èóQÎ^¿B¤/«ê\ç§Ë®êO£i¡\x0008óJ¸\x0004CncB\x0012\x0002\x0007#[\x0002¹n`N7Ë	)éËó\rÙ(;[\x001begs­´8)·\x00147;³ÜÃ\x001f\x001bÇý\x0008F.ÂW¼b\x00131DLK@\x0017þûtDJ6"ÈGÇÄ¤8¹÷\x000b9¹Psu]é­¬\x0015.ø$-êÜ\x0018\x0011^1ð3a\x000eÚ½k^Õ¼¿9 3ÂÙÚX+O\x001eïÝMá\x0017áN¾Uþ+\x0004«t\x001emæø=W+°ÁOT°<¨X¹Í½¯ÇP\x001dæ\x000c3v\x001ciQ:>Y£üD>¢ÌÌ\x0016kç	AJºÓð\x0003þ\x0011Ð`

	\x0015Ì­°1U\x001d3ÏáPß\x0008°tÔª%ár*.Ù!<!\x001cùbKÁ%\x000cvûü|£ÌKXãd"K\x001b\x0012°äG,Å\x0002O^Ãà¨Cµc\x000bXo~Ù,zzzT.¯;²\x001a/\x0011i3 n7U)´÷swüKCQKÔ/Â\x001d\x001de`&«!,® /BCNU£6H9à5à\x0007\x001dw%äåRFø|+\x001fÔ#Û*¸âæõ\x000b®`øQù×ø¯Ê\x0017jáyyqN\x0003¸\x0013\x000f,óIeBpb@ÊÃÉ£'N¤\x0010¬¸{\x000c{\x0004(\x0004ºÅÆRYZnÈAÑ\x0013\x0011¾\x0018¤\x0012'Ë´\x0007·	²f<!0±\x001f{øöõ*Â#þ\x001cN
 \x001e/}úKÙ«ð\x001dm²Ò\x001afý\x0000¸|zà#¿ÞÐ.{·SjÂþå2Ê\x0007í.þØ\x0002z£¼Îùbf­Òõ\x0017+$ î*Ã\x0011O\x0005¸l¦©ÚüÓ\x0004Êþ\x0010LËq])©jäÇ¸\x0013\x000eõ\x0011ßr2æeù'u\x001f
wpì/ù\x0003LoU\x001b¥þÈû\x001c\x0003\x0011jWføÄjk½¬¯oøt"ñXbs`~­\x0017;\x0015Ò\x000e{x\x0006´\x0005_O¬olí=
x7D\x001b±Ìª÷Ñ*¢\x001aë¨ð\x000fL	@uÇîî7ñ\_Ë,9\x0015,o;\x000brJ[\x0003@+Vß.5Ðå\x00084\x0017l3[å	$ñ,½Ì´#ú¢±bi0ÍÂ\x0003¾*eH\x001dP\x0001ÑY\x0001	HêDÜ1)w©\x0000y³ß²Wv\x001bpÔ±RA¹&K\ìÇj_0=)ûûûååË¾ÔoFc01B¨2ò	c¬+â»wg==+2|ß¯ã\x0017#V\x001fåòE\x0019Rc	Èíx
\x00085Ä\x0003P7Ot¿_\x0006\x001ek\x001bvä}NÄ2K'!;¾ñA£ZpBã\x0000¼,¿VåéúzÙ^nê[LT\x001dï,\x0002\x0004\x0000p\x0005Ü±«\x0011qº¯¡úæX·þ\x0018æå­È+:¡9ïÁbc#\x000cÞ:ÿE5ÚEÅ¿À½*Í²¤QÒ¾ê\x0014å\x000fÍµ\x0010
:2¥ÁÌÌ<Ë¢»%ÑVc¥H6Î/H @hihÄÅrÝfÙ\[\x001fujÐ
BEÒû7«\x000bÊ­\x0018èlLð³°\x000b*#iù¸²Rò`Dþ¡iÞ\x0003ìJ¸âÎ+_Ô+ OÔ\x0007á`\x0013ºgP©\x0018Ç ÅÒÊ>\x000f®\x0015?1±®zYmé[åö)Cµ¿yö),õ°"ûUù_Q¸%f®Tv®\x000cà\x0014¢
n\\x0000Tãê<\_±¼\x0005N®Ú\x000f\x0003\x0011Æ\x001e«`Ë¦ñ\x0016åf¹v£èßª½É\x001c¸&ø&L«Ã7©kR1t§-S7,Å\x000c:$\x000f\ÆX\x0012 =x\x0008ôPWçPÉcP@M=qPwð6f!aº<iôù'\x001fßÿþ?åÿùÿøÇbÔ\x0007e{c]pñö\x0003ê7FÂ\x0008\x0012c^Ê(öY¹þE',s¸ §\x001eÂ\x0015y§nÀ#<\x00199Ê_tði~­(7JÕUá= è)4í_2\x0010'a¬¬ÀÕ\x0018ü­ü{\x0000ª\x0016ÿ©ê~3þi¿ûTB=ìd<|Nùÿ\x0000.\x0014UÆcà0¾-Ø
Ü>«¶;õäYþ\x001a\x0006Ó¾^õúÆáilp^×e;Ii×ë#ë\x000bw\x0019869mÎ`­!þKr\x001e\x0004	oÄ·ãuÛÃâ\x001eÝP3cÊJÖDY)Úö5W/ø5Pð\x000cÊuyÅ\x000csOvjobÌqhFf4Øà$¼"Ë°wyvNå³Ð±\x0006;÷}$\x001c
@µ\x0012Pld¥áÐàÜ6\x0012H&
â^547G%$§ ~ÜÃ.üNº#ÔÜº#Fz\x001c0\x0012c93\x000c;[;*hìC B\x001c£9\x0006\x0005\x0013ã«*0 Ð±N\x0005ºdUEÚl¶*aqqEÇ2»r~z"!ïU¹hÉ]~UF:Aü1{ÅHÒå®j,\x0006SÑ½à\x001f=ÍõoKøR>öÃF\x001a>uç¼Èêr\x001e	§t1{\x0003´ÃDü1D\x0019çÃi:JUáóúà\x0012¦÷\x0019Ý3³0£!å³½GåÉæv¹éuËËZ­¯¿ôg¾Wþêÿ\x000bå½ÇOËUO£åö\x0008l±\«nf\x0017¥T©Ì´°a=6X#¼^úÎªåù²,û¦ªlk­UÞyú¸<{òH\x0002O«4%0qWÑÂBlÖ\x001a
)×Ê\x0013#¤\x000bnîÇr$#jeWcìW\x001eÍ+ÇE$bfAs¿UÃ§ä·¼D¿­õÍÒl­æògV\x0011gÖÒ{0à(FOõQT 7ýÊ|;#3Ï|B\x001bÌ\x0014\x0001±\x000c¹³½%ÁgÍ\x0002\x0014ëù,\x0015q¢¿ó³Âk\x0001Ä\x0001í±ìÉ\x0006vf°Õ×&t:\x000e I}³¬5/<Ó©rµÄ<Ì¼ÿÕhp²\x0004P6²W:Sü\x0015EYðZ^ÇÑ#\x000e\x0015D<hNBì\x0007\x001aÌÄ@>¾ÇHßqÊ+«Ô.[»)\x000f\x0008V´=ßÖ-3{)+ÂosµÌ)ÞÛ\x0005	
à¥Ç%á;ÚlÐ¤êôJ*F¹\x0011þâDåïÉ¯p\x0007Ný'o$\x0006âõoºvØ{Tü(\x000eêSõºÊÆ1õãÖ#o,	³\x001cÊ¦wNÂJ|8B©0Î\x0016´\x001eÂÚÂà \x001b\x000bß0bî¦b/\x00063òæ¢ö³ò¯~ÿ,\x001fÿü§ù¦¼ÿÎsÕÁ|9cV\LÛB¢f©\x0005\x001a\x0018H\x0000d_U§ÇCÎ±÷
Å`ìóY\x0017Ì ÍÁM
>\x000fý¹££ýéz¤þé\x0004)\x001ffK\x0004·¸ÇH!È§¥HÚ\x0018åc©\x0012@#=¼0(¦.¢3ö¡û\x0008Ï7\x001dÌòÏòSvÞ=dàÌÛÌäÙ^ùâr_â¹d&[þ9]Ö\x001dtåF^W¡\x0006òÙÙä[a9ìi»Ñ6C¯Qxt)Ú\x000eé¦ÕøÜ¾õqd<	|\x0003u;§SùKáâß\x001a¨aµº²ue¾}l\x000f®É32ä\x001d[Q¦è#¡qaÂmÙH\x0000ÃþÕM
èân-V\x0016$Ð+\x000cí
_ÃñP?KfW#È\x0000üë|¶¶vË§ÏËÖæ®\x0006%rv\x0016Ût"£Ù_{`§°|SOwtÙÈõ=VÄ5þÎê8TgL"8¬òÇ$\x0002§Ð-ÜE;`oëÉña98ÜW»i«Oì«\x001c´yüÐÿ+B©àg\x001a2	ã\x000fÅpE\x001a\x0008[>÷dïý\x0010n`¨&Xe0
\x0000¢ª\V
f\x001dL\x0006\x0002Þf\x001eÙU\x0019£±RÉHËDç\x000b6x*[béüÍØ©FWFZ¾\x0015\x000f1\x0011_"üÑU`¥·\x0010ÌLíµ%X±±»ÓiûÛÇ)Ó¹­Ò«þ`j¶]Â}æàma\x001e?¿ÓJ\x0006nÓÜÏ²Ä+´ÓyÎ\x0014	²"è½­½²ÙjþE¹<>*ÖVÊÞÊri©àT\x001a{x\x0018
·%,t¯ÂL\x001d'Ù9-p µ8§\x0006(f»Ñ\*Ow7Ê{Ï\x001eo¿û¬¼ûìqÙ\x0010`ÍÔ¬Dw×äP.ú\x0012:xòãô¢+\x0001ûV#ø«Òó@\x001a­K\x0018¡\x0003`¿W_f¡ê§<\x0010\x0010\x0008¸`ô\x001a:Qãáù\x0010Fbß\x0010¥\x0006\x0010@Dxêàca* n¦óªßh\x001fébúUô\=B\x0002QûÀ\x0007*³\x0014Ëàlì³\x001c>¼¹_bS´\x0018Òêu.ÊÅÙ©\x0005\x0011.cµ\x0000Hg\x0006ý«nÔÄËPÉ\x000c%Uö\x0010ÌToÜãæå<:eò\x000b\x000eÀÌÌ\x000c"èø2ÜE÷¬ú)¨ý÷¥\x0006äKñ±`ÁTiÞTWÅM{ñó(0TçiÁyB!ÀrÑ(\x001bÈg¼¹ÎÓt´-\x0006!
¯x@\x0014¾Y\x001ec
¾Ó=W>zÊ\x0013¢ñ\x0018ê4û\x0010ý\x001a*ç7Ã  \x0002¾ákð\x0019K}pBÝÑº)«y_Å\x001fB.Á­ø#Êí*pé4 ØòÀ`¥îý/Ê¿üß/þâg¢±â=xk«\x001aÄÉ\x000f\x0003Gx\x0002;~â¡\x001eY\x000eäJb&4¡-¾\x0011pã|3ó§®\x0018d°­\x000c?Ì~Yø¡mÉ?KÌ:°¤\x0008=à'Ó¡<\x0008ÈèN§RðCðâ>\x0001\x000c¿Â(	ïÂGKed @9Hü=þ¼¼ûî»\x0016î\x0012È\x000f\x0003hü\x0010\x000fB\x001eã·]å/!íÓm¶êSÊËÌÊ
ÿÞÜ_él¶·@Ia\x0014±Z¿Eòîzp\x000fdÜ\x0000i[\x0019\x0003dñÍ<%\x0010nýÿPËúT {ég_ú\x0000 ýey\x0018À\x0011rÂx65Ê\x001d´!Ü\x001fá<âIz!ÞªÞT?XÀ£¸D|±¡ö !\x000bF¹æÁ\x0003\x001b·;üO×-`>©ñ7å±Ü _Ò¡Ýã\x001b
(+ÞÄ\x000c\x0015\x001d_\p\x000bB,ãûq}3/ÞIñ'ÛU4åï±n¨ô¹ï¼ÿ;\x001fÁ\x0000cÔ¦)à\x001d\x0015Ä\x0016\x0011)2\x0011\x00193`vÒÈs\x00051Ô¿Ó|ÇNÑ;M¥\x0005ÁShöix6pR\x00110EFðj1òp\x0015£lr\x001cõGELWÎ\x000bþ¦\x000e3½¹V`¡"ñ¨S×([Ë^A0\x0013Õ¢Ä\x0014B_*J8­	ßo\x00008$\x0001*Jª§ÙMºG9#
ôIõ\x0010ø\x0014\x0019Ô%ÄÏ/Àh¹Ý|¹ìíìÍær¹°y}~\êD:G¯Ëg?ûrôú@ñÂÄ\x0016¼)·OÇpÅ»yÜ\x0002?[V4:]\x0012²\x001a\x001a¡n4\x0017Ë³½íòî]\x000bV\x001f<Z?Ù+Û\x001a¹³|ÅåCI\x000b}©NXº\x0012ªº|_ÞNÿ²\x001c¶ËY\x0007¡¤\x001f³Y\x0003	V´¢£P_u+º@` ¸©z(u©N]½}ScæêY1
)a«¢1á¦ÆÔ-4G\x0011\x0005ÑøèäØ\x0007h\x0002?Al#÷ð\x001bB\x000bñ@\x000b1-K±vÏITèÊ\x001bÒÕ\x0001yM§¨x|Y¹\x001dGîñÃs9\Á\x001e-Òb\x0016\x0002@B¤ì\x0017½Ër1 Âé>	 ]f7°SÜû\x0012DÁ\x000fBÓ:b²KµcN{\x000e[UBéªÓïÊ__ùbÊbÊEx
çR\x000cìa[\x0019R;\x0000/ \x0010^yl¹©:]lª-7ßeyCx\x0001çRà\x0004dI!`±Y¼nï\|G´S	XuzMsÝn\x001a¨öb´h³\x0014
¹2~I[~È\x0007c\x0001f^\x0010:x¤6ÊãFeå//\x0005SF¿BèOÑqK Ä?\x00113°]\x0010Ýs
F_åúñ\x000fÿµ÷\qëÖúZÙÝÙÒ(}ÖÂ\x00157ð\x0019	àtþ1\x000eT\x0006\x0004]ß°®¸\x001f\x0017\x001añÕ\x0018Ê\x0003L7ß|iªÂ#x1;pF¼\x0008.Ä\x0007í Q^5f9¹Â­\x0017A³Êºðº¶¾îòAÐ%iã\x0001\x0014ü¡¨oÅY×-ÄÉc\x0003![~¸)\x001fÕ\x0010=l(^:âó³3ï\x0013Ë¥MÂ"\x0008W\x000bHÌcâU\x001dÄ¬R$NºùnÞx])\x0004\x0000fW¨Ð±cÖelÆ<Ò¿ÄLXÍqWeºWÐ\x0006jTrÜõ§t±\x0007ên¿.\x0010+|c5¦Ýiüë'Te\x0017\x001cJfñ\x0004N\x001dCÛÌ®àÚø\x0012î?aÍÂÕÎÎg°°ÏñðFï±$pD\x0012|\x0019Çt´\x000fÅAÌ` ×Z]/;e}}Ç«
ÄO\x001e\x001fR\x000f\x0005ÔõIs¥àÿwìH£²K7#^<¡º\x0000YEVv\x0019\x0010w}ºùìôXm¢#Kr.÷J\x000e0Èr3Gó\x0019fô¹¿ü\x0017ÏÜêÐ\x0010¦ÜØ\x0003Áõ­ñ9Òù!ì@& ¼ÉDêß@~×íÙ¸L\x0002Q11\x0001Sà¤Â\x0016§\x000c4:bmH¢ÌrTFCu±A\x0002:ù¸«ÇÔ?iÒ	Nèçú)C:\x0014F{]	Wûå§+ú\x001d	 ße«:\x0008\x0001å·^áÃI¾+ ËÿvU\x0005\x0010ðP÷0Í]¦°ôþ¦)0ÄE\x0005àjf¾!baSøJy²û¨l¬,!oÅ½þ²\wNËùÁ«r¤ÑùÁÁ¾\x0002(²¹¾*zeö¥ÅK2\RÕ4æoËÞÆª\x0005«?û½ï÷>)ïHÐÚÙX+ëÍgÁHNäËW~ÖåãO¿*¿øüòÙ¯ËW¯ö¥Ëý£rpz^NÚåDi^p B\x0018Â\x0003KkjÔ,%^©Ñ\«<7ªkæe ª¿Uã\x0015Ý,4ef¶^öÁ\x001bF8`
N&;T\x0014ü\x0011\x001aú4ûT<9r{«xÝfB8CÙ¯þè\x0018=x%Ë¹4ä!¤FF,Ïä]+\x0008bÌhñæ\x001f³]øgé\x0017êÉ7¤®\x0004§S	¨¶\x0004´ÎàZæ\x0005ÐN9=ïú^ºs/7õ-Hq/Ùèº}1°?üK?Sø\x000båÙ0\x00041SðC\x0002E¤Çþ ¡êÈ\x00030Ê®21äÎ1\x0004O\x0004ØFsMmuC)y6=5;C\x0007\x000fÞ8@BûHÈóLÎ¯©èöÚq ûÀ\x001a@$d\x001d½MU¾Ã\}[É/Ë ð\x000bf,ñ³"áûÐmc\x00065xü
×8\x0011ãY&t:ÙèPXb\x000eC\x0002LT²÷%`.\x000fý£?üfÎk«¹ÚÞÜ°ð\x0002Oi«ÞA	\x001d
q!0sÕOß"\®¯b&Hñ\x00063R\x0008MÌ|Q<u8DX\x001fôËM%|Q^\x000bTÙË2\x0002ê\x0010Zãù$üÞ{ï=\x000b\x0008=Ìu$Ô{_ZÕi²Ø'\x001bâ\x0004ßÄGÚuE\x001e¸¯m¥J1îííí²»»ëYWf<Ø\x001bÈL\x0002{ß\x00198 ï!XFÐY\x0008}ZÓÃ\x001d;©\x0010©ÐT)öºY©¼ÈãÑ\x0008Sè¾TXf»IùÐòÄ!\x001aT
\x0001eJ*r¦\x0010E\x000e,Ð)M\x0014ö¦«?-ø\x0015£~[Þ\x001er§Èð¥ÜNÿK]ßîß$·Ä³%0çÆvfÇs\x0006Òí¡*kOí/\x000c%?Â9´E\x001aðb6·Ó§sEOrÛ´Ýiêm0ò«ö\x001b\x0014\x0014ù\x000e\x0015¼»î~\x0017ô}\x0013i¨¸joWâÍ\x0017>Ý|~~ªvÓq[ð)¦\x0012ü%ð£_6íø\x0015\x0007º\x001aANøû\x000fï¿øY\x001cîX¡ãHBr\x0003ád°iÌ©"\x0001N7\x001c\x0015Ü'ÌuöuwFö4V²M|~PÙäFd¯ùní1°9~IIÁè)\x001aÊI»\x0011*¢ª@XÞÕ]à)öÖ\x001b\x0004,5ZòÁ¾«£Ã×åT\x000còÚk¯X'\x0001>È3äS¤\x001b
0òA´¨ºÙ8KóT\x0015Dyoø)vu³\x0011g=
\x0001v\x0013Lk¬xlY7õ üÞ¨£Yj¶ÊÇOÊ\x0004¡>÷\x0014\x001dqð¼l¯.\x000f?|¯lïl«c0 |Q~\x0016$UÝ^÷Kñ\x0003ÅÜD~[Ö[Kå[ÏßüÖ{åÝ§ÌXµÊÚòbi©7â)\x001c\x001enæbQ±Íòúð¢\x001cõË\x000b	Z_½>(/÷OÊ\x0007ÊW\x0012°NÛ\x0012zÏx1@\x0002\x0016{±Ô¡°¬\x0002\x001d\x000cTd\x0003\x0004+µ\x0006b\x0000\x00035+½gh¡áÙ\x0017LTn
ï\x0019,ùñó&²´@eØÑ
w©°v(\x000be,Í/y\x0016\x0019\x000cøChVÌj­ÐA§-ZS§ÈÃé\SÀ~·\x001b	¾qùRB£: \x0010©ðº¼ÌÒ¸:w¥Ë²'3Tg\x0008Q\x0017\x0012¦$ uúW¥£8d]ÚýËrÑ\x001dXËýLfW\x001b÷W¡ø\x0006'ÒÏ-X
c\x0006L¸d\\x0010åËbéÐ%IÅ\x001b×¾8ÖÚ\x0001\x000bê¬9µDGí©ÊÄÌÕF¥kìuµ¸¸ZÍÆ\x001dcà\x000eA!L\x0008}\x000b çÐ\x0016#D¨a`ªªjÞ0[¿GE{VÜ\x000e\x0013~¡ùà_Ô±>\x0011\x0002 \x0000Þð
b\x0006KÂ è¼Ò¡Ø£Â\x001f&®$¬ p\x0011)v8°\x0015£wê«1^¿üÂW1ü\x001fü±7·ó¤Óc
(¸\x0016;Ê\x000e\x000e4p;²\x0010\x0005^UM!\x000e´r©\x0010³í¼T\x0018îÆ¡èÊ7½Ë\x000e¡\x0008\x0005¿Çýy\x0008¼ðp\x000b\x000bÊ\x0003ñ#\Ù¾¿óÝïßüÍßô÷W_}e+rrF\x0002\x0000\x0003à\x0007|G¢Ja#\x0015uböm9`òäñ£²½»í\x0013Ø¬\x0000¬iðõÁ\x0007ßòsLG\x0007¾íxÍ«¥ÓqÑ·\x0000Z*pfê\x000cA\x00081\x0013\x0015ß9SÅ\x0005ÂÌdÅV´±Ió\x0012mÓ\x0002Xø\x000b÷*ì\x0018\x000b}Y¶¤=`DÆ\x0003ù¾\x000bAm¿"üQÔó;
ÞæN/HÑðUÇ\x0001[EàiO\x001e=õD\x0007Â8n&(¹ÚÛÃêÏz¶CôH\x001b!¼Ã×xuWÂ÷ù\x0006uà>µó­*ýMõOI&ìÄ\x001bèePéN~Æ~ô\x001f5"CVbÚç'¾¢+¥8Ð7/o\x0016\x001cí]ºÿÆq,è\x0017jñòg³Üæþþßý?~äåç\¦\x0015Ï6¨ÉJÕzD^ÿfs.zÂ}f ¿ëö4b*.éWÍÂÅ@ÀZYÝ(;;»j\x0008<rÊ&LuRUz0ï(s\x00156\x0010W7Q¸ÀÀ¤`\x0015ÈadÍu÷\x001ei¶Õ\x00192ÕNN"ò \x001etâ\x000b=GÞµâ8o	ß®Þ\x000cP÷0iÒî
é/\x001bÌT%w?õ!<ÝÌª3W£ZimgOÖÒB¹8|Uæ.ÛeþºWv6å;\x001f¼[VÖÖÊ±\x0004Ó^·sñ/\x0019
×eIÔ¸¶²\îny9ðÝgÊZ\x0013qÂw\x0005\x0015¼aiÛòOÅ|Û\x0012
¤zê0Ô÷!\x001cõ¤³ïýA§\x0012¬X
\x001b^"HÑÑkT.å²*»ßÜ\x0005nÌÖ°Äy}6êà¸	&J\x0017Ï,ktt\x0018ÁL 96£\x0010pPÙTÜj­Zàg$âí½Ué¼¥µ¶¹Y67¶Ëôõ
F{ëÕé>f1òÎ-É \x0016®â%\x001bÇì^ÉNø`Ný,­UÌ\x0011j¸8-\u:¥Ýe\x0019\x0015Áê¶ô@Ê7°PÄe¯×µâ\x0005}PfÀQ8$TuäÖgÖ\x000c|©\x001eXbeÿ\x001aû¶Xjd³u\x001c\x001e`1fN|¡¯êå*:zz>öf02K T­®©ü{ÞÅ¡\x0019?B`B[VG/Á!\x0010\x0012Î¹Ã$aWvÄz¶¿¢^i£¶XÅQ1Å\x0010ª¶«¼#tðíe$öc-!\x0010²\x0005A\x0002¡ìõ¯"\x0006?
¿*âp<æ\x0001êà+\x0001\x001b÷¿*ø¯þg¯.4ê\x001dô»¢÷y_0KÝsßßËW/Ë	\x0002ðá ª[X½\x001c(Y,\x000bWÕ\x000c\x0016xF²P%@g 
ÍR>ü¤_\x000bºgqÑîy\x0002ðÄ\x0013e»íe"®Ï>û¬\x001c÷¾²%t!´#ø+¤Ü\x00187ýÔùH]ÀòÕ ²ûö·¿]¾ÿ»½ü¿ô\x0017ËãÇ]öÕµU\x000cç6ì¶ðàr(_ÄÅl\x0016t¤n:ðK;}è\x0008A¡ò;ÝÝ~­d®Ú³©<ÊOÝòa\x001favZRóKqp#q\x0002\x0012oÆ¯Àn\x000e=ë×\x0002¿b4ßo\x0002.+\x001a3m%pBY¾ã\x0010\x0006mê	¿àCp|C,.@ãlLL\x0010¡9\x0010ô«_ú\x0016NsoïGnÅ%
Âô\x0007}ó\x0012fððÌÓHÿÜµ\x000b?c\x0008sä²ÝøòóÓ\x0013
ê5\x0000ä:xW\x001eÔ·9µð6+N öxÂïø\x0017¹¿ý»ÿÛÎy¶âìÄË\x00157<y\x000f¢Rù¥®\x0010p[cñ\x0008*á\x000cL@ÚÕÝØ\x000fób©¨ç"2FTÄö¶\x0004,1$:AÒ¤:@jlÆ¤\x001f¨cªÂÿ}\x0013slì{1Òñ\x001cÆÒ\x0018\x001f§\x0007"«*geK¼²ôèd\x000c·Z¹¦u:\x00118-|\x001d¦»+\x001f\x0019}º\x0017ª:\x0016êË5BìÂ²âVy.áhYh9ÝÿR\x0002ÖEiÎß\x0015}³7èó¯^\x0007ûEcâÒ0µ½Á	½Å²®úÚÛÙ,ï)ì·ß§<ÕvG%À-©}I©pu£\x000eGÃO\x000eÊþáIùòu»\x001ctÔ\x0001]H\x0000¸p%¥¾/\x00195f¨nÅHÌÞ´ª?ÏH)ë<Çã}E\x00128º÷¼×s\x001cÌ^qzpmKÂôF«åQØª\x0004\x001f6j²÷d­\x00126Õà77\x0011¶üÞæ\x0016jËß¨íJíZíìÚây½²!Å}.øq8u¬[[\x0008\x001c¨uïK³\x000cÈÉA\x001eNgië-x#ýìK\x000eX^YáDà\x0012÷\x001b!\jäß.ç\x0012¬NÛÂOo\x0018³s.û\x0004"	IjØàÙ&î7B8b&J½gÔ¸Ò0¦ÎYÇ¾ð\x0000
îÐy\x0017\x0019+Në\x000eÔÉ{Ã;qÈ?~`¸""ç\x000e2÷÷Ð¹Á<+Ì^»G\x0012Î×¬òÎ¾4\x0018\x001aÅë(Z\x001b²ÇAm» xnÂ\x000f-×Ht^\x001f¤_Cå®¸ë~+Þçv\x001bû¥\x001b\x0008>H9°¤¹²©òÄ¦wÊbÆrÃt)33\x0000/UÐùP?ðÊ£ýWåÿ¿ÿSùéè=W¦c\x0000ì\x0013¤â!GbØ<Är\x001e'8YNf\x0006ú¡®¸d6g­R¸
A$:xf\x000fÉÂL°Gòý[Ê\x0013´¥,{¼ÁÇb?U\x0008aØeÜ,Õ}ùåå@í\x000en>·À¬ê·\x0006q%`
JÁkv¾©\x0017\x0001«!ÁäFé0 øÝßýÝò÷ÿÁ?(ßýîw\x0007\x001e¿ýÃ?úCïÿnØS \x0008®Aô G\x0015ÅÆôuJÁ*\x0015,ÊÏî(\x000fuÝfå0þàæU~ï\x0005**¢RáFy]f¥ÇIcÏJ×ÊyRÕá>ûo\x0004¿b\x0014oË\x0003´~3ï./øª¾Ã-è{K¼ooo¯¬j°¿\x0004ù¬L \x0014\x0001D\x001dF?ª,ä\x0001o«q \?ª+xÑªx1û¯¸6A=Ð\x0016\x001d~:d¾î\x0003\x0004§;\x0013µ\é¡ÞðW\x0001\x0018\x0000|òµ{Q÷½\x0007ëú²ïU\x0016fÂÉÂ®äßùµå¨|Ä\x0014xTÛvñCûëÿÞ?ü
§\x0008\x0017ýþ\x0002 `qL\x0017ÂÓÄeTD\x0008«LGRÇ\x0006\x0018WRÚÜ\x0005g \x000cÖQ±\x0004Y1o*ÂK.¼\x0017·®\x000ek×BÖ¼:~NPQD3o5<¦õ}AX\x0005±QpâBÕ\x001bPU\x0000S\x0011 \x0018á\x0016<ÏØÜv.Æßgs\x001b\x0002ªJ¯2WäOQL\x0013°êéNÍÃ\x001dxiáë05~5zÚI¥>=¦\x00048¼/pô+\x0006ÖË3@T®£ëÞIy¼Åu
¥¼xñeù}ZNÏ\x0007\x0012T\x001ae[\x0002Ä·Þ{R¶×ýæÞ36³¿ÿ¼|ð\x001eGp×\x000bOÀÈ\x0018ñÃÉ\x0013Åå^"ö\x0008uû×å´å¥*\x001e±e_:wfN \x0003\x0006FÌ01µOÐ	lC}k¿«0lo+®\x000bÅ5¯ÑÑª:üíÝgåÉówKkcWÂ\x0012Ô\x0005mÌ[\x001aImîj´­¼JßÞy\	W°6ÕAnKp`jÛ3V\x0008¼½ÕZÝ´°Öl®%®'â­»\x0006³uJ»!\x0006åæ\x001bêPXÚ\x0016#ê³4§Qüõ
ïWå\x0006ïGâ´ªÊ(Üpª;¾¼ñT.\x0002Ö±:Å\x000báí\x0008W7¢ùkáÁ³wª£63Sb\x000e>=èº\x0014F\x001e\x001dß²ò\x0003Ò¹²o­'?}¹÷T	=\x001f(<\x000bf¾AöC1;¿#©xhõP&\x001dêo:wmÎÜÜpûfÙXß º+<¬©~âT.m\x000b\x0001°\x0008k\x0000Õ?ô(ñPî\x0000	Xf%
 G\x0007¯1\x0010è!03¯BàhM±÷É\x0014ËìK¢­ÀG\x0008ÚÇúêë7*	\x0010e¿àWÝðÂ\x0008ýË+î¯g<\x0010ûâöOþrÑ>\x0011= H\x000bª×5	WM
>\x000e¼\x0004÷úðÀ3EKËì©s\x0006WÏBI±tL\x001d¥pUç)y0ø£ò§o\x001aÉ\x0017u \x0001¤`bYåoô¾h\x0013¸\x001d	Ìø\x0012÷âÒâQ½#É
!¸E&ü\x001a\x0006´~±CV1s¤¡©:\x00116ò³¤òé§#Fþ\x001a<ýÑ\x001fÿqùÇÿø\x001fòOþ¹\x0003AÍ\x0006 \x000c8¸ÚÍðaRª^.ô 9\x0004T'Ë
¨ï\x0004ã­¦\x0003uóágc0".\x0012³]ê]Ô¶¨Gtîõ³pN¹E\x001b£[ÿsùÙé×2ðM ²ô!Ët\x001fdþÒ\x001fôÉ³|®Ï»á\x0005×Ñîî£òX
pXú½*³Äò¬´8iD:ÆÓÀAõ\x0007ÞTÌXÁC76¶Å?×ÌÓ-pÑ'ÿÞË:M\x001f§¿Jw8\x000fâ6ªüQ¨ãÌ¿\x0003N(ý*\x001f,Ñ_?ó~òQ9W{GÏsA4§b(â  orHÙ1³\x001f¸%-iØW>ÑçþÖ_ùO>â"¼ããWb\x000eëiT+\x0001£\x000cÔÁ)\x0013 \x0018âb3(ûO1Z2î$«Â G\x0016îþE©Òù_\Ó£ÚbÜê\x0018Ù¡YxüôYYS'¨¡V¹Qeqªé½6B\x000cÇÐa\x001eQ¨jäEÚ2QáØ[ÑÀ\x0015é²â¹V'-¾i0;óúÕWåøèµ\x001a5ïÉç¬º\x00151XÆ?\x001a¾Â¢\x0010C\x001aJ³bF©ît«û
r\x0013ªnæÔUJá£R²\x0015´Ã| 
Fl7Á\x0008GR.üÍ©q_ÍÕð¦¬6WÊÓÝÇe[£ÑùrY^~ùrqvP>üösuú7¥}~TÖV$ü.ÏV³ü»¿ý\x001d1M.
e3äRÙÙ\\x0015Ãm\x0019wÜ\Î¦AcLõék TwÔå\x000c|%,¶Vd\x0016#[R¡xóp,%ðäkpX:æM\x0013sC\x0015b]	\x0019\x001aM]\x000c®Ëyï¦ì<~¯üÖý\x0012°¾#æ.A}ýqi­ïÕ\x001d	ïjä«»RÛ¥Ñ\WÇ×*UÑßòÒ²úÒòZ|/rÝ\x0003'\x0012*BÃúÌ<ô\x001a'æâæy1ç² &ÆæMö\x000c.¨LtØ¥/\x0001©}v^foe}Y£·ëN9å!Qå[H\x0008¡Hu²ÉÆèÕU¹ózÛel+,ãpx»¨QÙ¦¡ÈàLôÙ«:h\x001fo%À,«x*añý'OÊ»Ï¹\x0003cyðBØ¹àLi*ìrÉLáPúP\x0002Å¥°=\x0010\Ê\x000f|\x00030GfÇT\x001d®GÒdð¬rCxÛÚ~§¬ª"../«é?,é)\x001cûä`¢\x0008c\x000bªw\x0018¯Í\x001cø\x0006N\x0010ú\x0002?åÅB\x0011ÿ5=Í_Wÿ o}Fè(ÙïÄ`\x000cúÇó(}p¼åHg¿²Òô&h\x000e-ÄÅ´12Æ\x0001 aF\x000cdM\x0003\x000bµk}÷Ëÿýÿö-çgåñ£]ÑêPe;\x0017ßÚò1ôn×§3¿xùÒ3Þã&<²W+<\x0010ä\x0010Ú8µÄ\x000c7¹«\x000eñSq3\x0003{óØ³9n\x000fÂ'\x000f¢w5¨ bâK*\x0007ûf¨#:\x0004eÊé¥bêÑ8¡>ÃÜ\x0000Î@\x0019%\x000eÀ¾rCÔDèÀ\x001e\x0019§EÑK\x0008F³>ÙÈI×_|üqùÇÿõ]þ_ÿíWXdëÉ\x0006Z~Zýn*\x0003xôSV\x0012D¹kRBJZsqõ\x000bøa­.$Ä½HªKYÝX¯ê»ÒÓ\x000cD°ø\x001e³úÆ\x001fV\x0008g^àòHÿA¹]_T \x0005ÞétÈõ@\x0018)ö$zÆ\x0013?Ò#yòLZò£ò`wR\x0004U¾rfF5V.T\x0000iy\x000f\x0014:nô
\x0004ç\x0014,ùà\x0019\x001cº:îÌ{þä²$>M»(\x0015BUJ¢§\x001d\x0018¢1\x0016á\x0019\x0019¶Ôàß\x0002è\x000bEyõòXq2iÂ\x0015LôáÊI(\x000e0\x0013¦þý
\x001d¹ø¬½÷À¢Û½úY\x001e¬\x0012÷"vñ\x0018hºÃLÜ¡È	\x0016\x000bäqAù\x0006\x001f]ñ£\x0017åèøµÚa_\x0015'Úc#Ê\x000c:ô(z«ð\x001cB¾iK®s\x0004UW4ò/úVû¼á\x0012oî¹0ÂäÀµsêHá¡Þ-¯F
`\x000cP\x0001,	JÀ©Ú'\x000fFßkJe¤èvK\x001d1\x0017©É\x0018DMBbd4·|G<D\x0003J]ñØ­I\x0008\x0012¨$º{!Z\x001d\x001f\x0015\x0006â\x0006är±Ü»À\x0008<0rò
2\x001fß\x0014þ´Â³×\x0019\x0007\x000bSF~\ñ1\x0002\x0008DSÀ[¨üT\x0018Åpm\x0002\x001d\x000c/ü/útMtt®ìqR¯PVÔnïl'»[eKÀ:ÛAÇÛ0]åCÄy%;ö°ÁL\x0017%<yÏ\x000e
\x000e\x0006+¦Ïmä>}Æ(-5>	mëË\x000beEq,)9	¸ª\x0010¦\x0015Ëí°g5'Úà·u1ëµ5w>O/:Mî\x0010-ó\x0014Ã\x001bÊ¼ä=eÃ+á\x0000Áha­Ìú
:TK
¾%j
W"vö\x000cÝ£+7RêxÅ\x0004Ðó\x001bÙTìóZ )©\x0015BÖÒ\x001e\Îþ:+u¼CN5Ò¿0ó1\x0008×Ü O¯ÇÌÖÍÕ@å½r[\x001e¡EhÉ~Å]8á\x000fåw Á\ýÀlÙ:³w\x001eïï¼ÿnÙ^\x0010\x0004Î$Ì²4CÇ>PÝ°_MµW8¥\x000cÞ \x0011Ó.þJ\x001d>û°h\x000b¸Û÷.5Z\x0012°V%|rÐAt:~1\x0010Ça:KÆAÙ\x0018y*¡±ø/?\x0019o]%Íþ2jZ\x0018Àmü¿¡hãªóc+Þd,Ónr\x0016\x0013ÆÑéÂ;e}mE]ýG üöE³\x0008W,­R¡s¢uFµ,Ys1(Ë×ìµ\x0002·¾ÅZñ\x0010\x001f\x001bj©GãB
¨ë©ØÏN½C\x0003ÞÞgv¾÷\x001bß);\x0012¤PÓÁ¼¬º&ï,'¨\x000b°R&ï*å+}UÉ\x001b\x0014ÁÂx$÷MÅÉ=V}Ë\x0016\x0000®\x0010®¸gkeeÕ3UÛ[ëe·8ww½,Èé³ÜÇ\x0003î\x0011\x000e)\x000bô5.sðÝ,wØ\x0005ÞQ\x000fAú\x0006\x0019¾®\x0012ü­ î\x0019dp7.xÉ²Òé,½t)!\x0004\x0001diÙth\x0018 åH?é*óB2µ¤þ­AærúN°
(«g³ª6j7ñ\x001f\x000f÷{â©\x0008·\x0010®ûME\x0012mBfðazÀÐ\cÂ Xuç>ú\x000eî5ôe\x000cbÄ+¸-@1¸¯×\x0005¡o¢OQ¼+ÂuT§\x0015Ü\x0018Ôs_\x001b7·³¯ÂqþÆ\x0012Eðq9¼Où¥\x0003\x0019^Ý\x0012&qt¡Y\x0006îiQÂhY!Û\x001b\x0006
\x0017
*IEn5§0t´Ä\ÙÕÝïIU*\x001b.³eHÙT°½Î;u\x001a)\x0017\x000bJgAá\x0016\x0014ï¹«bÏÃý@+$¨ £å=
^\x0011
\x000cý1n[\x001d`Wöx¨	MÿºùëÂCáù~H¥ºÙ Qo8@«NÈo«\x00017Ù²	\x0011¦ÍÅ®Ì6å(÷\\x0002Ì\x0018:Sº»ÜðþìòìÝ÷¼aFÄe³êXyæ\x0006\x001d!} <C¾\x0010; :FªÜ{ÅI9±YïWáæòM1åm©­æjÙ\nu1±ò²¢Æ»¬ê[U«\x001añ¯ËïÓõòþ½ò­æR¿\x001a:\x0016\x0018=B9L|Eq<ÞÝý\x0003«k\x0012¨8IÈÌË]E§áÎá-
x\x0010ÿAbc\x001cKY°Ò7\x0002(\x0005	Ý^¿|ùâey}pâWt2jÔ·7CÑ'3vÐ{)+*ïF«Y¶ÕYn­6ËÆr£4Õ¶\x0016D«³Â¯$r#mªí.«Ýp·ò²Âµ\x0014SÛëÂçúJiÑñ©nCnÕ\x0007gs\x0003µ#ÕÏêbN\x001dö\x0004ØY®\x0018öeæ{`\x0001÷Fn<£äq"åR}C\x0013ð	6iss{l\x0010\x0016Í8i\x0004?Aw\x000b\x0008© B`\x0006§æ\x0014£Ç`ÜPÇmÑ\x001fRé'¡n\x0006²ã«+3Bò#3Ou1«NûgÔ	¤{½
AÛÐ\x0019'\x0002ÿ÷ßo\x000e"PIøa³$Üç\x0000\x0006pÄG\x001cÐ\x0004B\x001f~\x00102?õ|å78|\x0017ÖU	ª~ÅÏ³b\x00080Ðs#,Yà_\x0005\x0014Ú\x0000Jô«4(\x001b
³éZ*óMz¹·ë/Ra½*Û$¤}¹î/qJ?oüLKòdûÇì\x0017\x0000Ô\x0010\x0016©gã\ö\x0019-Q¤\x0002<«Eûÿ·\x000cQ0Gþª¿V>À4©\x0006ÊÍä\x0016~m\x001eÓO\x001d/(ý¸þ#\x000eh-çÀ		2{\x0000®~¥\x0011\x001bæ½\x0007Ox')ü©o\x0017WùFÊR£¸\x0011¹R~«?p\x0016¤K&´°3\x0016àéÓÃ¯'uôÍifÚG\x0003\x0014Ú1@ÞêtzÝ\x001cñÄ7t[Çñ¬÷XTÂO\x0013	±Èò\x001e¹©\x0018 "¦æPFÛ"ÎIo( BS]xÂ\)»Sð{\x0005á²`¾dæjo{KÃ;\x000bN¨ÍÎ\Ë¬Aa9¼n3\x0005$^CEÙ\x0006åµR\x0000tÊ\x0015\x001bß"\x000féÅõW\x0018f"5GSu\x0004N¿®J4]0iND
ÈrÔíëî©Cªt4¥\x0006Kb\x001aý2+ì0[±xZ^\x001d\x001cª\x0001²±Ífo\x001e1~ä}J4@Ò!ýl¬\x0016Lå\x0019BeÆý ìËà1ow8ê\x0018®Õ±p/\x0012Ïl4ÕI¯am4[e[BÖNK£ßµVy,a
ê­òîÎvùª\x000fßyR¾÷Þ»å»ÏG\x001b-U3ÓÃeu]Íy³í\x0007\x001f|P>øÖeggÇyRiå\x000e=\x0004à?ñó6H<\x0001æl¤© u7\x0013»É¯è\x0019\x001c!°²Géñó÷J³µVÎ;ýrtr^.ºñàùë
$òl\x0011\x0003\x000cnÂ_o-';åÃ÷ï½ÿ~ùMö¶	\x0007%4m5\x0016$x\x0016	W×¥)ÁlKÇ«Kåéöry¶»éG´ËÐºhXî·LyKxZtÔR®#)£-	:kÊæòØÐ\x0008´ÒwKí®%¡7\x000cÕ.\x0011çÅ\x000f\x0010a½7åZø^\@ iÒ¹\x000b·È\x0018È~|¿Àï}J¹ó¬f/ÀâÉ¸ª`ÒüuTÂ¤¹þ]zýC£0V6b{`°+¼Wh\x0018º¿!,0ûøÃ\x001fþ ¼zõÊ\x0010t?Ú\x0000\x001d\x0008@|¨/Ê
 »}T¸ÓyÂ®®p[p½Üà\x0001íYÓ÷·¿ý-\x001f¢8>=·E»?ßy¦A\x0007á\x0016%\x0004\x0013\x0000oJJz£}£0§\x0004ü¦\x001fÌY&òpåÄ\x001d~O~ô7©\x0000âùUTBÆ7\x00068®OBÆeN<ÿºÀé\x0003\x0014UrD3-®\x001bPÇ\x0001åÉr¤;¹uýè/i¯T@ÆA_\x001a÷L2;\x001bD\x0003 ;Å/X\x000el·sÖ²úy\x0006]áZ)x¦z!xè7Ñá¹\x0001\x0019Ãr\x0005å	y\x0003?!äRªX²#lûQ~	#\x000ct¸½\x001d9\x0000\x001c$Nº9°\x0004Ìa\x001cTî\x001b íM/ûûÿè£vçÜ;ç»ýs\x0005\x0015CFRéYkä\x0019,6w¢ôWE\x001bß\x0014ÌþÉ´TeV\x0013ó\x001fvä#f¼Â\x001d7Àåw&ÙäËfé½òìù»eS\x001d8ûØüsÜµE\x0018!@\x001a­r\x00121è×iÉ/É:#¡0p¥Ê§Â\x0011kÿ×ê|÷ËþÁK\x000bY^zñ\x000bwG(ô(Î0\x0006ó vÅ`;\x001bß\x0002\x0019\x001e¸Ïü\x0010Ü\x0017%7ã
\x0013ÞÌ\x0016Î4·§w¥\x0008ztf\x0013cÖÉ·\x001f=+ÛÛO<RcÄÑÁòã\x001füai,Ü½­µ²³¾êëÄÏLFGÌ|vI\x000cfiÑ3\x0019zR\x0003ÞØÜÌ\x0014,\x001byÙÐ=â9Ø\x0003@êGô~s©N»\x0017ºg4êáÀÖR£¬JØÞZm]u&O$d=ñþ³Çesu¹\x000c;\ópR^\x001f]kUçå\x00064Sv\x001e=)¿ñ¿]Þûà;>ÕvËc½*¯OoEm\x00125}Qù Üÿ\x001b¢\x0004é\x001a\x0000\x0010§ßªò·b\x0007U22}Î	Áµ:Jé}uèg§¾\x0016dØ\x001f9uè
Å³²4WÖ\x0010Ï%.IÓÂ\x0003³¹ÌD­\x0008ß­Å¹²*¡gUîÌÜ\iGàiµ)ÁsÕÙ.×\x0004¬4=kðpzr&áè²ð°v«!át±aakøDCM1Ûe©\x0015	VÌzµHK\x001d;3S\x001c0FX1`ÿYkm[Âö®÷²=}ö^á\x0014!×X ¤³DÀ\x0008ÿÞÇäkPd\x0016Ã\x001eHÈk\x001d«Þ8\x0006Í>ÏJx\x0001÷à·n~\x0008\x001e
Ãw]eg	\x0015\x0008õÖ\x0001â\x001fï:úæ|å\x0019 £ñf`©¥Æ\ùñ¿ùAù\x001fþù?\x0015M3ût¥\x000e#\x0004,f6\x0018¥3[ÅOÌ0a?`6xÈè>Ûiv`øg\x0005Á³ætlÂÞhE\x0001âQ\x0018èY2®â`szkmU:÷\x0012Í¸ny\x0010Ú{ã\x0004'¢)+S\x0008`©W\x0005\x0014Ôp2úN«O2£È+Ëc\x0019KéØ×q¹ÜX\x000evC\x000fs~çÁT$T¯\x0003pÄ÷\x0018Âv\x001eØ[018´Ó~ìV'ÜÀqv~iN\x0005~m¶kå>úª@å\x0005°u\x0018AÖUþÉÍ´#ýðo\x0003*÷W{§5y#ß\x0015K\x001aÕ¯¾\x001b'cÉwìUbºbÆXöv\x001ey¦.ãqù¥ÆÉE9 QôV´p¼¬)¼l¼±µåw\x0007y³þÜ\x001bßFh!f"âo °ã	:¡ Q
ö\x0010f¹»nh|\x000b¤ó­ÎG²\x000f¯·°/C~!¼!|Q×D\x001bõ\x0001³®á\x000f\x0016­\x0015 ð#ºcÓes¹4ÄçØØÀ¥J1²ÔQ
YþFÇ­
è!>7¸D(¹©Ìb®«Rf¼n\x001cdL]\x0011ßóòJ\x001dñ5\x0019Y*«k\x001be{w¯¬Iç2>üe¦=S¥B»\x0013«ÔUáÞ\x0004ò\x0010ys0{Å¯t\x0013\x0014\x0004Æ\x0012Á±Fmï¥H\x000fÜm8p\x0015`7\ùyH%L¿®J4ß§\x0012î³¿\x0003ª\x0007îæa\x0006\x000bÝ®5òh¬¬Kðj¯^\x001eÏ¿|YÏ/ÊI»[.º½8yæÙ\x001cÃ|\x001cñ\x00060jâ~SÛ{Á
Ô\x001cQ¿\x001aJ \x001dª;Q\x0003\x0013Á³<ÖTg±ÚlíµfÙÀðÎÞfy÷±:óíõ²-á
õhsµ< ±¹±àwT\x001bKÍ\x001b«\x0012\x0004wö<\x0013J=\x0017fRL\x00030hPeâ#\x001aÞýj\x0012oSÍ\x001e	\x0001*Ì©°¥}qÛ|\x001fÁr©YÞýàÃòÛö/H\x0010|®\x0006=PPïäªnÀWGF\x001c\x0012úoØ\x000fÄ\x001e·~·,Ü\x000c%xÍ\x001d	ROÖZåÝíÍòÁ£ÝòáGåÏç[åÏ¼÷®¾·ýfäºü­,rï²U®Ê*BíæÊ:ÃÇkëå]1¼÷7·Ê;\x001b\x001båÚý£å¥²×X,»Ëe[BÕ¶¾7$d1³Ðµ$¼2Åhteu³ì=}^ÞyïÛåo}»<~ÊÆÕÒàÙ\x000bf²Ä3`àÐ\x0001uÎ Äû¯ªúG}\x001dÜþ2*aÒ\oÃJd¯|Üx\x0000a7no\x0017ô\x0011\x0014b3zÜ5f~üã\x001f/¾øB£òíØÿ\x0006=Gcö\x0019$ïé¬\x0006Qð¤}Ó¿¾Ó>Õäw*SY\x0000M\x001c|òg®\x0010è>üðCé-ÇÙáþ3¥\x000bþ o³û\x000b*H\x0016}\x0005¤Jü Ü~ªö\t'YFü¹óJ¼§>	£,÷¹×Ã>¤ð3©&óêë@%ë"!ó=@Ü9\x000b*g´Hûë¦÷§
_²SÇQâdä.å|ëoÒO* qRÍÂ#+øù,ú[
°|	¬\x0006*Ì^­°2¢\x001dÜ
>Àv\x001deÿèÚ/­«¦mÇ¸of`G?ï~zìFä3Ê\x0011e\x0003ØÄ¬\x0015í0ÃUøIwëÄWA
÷\x0001A\x001bY~ Ã&î\x0000áeF\x001d©F¬\x001a\x0015­´Z~»,\x001eÅ¹PÌúdb`âÈ\x0005¨\x0014ÂU¸K{!P¥8äB;®±_âåzåÕ²¾õHûÝ²!Éy^\x0015b7\x0004<e½>H½Þ8WSú\x000f «\x0014Ë\x0011Þ0\9ª\x0019\x000cß\x0013QX¸FÃhë\x0019:Ý35 ¦\x0010&iDã7Te\x001f#WñUß¯«\x0014è
3úC*ý×ÃÂa¦:rYeòFÍ ¦)ü¢¨'ÊÉõ\x0018Ü\x0007ÄÍäÔýÜbSéFÙR}pGÕÏ?ù¢|ñb¿¼Ú?,G§\x0017¥×\x001f8¢³ #ªWá×uEÌ\x0015-\^^[q±æÕàª\x000cÕYô;\YÐõèûìì¼*þX>ìyfË\x000b\x00116xRgWÔ#	XO\x001emIx\x0012­ÌK\x0010½ò\x0012ØÖÆJÙnÕÙ5% ¬¶^:ñ£¤jÐnp*\x001b\x0003\x0001Êl@ø\x0006¬ª©æ\x0007\x0010;Rõo¡¹k\x001cïX1\x0000a\x00030{8ØGÃÃ­í§\x0012°fK\x0003	áßeõ¬ZÑÑÈ\x0012sþö²4\x0014Çªì×%5m5\x0017Ë
	Y;\x0012$TýÖógå»wm·¦¶¼\x0000Ý^Ih\x0015\x001e¯\x0007½Â\x0003ÜÄ¹D:¢\x0015¡aCïqs¥¼³¾Q\x001eI\x0010}¼ºbáìñzËú¦ðÉ\x000cÙ2y§­©,,\x0005rU\x0005§~ëC	X\x001fÖÆ¦\x0019Lùdðlæ*!\x001d\x0006h&\x0008ª¤¼KT½ã\x0002Fu#¨\x0001¾\x001fRu¨§Ùuð\x0000°a\x0015{0/:ç¢ë7{/êx²³F°ùòËÏmfY¸}ð\x0000!K4\x001e{¦{Õ\x001dú\x0004\x001f?Þ¬2£|í\x0002v\x0008Z\x0015.PI/©ÒÞKQªÃ5ï+d_\x0013Ï«Í°ü¾¹³]\x0016D_æZQX`\x00127À\x001d
-Óü\x0001Ø×Ë>âº[O»º_òöî¨I·o¢QóiFéæI»7Üª}y\x0001¨ÔÓ\÷
\x001eËÃÒ,Ç.©}¤âÛ\x000fN+èCêO\x001b¨\x0003¼RÎzy\x0001²â\x0000\x000f )Ï®W\x0019ú`ñ\x0016Ê3zRjÊ\x0006G¯¶_É£%\x000eÎ<¬\x0006\x001d'\x0018o³Õ^,úU6Ã\x0003ÝêF}Õ-\x0007×â[¹¯Ì*/üHùK³\<PDGÈc¥Aî½¤\x001d»?P\x0011\x0013W#<)¾Ñ\x000c qç²
\x0001ÐGAOwìgA\x001eXÖH¶Á³\x0007\x0012x|Ù'\x0002\x0010XdE\x0019Rt\x0000%.t
Q¡X~\x0013úT\x0000éR|s×\x0014~FþQ¨ürL~em§lî>)[»OKsuKÖe($²Ç½\x001e\x0008j×\x0016ø\x0010¸ÔaJ©éFþ\x001e\x0004ò¦B;í\x0000
mF$i\x0015Åqñ@°$Ø[ÌÓQG*Ó \x0011øMá×\x0019>+8\x0015nT4\x0004z\x001bØ¯êwû¼4b¡VaõÍÉÍÝ½ÂcÌ¯\x000e\x000eËÁÑq9>SGÔEâçå~.3\x0014®D¬L\x000b6\x001bÝ¨!hÅe\x0012ÄâaödõK'[|¹mGñIÀj_sÙqOÏ@q^±Ù[UGçÇmè[Ûkec³U%\¨V=Icc»F*#{¹½b&Ë÷ìÁ%D]UÞäÍÉQ¾¡Vò}\x0006ÓìGÌ\x0016-Å¾CÈåå\x0015â$pí\x0010³ÜR¿¼Âi«=çIªIÞ\x0011°\x0016ÄU\x0016\x0004\x001bÞzÛÙX¹á}U[ê\9½ÉÓCôýtk³,
\x0017KV7eQR\x000c»çÔ¤­X\x000efÙ0öxÝJ¿\x0011ç¥¯(­åfy´¾V\x001emlÇ[[s³ì©#ßV\x001a-6Õ3"W\x0019\ZÕ+<aai¥¬¬oª>v½L\x0008½°tèÙL	
´7è.ö¥ÐÞ	\x001cí\x0011#8¯ÓjÂ}¸þ&0-®LsR-5ØÏANhò¬\x000c³@ñ>$v\x0016´Á¥\x00143W\x0008P\x0008ð\x000c\x000e\x0008³R¹iÝBU%PaÇ½nõ\x000ftÜ2Læ#ÝøF/½â}fÆö÷÷.y¡<ÞÌ7\x0007\x0007<;Ä	(¥Kx©ûÚþ/eðH<£¦\x0002ÌØ¡rÓwÎàd½gzÙ2¾ôÊx'ã¦\x0003ëßÎ}*ójò{RÕÃ\x0002Ô\x0015À÷¤¿:`G¹êeCýÛ
õ£ügÙ2ÿõºÁ=ó]ÿF¯«zx\x0004úôÊU+ÌÞ×+Ú`ð¸-$ø\x0015Ô°
,\x001f|\x0003Ý*å
É\x0007i¶Bn©Ô­å\x0010É\x001cEr
~¥#·P·Þ#Üïº½\x001cXGë!\x0008^x¨ÃloØ/\èÈ©0V¸\x000c\x0006-~,\x0006½¨8$Ü\Â\x0014m!	ÉK\x0011e\x0000\x001a\x001cY?	B×B2Ï=@Ü\x00074«B.F=«8ßT§ÑPX:¤[u\x001eGOß+»k4¼-ÉyY#¾9	X3bN*à\Ã\x0007{9c5¼ÆÅ\x000fuæU§Î\\x0018hËNÎ®fuXÊ¦\x0000\x0003âxñ²:æ\x001b1Ï×/Ä´^¨¼½²À;.pµ¸¨ü-©b\x0014O*`\x0012*,\x00145Í_]e9Ã¢ó
ÔãÊøëáë
ÚîÊ"ËNÄò+ò}¥\x0014Ã(­kõúè[õAh\x001dpã÷àª<züÌ\x0017o>~þèqVÂhÐÊÑéiùé/>ö{wÌVq8\x0019-<%ÖSÇÐÄ=N§\x0012¦OÏ|"ñü¢[N$T\x001d\x0013	V'ó+nu?;óÅ\x001du<GêDú×e{oW	OG^æG1ëÊÉ@\x0006\x0005Ì`mmlÆ}5¢¦ÊÀ~\x0014\x000bz\x0016Ä¥T&«
'Ytò¥ïûUT\x0003þ)\x0017\x001dçXá\x000e.ëõ1©HNÙ«F+#m ?1ãÃu\x0013\?Áu\Á¨×B\x0018ÓÚZËõK~¯\x0017tÊÈÞ¬YµÇ«~ß,£+Ü\x001e½Ú/]áY<ªÉ\x0011\x0016\x0006B>(ðÂ}DëÂã¦\x0004µõ\x0016w­Yã{\x0019\x0001OùFèãÊ\x000e¿§·È	Sñ\x0005Ñ\x0005£U6ìÏ)}*¨KÂ Oj²¬¯´\x0006\x0012¨\x0007=Ñ\x0006'#Ø§D~/f(Ùsæ\x000b\x001dUÖA·i*\x0001<¤zû¤¿lCÑXÒk\x000b%\x0008AåììDüàS\x000bW\x0000x\x0003ã³Ï?ñò\x001f×\x0013·|û:\x0019I´gmÑ­3ø\x000c#b±0\x0003éBA½R\x001b¡.E=%ð~«	\x0015Ô6Vkk\x0012j%\wº]
Nú¢Û²«¶ñìùóòÕ\x0017\x001a\x0018G\x0016\x0019ø0Á@²ÜÃ¥\x0014Æå®«otè\x0013\x0010:TVèdÌÃ\x0010Ò:á\x0001ðm)ã­»¡\x000c\x0007¾0\x0013\x0006\x001c¤Ði\È\ou°\x0019>ã@7ÚVã1\x0014vG\x00048ò\x0013åg§1-dÞ1F\x0017Hs½©\x000cjOJn¤¢}.ún²Ú;:mA\x00138§BñõyHñB\x0005üÕÓ¦*T\x0019Ò\x000eÀ\x001eÅåºà\x0003\x0018/Ú]Ô\x000fe\x0003\x000cø0S\x0007\x000c@½%{ê%/\x001dVíX\x001ct\x000b`\x0004~±'.\x0008\x0011à\x0013!Á/@»à2^o\x000f\x0011Oä@\x0014r\x0003\x0017"; 0×å´«Ûß\v¥%fn$0]Oè4>©ëKÑ·toS\x0010û ¶0·hû3õA¯_¿R;V»¡(ª:-¢s½ïq¬ê'ë(UÝ.ïÄ­ú-\x0019\x0016Õ1©\x0002¸s7ÕZ­5\x0017%di·È¬VSßB\x0011c,¡
Î½4¼G¸$)\x0015$.)\x0014T\x0018¸ÈR\x0001æöB1d%]VÅ¬ÙÌþôÑÓòèÑ²µ³[VW7$ÔÄ\x001e ®\x000cCêU\x0006ãBQ\x0015\x001c<\x0011¯Âû\x0002Dé,%\x0013»\x0003ò\x0007	\x0003£\x000byIq0=/©uÀ2W»\x000c/;¿z"(\x001b#ôQ!®\x000eÔip}ÂCá¾iÀhæä\x0001x(\x001e/%ÎÆ¶/*ÔÈBÈ\x0017H¥ïìíyY=6ìÑcä\x000c\x0019,QíÌúåP\x0002VwPÚ\x0012¦ÎN\x0011ª¸µgX¸©~Î:r \x0002ÿjÿ°¼~pÞ)\x0007\x0012¼/Ú\x0016ÎH¥¦E1©[:dÑê¬:{®\x0007@¸f\x0016
ñ\x0008&
	Å0\x0010FÒä«^æ4££¸Ú\x0003á
F÷ë\x0000Fe¤`áv"NÒ#\x0008|¦cü²q\\x0002a³¹\x001aù¢\x001dÂaF\x0001{f\x0007\x0011RÏ\x0013Rfú.ôÍéÃxÌyèYì®ÔQ)\x0016ïZ\x0010~Ð=\x001bÉt:£E\x0006(jC\x0008\x0007Ì \x001cÐÑ)!7\x0014
Ì\x0000«\x000e0ö8ÖÞ[
FK{Ìezf°¢©×\x0011\x0010¶òí¸,Únìr\x0002\x0019®\x001e>Ý&á>û·\x0001á&Ãò\x0019m^å\x0012o`/\x0006Ëà',ò°Ç\x000eÜAãÉ\x001fGþ¥È?ÖËTWé\x0017\x001c§\x001f n\x0006ø\\x0012o\x001eP,·ð
}3ÅZø»\x001bî>xÞëx§IÈ4Ñ§©4×íê\x0000ÝOSà\x0015\x001d¨ççS¯«¨»»ö	uó´òLÚ=\x0004Ô\x0015*ËD[\x00072\x000eOVLQ\t*ý>\x0004ò:z¾r\x00194ã\x0003êfüå)pÐ}Òõ4\x001e:
hûl¿\x0008\¦àB®\x001cgªvRõ§\x000c\x001cG\x000fÅ«]1\x0011<\x0000ßbFÉû£'\x0014\x0002\x0018
VzÝýR2\x0006|ÒÂ\x0007÷Q6%®<Ð6³ÌQ>Ú0'¹j\x0005\x0005?ä\x0006\x001a\x0007B·\x001fæ¯êê!HÜ°÷> \x001f\x0005)mÎ£°­ÍòD\x0002\x000f/ho!h5×ÕñJú\x0016æBD\x001fµÄd:)/\x001fHrõædEÎ7Ó_½Ì¡\x0011\x0011Ë\x001eì/Y_i½­Íòüñ£òþógåÃ÷ß/4\x001aÞP\x0007Þä¢B\x0010"¤ûöqeÎD`RQª\x001cfÏTªü)\x0007TÑÈ\x001fá¦*\x0017Ôµ£
UE\QöÏËyû¨\x001dXÐº¼Ì
n"\x000c!,\x0008\x0005\x0015Ì

u\x0017°\x0019Í\x0012Mó;íî3OSosG%PÇ©\x0000ò;
/;TBs(Î	7²¤Ó\x0011#8Â¨ì=\x0016-líø4\x0008\x0002\x000c~P\x0006\x000c§`h\x001cÔS(fjèüÏÚ\x0017åèø¬\x001c\x001eJHàñá\x0019uðs¥=ã'm\x000eÏºåÕÑyyÍÏ\x0012\x0010Î$4÷¥3¼.\x0003:nå¥b6Úsë; xç.nXç²Ð¸$Ôy_¬F±\á\x0006ÌÒµ\x0014\x0003\x0002ReIH3õôó\x0002R\x0007FfÑ%kù³RÞ¸þEw0\x000fÌ\x0016fw¬2sm\x0003Ë¯<~ÊÌ\x0010ÂéÙ-\x0004\x0018Çy·+!ô´¼:<.¯\x000eËþÑ±¾Ï-î\x001f×G'v»Ð\x0008tA\x0002ðêi}ûQYnq\x0002wÁ³]á\x000bN\x00165Zaà$ü\*±³~×3gb8'\x0017¡Î\x0010æº=×\x001fû¸d4ó\x000e×ì,²\.v\x0018\x0003Ó\x0010¤ ¯\x0011ý©}¡¼4/A+-\x0018\x0011M\x001dG	ØÕUÝ®nþºê> M:"+ùît³\x0013	²m3^\x001ec®\x001f~\x0004\x000e`À\x0008¢Ì\!p^IÀåÛw	UÂ\x0015iTé F÷
)\x001e+¹¦\x0002\x001bÙÙ¼â{q¹1ÚsÕUýf¸q<\x0011\x000eVî¬\x000f\\/5¨ã*ÍõïÄG)\x0005ÆºJ·Tuÿus]\x0000TãNû+wð\x000f¨ôS×ëª\x000eyÏï\x0000þDùR¯k\x001aÔÓÆß×\x0005²*ÃÞÃð\x000f¿Ù\x001aò÷³OïÒ@V\x001dý\x0002Ð\x000fµ	\x001cÌèt\x0015UG\x0012þ¥êü\x0001\x001bB÷%*={µwZ¨UBÜ©2tGÕíëþT6Yn&êP¬0Ä Nvw5ð>Ë£ãrpøº\x001cDÿ\x0003)f6³\x0012O@¤1Æ]ò'\x0000¿u\x001c\x0003uúûþ_ÿO>R\x000b{6H`©	àÖÕ6Rc¾`>O\x0004b3b:9ÍàÅ­®Ü\x0002Ï¾\x0016¯-ªPròÒ\x0007·½rÎz«)¡-nùEßÙÚ(\x001b\x001bª fNT(ò&$Üªæ6u\x0010Ê¨\x001fD¥° bèËb
\x0003ÃÝ\x0015µJÇj=¾s)'\x0010¤;,í\x000b\x0002^ý¯Jx.?x\x0015tDÔ\x0013âC¯#X\x0013@Í8a?FøCæi:P·{HéÇþ\x001dæü¶©\x0016OÍ8åBN®gh­oKxY\x001bâê½pø \x001c¿þ²ÜöÏ$\x001c¯úÚ\x0004U\x0004\x001a\x001e5fyb\x0016â!pÕS\x0007}Â(A@[ÂÕü\x0004fKÑ:K	_\x001aE_SuêÝ\x0001Ët6Qe\x001cj`·üX\x0016l)oìïñ\x0006j	úÌn²É÷ä¬-!¹§4Úvgï\x0016OÞ<~þ~ÙÜ}ìk'âuq\x0000d(w4Jh\x0015ú\x0005 ±0M\x0007ð@ùÄ\x001fef\x001f@l¦\x000c\x0006`Ð7,À{\x0004¡'é¾\x0002:ä´¤èp(¦Ó==*ó\x0012î\x001búæ~·yá»àxJÃ\x0003}ÌöCîÍ:j÷úêh¡ßW	[í.OZ5Êº\x0006G;;·\x0013yÆÎ÷¼-ÁUx¦¾ð,!\x001a¿>Õ\x0000×C ê,Þ;ô¬âïÁ\x0014åÎ ~yLz(<ÞH\x0010Üyü¬¼óí\x000fË²\x0004nN
úEý
E\x0014\x001f´ZNcCM\x0008»ËaÏo|i`Ó\x001f´%D2jäÊª½	\x0012¿@2­ÄyÚÕ¿\x001fRÄYÿÎ°	·âg>Z.\x001eäåE¿Ô\x001d/
¿¼IÆ¶_|ü³²ÿêpÜ\x0012ëkvbfL§?:\x0011RÒw\IèbÉ¯\x000e^\x0002¬\x0014~\x0008åN{>++ùá4.Â[Ì,\x0002É£,È¦Ç¬\x0011Ë\x001bð¦»bÐ\x001f³\x000c\x0013÷ÅÈ\x0002ZDÏ\x0019\x0016Ï¨`Vôû¢\x0006\x000bwó\x001f\x001d\x000fÀ·¼ üe~\x000323Oj¥Ê|×¿Çfâ\x000c\x001cæ÷¤9õ»iT~êª\x0002?·$²»\x0010e\x0018ëàå!Ètñ_O\x001b{ÅMþ&ãuþ¾\x0006L&O0hm\x0000)( ÓÎH3I\x000c\x0003\x001c¦;É"\x0000­®¬Ç\x001fûÚ\x0015¾Û*D\x00001D\x0019DwÈwØG\x0018)E
/wúj_ö%;Ò²\x0010®øÝÓù¾¾ÖFv©ód\x001dmèJ\x0011ßè\x001eÄ¨íÅL;\x000fç«m¨\x000cÃ!v}ñ\x0016&PXb¾SºÝ\x000b	x/J»}¦~é°\x001cKÀ:;;.ÝÞø\x0010ÏôÛÕ\x0018ïÓëA57²3\x001e\wý$PÖ¹¿ó·þÓXÏÃ\x000bøg­·é8Z¹ÚZWGÚ,kB:'µØËC§³³H{3¥ÁI£ÅÅÒ\x0014óYF0SgËÛvsê,XÀA÷i(YÆYÿ%\x001f?²FCVa\x0011à6¯r!\x0014Ó°qómàÄ)ÂÇ¿\x0002×Q§\x0004i²PX\x0015×¿A\x0002\x0014Z\x0011¡ÔY9¬¬dýØ¬:¶Ò\x000fÄT¹§½ ?\x0008¸xä\x0013\x0004\x0005c©!\x0015UGhe¬ÛM"ïi*Ý\x0012&íê
â^È06*^é)8¡ÛoÐQÓ\x000e\x0005ó öÖöã²ÜBàå¬\x0019Ä¡GàÒÜeé¼\x0016
^õ\x0015ïÝa&\x000b(W[-52|ÜY7X\x0004:í³;ø®¾¹ÿd¹µV$\x0007ã³\x000bÏÀ°\x0017«7¸Q\x0007¯Î\x001c\x0001KauYdiXå¦A]s\x0001d»\x001c:®~'a\x0006^vdfìLq\x001d\x001e(K§³$:å$êæö#\x0011²Ê!¡âVq\x000c rÓÙÓ¡gÕ-³nðI+S\x0014
N\x00085²\x0007C¸©Üì3d0éøÑù\x0002¿ø&\x0012Ó ¶\x000c>Ô.\x0012nºjìCÑâ¬\x0018\x0007õCû`@ÂiÖÎ /ÜôËQ»ã÷
ÏûQJú	8QÙÙ0/ù´ÌI\x0018]P{U£T\x0007_|Xà\ø?:E\x0000cöCpÌv+á§ÎÄ|N..Ê\x0005\x0007\x000f\x0014'úbf¡¨\x0013Õ;³X
s.?¼\x0005*é¬ì>}§<ÿÖ\x0007\x0012WTíÁ\x0001èÍovÒá	\x001fÆ8°íUnØÎÛÇ#\x0001K"ÿ1x\x0002ê\x001dK]Md¨\x000c÷\x0010LÆ52+¿<7äø¬D+¢QEC£ø¦\x0004¬\x0005öÍÏ5\x0016Ëç_|\>ÿô\x0017\x0012.y[\x0012ú>[x\x0019ýó t\x000b¸óÒ7Ù#9Ï\x0000Ô\x0003E9çµì\x0016'£¬X9\x000e¡7:¢Ü·\x0004íVQèçnØ»eö @úX	wÂ?t·Ä)õ\x0015\x001dbÌÀq£G°^©\x0005lç;T\x0016\x00083în;\x001bßé~?à§\x000eñ\x001damªIvªÒF0ã=:BYó=2Sf}ÔÓ\x0008ã(Ïà7ÊQ¹O\x0000ýÃ·NêRDÆ«âðÝbàTtuM\x001dÚKT\x0004	ý­ \x00042_hÔ\x00154Y\x0017°\·v\x000fNÇéÞ\x0016\x001eBgÿ$oç\x0001<|¿³»+^´d\x001a÷=ýo0½ùBê\x0017!\x0002»\x0014\x0000vè,ùÑ¾\x0011¬d'ºå>Äø× ßSûéKè§£Ú¥§>÷\x0000»ØºÃ7:÷\x0005^t¤Úâe\x001a ñ}~~\x001c÷\x0008¸/?=9R¾/ýpô}v .¾£¾þô\x0004µ¯°G·PÙS\x000c=A? âóúeùÑv\x0008E
&xiPå\x0006·þ®p[\x0007ìæþîßþG\x001f9B\x0011*S÷ \x000e¢cdÂC¨k[e}mUéªÂ&\x0004!é\x0008MJÙÄÆÒôY58Å¬xn$e^it~ôÉût2_ò/û\x001bT¸¤L?d*b\x0018°\x000e*DsDÇ>¤a3«ÅÉ'ê\x0018¡Ë=¤\x0005+Bèg\x0006P×+àËòÉR`»}*	V ¤S<ê8#±.\¹ÑVñxÙ²\x0002\x0010Æ_\x001d À:r\x001f2çw'\x0015?i÷TB]²È'M,ýý¨\x000e%P³ïn}{¯,6W%Ì\x000epS\x001dHÀjªn¯z§eifX6\x0012¦UÁÌ`ê×
	CFå\TÇãÌ4\x001c\x0004-\©cF\x0004æº\x0005	<§\x0012\x0016^\x001dpÍ\x0003·3KÂÌ:\x000cE\x0002½±\x000f°µÒòFu\x0005tCüâÓ/ÊÁþa9A @qv*¡êð¸\x001c\x001ex\x0016
ô~ôYÒ\x0003\x0017`>{÷²¾ó¸ÜÎ7L\x001dgÄ«ÀoØÚL\x0003AøJçi8\x0004ìciPLLøò\x0005£ÐM\x00157)yFÄ60UùÅ]8BÀº\x001e\x000eJ_bÿÓA×y¢3çD[WíÓlöï^ÞJØº~]zW7\x0016ØÅLÖPÒÀ¬Ú¨8d\x0019¨Ý\x0008¯\x0007Çb>\x0012LÙ«Å[x¨³±v9íH(Pý\h¤w¡\x0011`÷J£Ákv&2ôÒlVíKàêÂ\x000c\x0019\x0014:\x0012`oT?sË+eïù{åù»ïyÕ\x0011ì(ð\x0003×@°Â$p¡¾°£=qB\x000fÆÅ¾Ç[\x001a\x0011°2üAJÈö\x0000ÔÝëê!7T\x001dÞ°AêÓ³ \x0012®xD\x0002Ír\x000f£oö=QKKóåÅ/ÊO~ôÃÂ»t\x0008X3NÚÀê\x0000\x0001\x0008¦KçÄÞ\x0011TÉâ×gfCÆ\x0004¬ë:P\x0005\x000fw§)¦á}\x0003ÜM\x0007\x0008Áa\x000cÊeeJ>M¥\x0003þT]À"\x0016Ò¼OÀbõÁ\x001dv¥ÞÈÈ=ß\x0005"L@Ä:åS½(\x0007é\x0017¨Ëô_\x0013\Àd|	\x0019G]§ôo
XaÎ<@ u{\x0000ûG-ÖúCù \x000c
<[øî\x0019Î¸ùOg:÷Båq¢Vî.uÑ\x000e­çwõ£^ßù``ÌÞ«'\x001clÚÜÿÊ_Ý?º¾Q´\x001b"å¾?åJ\x0017>l4e¹M0³Û\x0013\x001fº¸hKØ9/''ôÁâßêÏ¤QBqÙçÉx½\x0004$fÐ¹\x0000%{$®Tâ;®V
u¢o¶û0xk_H\x0010ãÉ.J¼çïú\x001dc\x001e\x000c.
·\x0005\^uGúEë\x000bä2\x0003\x001f¨ªJEP[\x0010^êu
dùG\x0008\x0002é\x001f}îo±DH$T,Ò¨\x0010â^Ç\x0012\t|s\x001a½ZêV¤H}¼Ùu3Ð÷\x0018Í\x0004£2ÎQG6ò<Ä@#An:\x001eÊ¯©t¡Z%à=º­N±´*\x0004t»åä`_êu9UçÐ9;\x0010¦ønW:4\x0000FRþ<ÛÒ7>©¼&ATzB0\x0010¦ëû¾TôPi\x001d\x001e½rEÜJ¸\x00198®À	?\x0011\x001bgÍpô=Bªànìú®Y¤\x001f äÌu;à>ûû\x0000\x001fVß\x000c\x000c1¡\x001eSº«ùI^°µ±ý¸,6Zªz	Mò\x000cÞæËeYTG8{Ý-Í¹+?M³$\x0001']¸qzÁ/ðJ\x0002\x00167JÓX\x0016ìõ¶c)iq¹é+
ö%$í\x001f¶\x0004ÁÃ\x0012¦%\x00085qcy«UÖ¸Ò@VcaQÂß\x001aÝOu.\x0018ñ\x000cD\x001b\x0012{j|q;yWùP³\x001cÈÒà;\x001f|G\x0002Ö£r;·$£\x0014Ì-AÒüBç\x0008\x0002ê\x0004ùìá>ÈF\x0006Ô\x0019%`ê¸fPLEnÄI&Uy/éî\x0008Õ
H a\x0006k~\ÌeGàðuY¯ù9\x0014Ù.\x001cª]tKÅÝ Ó»ºÀsSz\x0012$Y¾óÅ°Âíáüò²èûV\x0002'ÌëL\x0003\x0007\x0004Nîeº²¹#¡ÊWc°\x0014¨¸»,ÿ)¯·ê\x001cl\x000eU\x001bcÃú¥Ú7*<X,¬Jx\x0013\x0015(ÿìáZ^]/O$\=ï}§O÷\x0007¥À\nµ3ã@ÁP } `(aä¬Z"\x001c\x000c/ä!®Úðþ&ëÄ­;\x001a©;ôÌÓTÝý
P&ÙC\x0008ýªöÖ¢ÚFóî¯cv\x000e\x0001\x0019#îX;×ÜÂãÐ¼¯É~*:(òj@éP\x000e\x0004,ê Ám,Ð3UùA6* ½:ä·¢y\x001cw\x001dæÊ_ê¤£Øã£ÉolF3\x000fr¿\x0013?\x0003Êè¨CO\x000fVMP´tÙ£\x0016Ø+©SEÂ=àÍï±y\x000c\x0011\x0016Ý\x0001;hã.ÔÃVé¾EÀÊô&uUÌ\x0008Ô5¨\x001c/éOà;!ã\x0007¼
ð;©\x000c¦\x0005¯ìFùå¯îï! 
ù£R¸²NÝUywY "AÆËÿ\x0007¡¯Kkuµ¼óü]Óüø\x0002ñó\x0014amFlS\x0003\x001aÄJÙ	>\x0010î_p\x0005¯¹\x001cú8$\x0012\x0016E8ÁÛ\x0015\x000fdæ½Q\x001c.A\x0010b9%>#.\x0002\x001dH¡#\x001cY]²1kT¸oYcd
éRL\x0012yËO¥3\x0011s%åVþæ¸CQmÉÙ¹\x001b/ý3ç\x0019PrìòE¾¡»É¶fÀ¯Û4ùOü$¸ì55÷×þê?øÎãg<\x0015sÍ>*\x0004­ËÒSÁ¯%<ÝH@\x0019^¶Ë¥Ñï+\x0015xöV£éÓ×¥ß9-ç§G¥Ó>ûò@Ç¬Qß¬:]ùo¨@<\x0003ÒjH²Vo®:å»§Ès$V	W'û/ËÙáËÒ;×\x0008W\x0012ç
'üzçece©Ì¡X:d\x0018³ò9Ï¬pAÎ]Û\x0013z\x0008Z ôÔ)Áà%	\x001fªC;´ðVd3x\x0010®Ø	
a z©`Í\x001a\x0010k\x001dÃ\x0011Ðº>	ÓÜ'ýò"môÉ
¼\x000f ;³iÄc\x0004\x0005C#¸a\&YÛÔ²­Ý²º¹WfÔ\x00141L9ñ¸ö<ÂÕÕyY¸í¥¾\x0004\x0001Õ«ê\x0000A½BtMè\x0008S,téÐ%\x0010Ñ¹ÐA¯nnyO\x0010'ÞNè`5 Ñ)\x000czsy¥,7%T-KÐÐ :ázXa_\x000cépÔ0æ.gç¼Å,Î©\x0010N%\x000eÔÏ¨\x001c;ß)Ï%`­m=** ª]uLÙù\x0003\x0001tæ\x0008èàØpã×¨ªèp*tÙt8Ýü¾\x0015	Jh³\x0005Nü@BÂèwøè-9ù\x0008Ý
»CáyÁ¯ô3{â\x0019[ù½¹à/ÒCi\x000fÕ\x0006\x0015a÷zÆee¿\x0019Àþ õµ²µµå?rÃCÒÌæ1\x0003Ð4TÌ|
\x0007\x0016ÂBd_\x0018;\x000ef\x0007î>»èQ	\x001f\x0008WW\x0008XÂíµÒöÓBìXj+
6\x0016[ëee}§<}÷[åÙ;ï«N;Ê\\x0018E\x0016\x0015Òî¨\x000f\x000bVØ\x0004þa¼p®Qæ¥x	
\x001aç*¤w··
Ü)HÁä\x0013¶ëú×m\x001fSA\x0015:/:ãÆuðÇ\x0015í\x0008Z¦~È7S·;;\x001eXþè'?ß\x001b/\x000f\x000e¸ÌUøª·Õ,K\É\x0000O~R\x0017F*ePö§\x0015!íVÄÿØGªè¤Bcöoû!Z\x001cU\x0012Ò«ø+ü&\x0010U\x0015õ@\x0018öÓÎ÷h	/\x0010A\x000b 6­We`\x001bgüí\x0013}ìBøAO{ÒÍï\x0000ê\x001c¿¡ é§æ7Ìñf§­z¬ÓÁ4ÀÿÝt	¦o\x0015z¦mûÇÿú\x0006dåA¼¼BVq;uÜdº\x001bë]Ètë*\x0014¼¢+\x0011\x000fi\x000føhJ<8\x0012¯ð;E'>è-+ê
i9
ÓÌDÝ8¼~å\x0017\x0014²|·¾ºQ={î\x0003gìu">h
8d\x001c\x0015ÂÜÇEQ\x000b1JÑ\x0016È»CDù¤ßÁkZ	ÿ²UhN}p¬ ¹*Øu ;Ñ\x0015ÛDðCOÐGË
n\x0008K³R¾r\x00033òcâ\x0007?Äyí	\x001e6ð#|FÌÛcÇpÑû+÷Ê³zþ±\x000e~T!Ä¨¯J×·Ë\x001båÎ6?	ç¹¿öýÿü#B2ãT$é-Í^©EpzU^}õòúå'¥}¾/Ió ´%L\x001e}Y._ÙËNY\x0016r\x0010®®¹êI\x0008\x001bôÕ\x0019_\x0015\x0015º¡\x0002/JÐZS9¯\x000eY¥Ùk?ã±<§n\éÍ(=üÏ*üüMOöÜZ-óµ´áò§¥wòRq\x001fûFëÅyöS¡©ã·ªJc\x00035ÇÐy9\x001eÆÚ©O©ã¢cæ\x00022Þ\x0003;;=+\x0007û¯Ê±9fÎ@.s\x001blÞ÷D/
Zè½
`\x000e/SÇg¥@½	æ`TÁ\x0000+F\x001bQ¡\x001c\x0008Rl¬efÐo@ÉÑÄH\"7ñWw·\x0019]ñÄþ\x0011,øGùàÏÄ\x0001¡Q\x0014å\x0007bUÔ\x0010ý­\x001aRgÝöîÓ²¼º%ãj\x0006Ö$È\uõÕ+Í\x0019	W×geáê´,ª\x000eç\x0011r\x0015ÖË_R¤@ãåBÑ^¿§Q½\x0008WöP÷\x001aÃàj\x0018ÐJ îJÐ\x001d¨ÞéÌÉOoÊ÷^\\x0012¡K¿\x0011
ÞPÇj ros¥þ¥BS9Rý]¨No\x0017\x001b¥»(ûµ²ûüòáoý÷\x0008]iðn\x001bg¬\x000b¥%âv:Ì~\x001a'R0gÏô¹Î\x0013sw\x0015{\x0013ÜÙÂ \'ú©t\x001a\x001fËål¼UÅ6ýUÌÇO>\x0008¢Â²_e^´j9ëvA8ß.\x001b;ï=ÌD£\x001alÜ\x000eEû\x001a¸°\ÐÓßsá´Í]ts¢wn×`e¹QZÍFÙä®\x001d	¤\ï\x0000³ì\x000c%È2ûuuUúâ@\x0017Ê÷¹\x0004öàªt\x0010z¡\x0019ÿ% ñä@i\x000co6»²ÍÄC­ôéÐÕ~ºÐÖ·ßùóÿ«òíïüVYj´T¾\x0005N\x0017U^ÞCd¹t\x0016©PèðþkXPÐ>ÔÀ(õàøÐ£T\x0000×p\x0007\x001b\x0002\x000em\x000c´z&	\x0003ØS>ccl½6\x0002ð\x0012
¿u÷i
f\x001fÊ£\1]Ò\x000bá\x0005êWÜ*;£f^\x000eéÌï°4øÙg\x001f{Y¢Ë\x0012¡hÎ
Á*÷I\á|q×÷q*.@5b2ïÃ\x0001#ø¸Oñ'àÎG*íGßoÉÒ´²í\x0018\x000fÿììðt$ÌT¨>T~%N\x0014/Ì\x0007½*Ç\x0019\x0000EÓpãÆoé2»cÓY\x0010ÎRt¢´/:~pBh\H¬Ä	n¾\x001bõ+®\x0003\x0012nÓnäÇ\x001fÖQÌ"¦;xH=UÄ\x0015öQÔ\x0001ÊB\x000c\x000c\x0010é,ý0(Bù\x000ccE\x000fÄÆ¿ït\x0013Þ$Êè[ñ"ì8\x0019åGÊ\µ¦C[é^wã\x000f¢ñ Ì\x0010=þsèFþD#\x0008\x0004
]×&ùQ²§þyúbÐÆa³8p&÷JÅþcÕ³\x0014õÁ¦p\x001dì}¼Ö(\x0014:e\x000bÐ£ÝÇ^I\x0008!M¸?üNô3ÎÕ(?à;ªf9@#>a%~?X¾ð§Â)¿\x0010¯~cF¼=ôèÇR\x0003Y<\x0004!J:¼ùFüÍîÈg÷àµâã^9¡ÿÇ,{ú\x000b/U"\GÌÊ\x0000¹åÏÂ\x0014[ p	r\x0011¨Utê\x0014ÚÀÚè\x0018(\x001fé+\x000eh<*bÓq¥ëÇzÔÛ\x0018>çþÚð\x001fÄÄ¢Æµ\x00081³êXÝÓÒ>y%ÿªüü§?(\x0007¯¿ú²\x001f½,öqS\x0007¹¢
nIxº¸8V%õ\h>V\x0016ç½é\x0007k[\x0005ùaÏ\x000eËLÃ²¨Ü.I5Øð %0ç9!kæ¦¯x\x0007{¡ô½\x001cµ²¤Lëûöý[½Òïª£íÄµ
\x0014\x001c\x0006|-f`\x00051r\x0013'Í®×êèã0ì/Úír|´ïõÝ¾:yféèlÁf
-ú\x0018é\x0000Èy\x001b\x0018ÑPNeD2àQ`e?©;)\x0018m\x0005o¸OÀ4w_C0úF¿ïYá:¥\x001fý#\Á\x0017ø¸VWÖËÖæ^Y\Ù\x00143àB×xá~N<û®3=	Ã\x0012°n.T/C±\x0015]_\x0004	âÄ'ûx8=å\x0013O4\x000eÚ\x0003Ôª\x0006Çr\x0013îÝ«Kf/Ô¸¹ßG+3\x0004Hhd,3s\x0002Ä7jKà°`ÖUGæý@W¥'Å¬ÌÊÀî.N·ÝÌ,ûj\x0002ÞÅcv¥¹¾¡rË(#íF9uG.\x001bÑtÍ0\x0003\x001a\x0010øÀþ®NDãïðgKé\x0016Ôo,¸Á\x0018eåÆeC\x000e*PÁDÖêX®%4d´\x001fïãý/ËU÷Dþ$<"°QNù»TÙ\x001dÜx97Ì4ð\x0018ôê2÷ÎÁÐ7ùµ|#ó¥Ü»ò×\x0011Þ:Â;Âæ%BðBû½<J_\x0019º\x0014CòìÚ\x0004\x0002åPÙ\x0001[Ð
´¢\x0001ÊåMY\x0017¼÷ÁoG{ÏËbcE^\x0016E#bNJ(Ð±P¡¶5V0`FÂLßsðáôôPüâ\\x0002&8\x0003Wj?\x0010±ö&Ü×\x000e~­ fopRn\x001894¡Wê¶4WÕ\x0004¬O<\x0013Î2\x0007K¹t¸f¤rä4!'_cÿ\x0015\x001dDÐ\x0003\x0000Ùdq~­Å²òË\x0001xµRÝ3Èt9õ\x001dÂPð4ÓTQûM¤\x0008ø\x000eI\x0002\x0007\x0008"\x000eGñVª.Xå7z\x001d¸§M!£©\x0017âÎwtPo\x0003è(ã\x0007êñg\x001cõ¸&¿
Ð.ñÈh¡ÈQTñ\x0010w]Ç¨ \x0004çÛ\x0012vµtü¦Ì	~F\x0000P9ÕuøMäul\x000f
Æ\x000cø§Ús.\x0005R_Yg©êP/7nQ\x0017â\x0001â)Wjß¬$pz»0¡ß+ñZèÙ<\x000cÈaÔqr{ÇKõ\x0003ð/K\x0010f¡'\x0015}/\x0003^ù±°ç²#\x0012¥#û\x000c§,}å6U¯ZeI[êi~\x0013pñ>Úøª»õè\x0004éN$?nåò\x0010`G°)\x0003
\UÐÛ¾vé]\x001c^û°\x000c;bö\x0012¸úí£r*æÊµ\x00062Ï^vËì\x0006ÞäÎÍÏ*[Ó\x0017ø\x0019ñ5\x0016ÊÆjËogÑ²Î EÅq²ÊÜÚÚ(ëÜ(½ìN\x0003!ø\x0010Öõ³Â¬:\x0000Ò=~ýy9zõY9ßYí\x0003É^ç~w»·fUQó*(~ÙóÅ2\x000b\x001cÿüì¸\x001c\x001d¿ö½\x0017lãJ|x§\x001f©H¥\x0017\x0015\x0003b "\x0008c¬ò\x0007TúÁ?
fßné^ÿN?ÄêW\x0007òUWw=%wî¸\x001aß\x000bÅ\x00084Þ\x001fä\x001cÞh\x0002ÔTx\x0012õ 8\x0003\x0011^\x001d³\x001a6æ\x001cmùíA1¨+	;4J\x0014
ÔKq1¿À¢\x0016îÊÒRY_Y)[ÜÂ.µÖ\öa\x0007¦å9ðpÁ¥G'åààPuÆQZåkMÕ1ûÃ³\x00077bÌèVü#1wß{¯lmoù0+æV/}V\x0006f­D\x0010¢\x0011	ú\x0008×Ø\x0001 Ø\x0013e%?ÓtpàNÊ;ÅÝë\x000f*åWÊK\x000eV«ïª1rS=B³/Ü%f¼Ê\x001fõÃíê¼'¸ f4â»Ô ãB£W¯Êèû@tê
Ç\x0008esÌ¢ 	ßÌJ±GbNmi^\x0003å\x0005%È\x000c\x0015B/7*«­XW½
å_\x0013fê.F¢ìÃÐ¯Ì,\x001dÐ+¯å\x000f\x0014\x0007=\x0005P:\x0001\x0015 ÍÅR\x0008[ÐâW»óè\x001c[µÿÙÓ;v7cÞÇlºâ$$w\x0004AÿAã7Á¸ÓúúÂÁÿ\x0012ü¦ªC~«DV#¸Ù%`²é\x000f\ &íÒ\x000cd'\x000e>S¯«Äeú4'Lóû¾pùí;Ù	©ì\x0012êy¶ªð0\x0002Ñ	áêåIóäwëP·VÆL·úFuN\x0008N(Þ4¤u1 B-ª½,\x0007ç{ô£9CXO«^Æt¯û¡ü\x0000q°ïþ\x0018ú\x0006ïðqâë\x0007÷\x0000Üðß_®=3\x0013æqX¹Uýë½
&õ«\x0002q< «©ö¨,ïCjîoþîßû«¹ë^¹\x001eIp9,ó\x0003	XGê\x0014;lUÑ\x000b³\x0012 fÕ1ÎÕÆ|i5æ<{µ,ûlãÊ¦:Jß4,Ä4D\x0000TVÎÐXâ\x0016sfÖiS¦\x001c\x0017Ø¨«ÅO¨\x0013á:a¹§Èßêty)\x001eDxF¬\x0015_K1\x000bÅl	\x0017NÎj4
aâBt¢pÃ~yýêE9=c¼9¤.ß#ÒX«\x0015*«C\x0012Ó$Q\x0001ITIdi?í\x001bHâO¨Ç­Bø\x001b\x000c;	îþÅ<Ý»ô
¥7ò.ì¨ãGðbúwkc¯lnì¥åU\x0012S¼`q#áy¦_f¯ÏËüuGªgáD\x0015¡Q\x000f\x001b\x0017i\x001c\x001e`ûuá]B6¹ó\\x000ew	e¹h q}êk0PÚ¼\x000e \x0001[B\x0016K*ldç©nÂs¿\x0016aØ\x0010yÑéùDÛì,\x0002\x0008\x0017.!bH0ìÅôæ\x001båw?(\x001f|û;åÝ÷¿Ul¦\x0017cv§½yWÍ×¡3iáÛÜ%8D6³a\x000ewupÍH\x000b\x0004¦½ë¸dK\x0014~´TñÛ_=ª;ºã Má ý±o\x0003#íãW¾o\x0013\x001c\x001eñ·ðÈ\x001bÌvñÐ28[>OùXjy©D[B@»Ë	Á¬¸$\x0013¼«ä\x0018©Î©-y¿ì^ç\x000e\x0019W¼H:R,ÔAãâS¢S[½\x0015M0Ó¶÷èyùÎw¿W6¶ö,\x0000ú`ê\x000e¶v#¢nIK)ºpÔ\x0012³\x0008&Ì^qêg¨Á¢U¯ð\x0017îk\x0007¿6 \x0002wR|Wy§V¡\x001býAÌT¹úÔ.\x000eË\x0017_ª,§Æ\x001bõ
-°_û\x0003	7â+è\x0008¢\x001eÂüË\x0014úz\x0018~È*0M[©s­Ìð;*íôa\x0001ü®ªN0ý Âm\x001c\x0006¨Á©úR\x0006gÁá¤fô7Í6PO£î\x000fH·\x000cöô*?£8*]ßwâEÂ
T~Üë~ü~[BúT\x0000øD\x0008J\x001bÙm_Ãu=Ì}PÇ\x0007ý\x0001uÈ=<$ÎsyÄK?¿Ø\x0015<p\x001aØ^mz¹'\x001fwp5\x0001æø\x0019u¿\x0019ß3~*Óü?>"À[R0Ôózæýë´íz:uóÜßûëç£k1½ÁÅQé¾.\x0017Ç/½q}Ð9Q\x000f¥\x000eV*³T+\x0012ªÖt\x0012¶\x0016nKkËø4\x001a\x0016`¢MuHCÂvg&^Eã£Se=·Ùl©\x0003m*3tÕ\x0012\x0012ê\x0010#\x00137çá²þÊZ1:\x001bc\x000f\x0003¨S\x0010óRçÒ»à¶:wÞZZñÞ«!\x0005WHÌ©óéÃýòêå\x000bubg"\x001a^È\x001f*þ+å\x0007ëÂÑá\x0000F4ùö×\x0018ñèFfÐì0ÓÎaÐÓ®Òó;ý\x0003 ÞæZ\x0018w¼\x0015¤±fu\x0007¦ºÓQI»W©öYc'\x0017¹\x001cJGÈZ9³#{ÛÊêú¶qÈL\x0005~¸ÿ
{©°lÛ.\x000b·ê\x0014é½×Æ-ÈJÀb&C\x001d3B\x0005¬:öjÔéÔÁ/ÓO0QêSuCú\x0008T\x0008Ð\x0008ÓÔ\x001aÖ\x001aÕCÍ\x0012°È7\x001d8\x001d¹Ú·O±]» \x000b¥/É\x001bÊWÖÊ§ïßøÞ¿S½÷nÙØØÀ¬L¼èèxuÀ\x0002½âcf\x0006åù;uªÑÊ¬ò£<Æ&ô?}¿¡+=ö P&\x000bXSþFKÐÂmèÄ+`iGv=Ñ%óÃåðÕçe(ZeS5\x001d?Ku,3åº¼¸\Ö[+e»Õ*\x001bÂUkQxÓ ÷\x0000¯Á³Ê{¥<!\õÝ¾¢á_
\x001fìV`Y\x000eàJõY*fæ5¨Y \x001e%[âA<-*P)Ù\x0000+ÓÜRyþü[åÃ\x000fÃWn\_#x¹3{EÛtOIé\x000f\x0011'%¦]S.5ýÒ0rxø¢´ÏOTüK\x000f¤h×jËÆ¯P2R|WªÂÜ¯¦&â¬+/a\x000b7£~à?ä?tìÙgÄÉX2¸È°}~^¾úòsë#¨êÙ\x0004\x0006Ð/\x001cÕ"«\x001a .ÞÖ¾¿\x0019üòOYià«º7R¾Q¹÷*ýd\x0007v	Ù\x0001*¸r\x0010­Îz¤\{Ì\x0008	*<¸@±$ÅÒi(f,BÀI¡ªÞ9\x0001º\x0019à3íRç¡ðJ}dBÁ/É¹û&øÚ^ãÔ?1àN\Æ¾ùEOåÒË}d§p#?ÄATúÈ|\x0012Ý¤»
Uq3àñ \x0007¥~ÍBV­N²\x001eRâª\x0014ñ×Ýêx!\x0003¼ÒòhïÔÛ=\x0013\x0014±\x001f¶Ï ôþv=è³{Í\x0012±åLÿ
°.?õUÏó½à\x0003\x00190òi~Ýô¿&ÜÁü\x0019¿ëéÔÌsßÿ+¿ûQ÷ü¸ìU÷¿(§b\x0017§ûå¦ßÇ¡\x0010xåå4îÀâ½7Nï©Uå2; \x0002TÅsË1\x001bxcÓc\x00185\x001cFqÌjpüM¸¼¿Æ%?\x000cìÎ%	)\x0018>\x0019ª£ÏtÈ4@oV\\x001e-)^\x001aæ@Î7³r·F;jâ\x0014g¿L\x0018×^\x000e|õê«rzrèN¥ÐiY°
aÍûjÈ¦\x001bötäe\x0005ß§\x0003\x000c=
 î§îxh$	Óâ¯ÃîtÂèÄ\x0016\x000eQf:\x000b\x0017fjÌ\x001e6Z\x001aµìµÕM5à%Õëp¬<W3·Råà^YPg9ÃÒ+\x001d6\x0002\x0016Re¹ºf¹ä6:r\x0014\x001d«ì©/3\x0018¸\x0008ù\x0015å`æ°Är\x0014\x0002Êâ¬tÊ¡<Ñ)#\x000cêßÞ\x0011,ÊÌ|\x0019pòMÞÊ»¨Nt´R¿ó­òÝïý\x0019Ï^­on\x0017\x001e\x001a¾$\x0006­xê\aeoÑtoÂ&_\x000c^{\x001eÍCÉTÕ2MW°Ñ7B\x001aß1ú!n\x0004%:	À?þ\x0007\x0002¸é\x0013°RfáösyÙñ>Ç£ý/Ë%w³±¹Sm©Á\x0005¢j3,í²yeÂ\x0015}«ìe@4£ïæú¯¸XR\x001bã9\x000bê\x0002Å2d\OáÔÑ\'\x0008µà\x0008AwD©¦\x0003\x0000iÇÔO¬\x0011^ÂT«µ^ÞÿÖå÷?ÿU»åÌgø+äÐ\x0019AïÔ'\x0003!\x00065í6OS¼öÕ(¾weY\x0010ô\x0006ª§X\x0006÷µ_\x0017P\x0007¢0WåQ)-Ì|" #XQ&f²{õêeév;\x000e9dvÓ;³¯\x000c8êÍ\x0000øeåê{\x0000\x0005¤$¿\x000cDÙ\x0010'ce&õf%û4ÛO¥Oò©Q\x001c5sºÕ!\x0005§\vJ=Íð¢:\x0004¦Åw_ü|NÚMo*¸\x000fN26
ä;})`½Q
U§:ä7zÝ\\x0007»)RÒI£:¨©­Ê\x0019+Tú\x0007ò;!ÝRQÉï±BÀ/»»{¾û
;f¯2=ê0\x000f\x0001\x00023ázÜ)4¿
À\x0001þ3Ìç×\x0002y³ßZØIÈøîSo,[B~ÂVz=¾ºyî/ýÎûèèèuÙ\x0019ÂUï\\x0002ÉàB#\x001bwÌ,°§*8Ò\x000fÒ¹²Ô£\x0011\x001a\x0011¨#H"P¨AÏ/ÊÈ\x00136#\x0000\x0000ÃâIDATþná\x0005~_ B \x001c
é<ÉÁÝ<Ý\x001e7L_¾-.5t-c$n1HL¯/\x0001MÑBIÕ\x000cÅ¥Â\x000cB@S§{ÖæÞ-uªÊÃÒ$p5\öLìï¿ö¥¢\x0004\x0012Ù\x000836azLeSJfL\x0014ÈÑ*p\x0012ú4þRå:kÝ.ý¥=ßé¯î7ý1\x0002´VÝ~ì.ðGÆ\x000b¤{²\x0011Bg¯¡{ÏêH\x0002	³»e¥µêÆÞ¥ù[Î\x0012\x000eËü5UW\x0002V_v}5~áÒØá%£söì0+B#R½HXá´\x0013Ù1r3"2Ù'YdGYýRh	Æ É«&T<\x001dÓàmá@\x0015N{kúÌ\x0014Ë[~Æg}k¯¼û­oïüæo÷Þÿ°¬mìöDq¼\x0013-<§ÃéÑX¶S^¬Ä7\x0004#/\x0011Il¤?õ_W·°¯püRX\x0004µq:²o©ÊM²\x0000iñHç\x0016ü¡Ö³£røêÒ>Ù\x0017Õk`C§Ç +.O!]Þölª­ÌKH\x0005¿ú^%®¸`	6H>,)\x0014²|¾ |3»Ü`@$ÅÌ0\x0003#]e\x0019½z\x0006Yá99Éõ	nwÂãÖÖ£òþ\x0007\x001f½½'NB\x00064Ì£\x0006,7Â\x0013.\x001d\x000e;ßãuÁíû'eÿà/\x0007d@ä\x0013£B<3?Ì¡;Ïe¤jH4i×¾¿ó²+Ò§\x0005,¨úõ¯]¡aÁÅ%\x0004-	âw\x0007\x0007û.#\x000bu\x000cÏåõ\x000b\x000bX
\x0005ßc\x0006\x0018\x0012Ö( õ¯\x0003\x0015?¿\x0017¾\x0016ìq¬bÿ¤Ú>\x0010°L_R\x0008SÙaóÍ\x001f4ÂÛ4m\x0008ÿøA\x0006ÝÎ§@½£¥³NV4 ®ìÉ\x0010þê\x001dÓ¯å¥\x001eÓÞî7TÔmè6Ëí./VÿEcr]:zÇú-\x0006ýþk\x001d(»©É½ÊV\x0005ñ\x001dvé6Î×\x001d{Y\x0011\x0017¸Gqh\x00005ú\x0016þ]/é\x0007Þ\x0003­*(:%K\x0018ãd¬÷\x0007>Äµñ­Â2\x0010e½Ò´Eüg]$þÔtw<ÊA8Uå\x0001Ç\x0015®ëv÷)xb\x000fZ
3:ª¿¡\x0014Þm6<I\x000bý8q\x0018qMSñ\x0007+úÑ_¸)°t·®o'?aûßøíxø;¨ÚÇ¥\r\x0014ÿÖû«ÔY©\x0012å9Pô4\x000cé \x000e\x001b¡Ñ\x001b\x0005e£,\x0004¹¨0Ì¶}\x0011·Ð`ÈlÜõ2*Þ>ãn¤NoXÚ<"¦ÍmÜÇ|RN\x001b¡·ë®Û+}s0q¢ü«\x00138»àý´Ê+Pùàvxn\><>\x0014±¨£\x0010\x0013g##G>1Ç¨E\x0008¢,&2t}VPoÔ©î$´û\x0000wÂOúË8\x001d?5E%c¢÷¯éiÿ {DUAeo\x0008z¡ÑÄ·\x0000<â^^)\x001bë[eeÆ%ÿÂÑ¼\x0004ÐÅ\x0004\x0010N
r}\x00063½2£ÿJ#y:¡êÍÐ\x00084\x001a\x0003)~dë\x0018iS²W=\x0018qàåb3
²§úñÞ,uÊø/\x0011Ò\x0014%(f­|jN\x0002ÓüR³,J\x0018l®m§Ïß/ßýÍß*ï¾÷Ai­m)\x0011	ó\x0012òäUéR¶\x0010}bO\x0010+,Ì0(ùÎ5\x0008\x000eÆØÎ\x0012Y~SºnW¹aËJôuW§\x0001\x0003ÜÕnÐMw.aãøìD\x0002È¡\x00067¯Ê ×\x0016^yBø¸Q\x001d1e\x001fød\x0019oEu¶±²\8=È¡\x0012Þ\x001c\Ë¿ÜoÔ\x001eÀ¿¼° \x0019xæD+\x000e0Û0½\x001e{ÑXxUYÈ¯ÆO\x0016\x001cb&RX°º½ó¨¼'|¯ol¸¼4öyyF§ßÑ@éÂ³6\\x000eùü\x000f4Ð9ôÝWÜ Æå~Ì\x001cÇqxr.¸\x000c\x000c¿\x0001ÙNþô@ùQ\x0019ãä\x0018ô)+)SÍÂ+ô¬<#@]©} \x001e\x001e\x001eª¼\¬ÌÀ
Â«Í`ÉÌ%Ðr=÷Ñ\x001eÂüË\x0014KUò |\x0013\x0014\x0011\x0006Ü2´°\x0000%»I¾\x0007£Ó©§Ãú7ÂÛß¨\x000eÃ.Á´T)ÚH]Õ;qb\x001c«|)Ízçðf:ÐÌæç\x0001õtzZu=\x0015Käw@ñÕÝýF¥t9ÜCrÛ¥f÷6ôÃwwJÀßI\x00153Ô\x0001|§>rWùÓ\x000cPÄ	Af[\x0000´ë%nù®q¦£ì\x0001¸åwG\x000e|â6-\x000f\x0001Õæëo\x0004õ°@=þûÀ>éÏª0ÓÒË8ïS\x0016¾&dÙ\x0013&ãªÛÌÿçô¸ýêËOËÑOËÌàÂw\x001d­ÍÕfÙÚÞôl\x0002Ë\x0018ji
¢\x00044
½fß\x0008\x00184÷f°|È¦iNÁIØ {5¸*gmÄ@Ê\x0016\x0008QB;B3O~°|È3\x001cdY0ÞaÃ;3f>ª°T6Hæ\x000e\x001a6ßbæZ\x0006^ïõÕÌJ8_ö&í¦$ñFsÕwýðØ-3eÐ \x001a!9¡s£Ãä\x0019
¨\x0001!AÖ 2­ïº\x000eÔÍÓ N ÓÂðÀÈãXw^áÌ5wf êú]f\x0005TÊ¸T:ËK\x00003~|/sÄ^:gcs·|ëïxÕ7§3£p5(\x000b7}	V\x0008XÜ]¦:¼j«>ÏËU?3ºDÀ\x001aH\x0010\x0012
\x0007\x0012@\x0006±\x001cÌ«éÌFÐ\x0011yªç-\x001b\x0011@¾/%\x0008ôº\x0003øyÒEB¾Õíª~T'ä{n¹\x000c%È,H\x0010ÜÙ}R©ß{ò¼¬mlº\x001cóË¢!\x001a\x0004¨eÓ\x0010ã\x0007¨[Ðé¥\x000c¼ð­tÈ¨À§"o\\x0007ïÔc¦/ô\x0010¢\x001eÒohÈ30GhCðÎ7øG\x0007/\x0000þPä
\x0006WÝË^ù\x0017\x000cÎ\x000eJïìuéëóÒ=}í{âÖ
Õ\x0001§jKYR}­.7ÊZcÙ§
ç?æ`¹#;ÁNÛ\x0012lÔÞ\x0018°p¡(\x0007\x0016¸\x0012á/ëk\x0017È\x0017ß\x0008qÍõU\x000bSÌ>ºó«|¹ÐôêÿWÜ5Y\x001cy 9çÜgDFdD2\x0000I\x0004+ ª¤\x0007Õ³SõÔ#;\x000f32û°2+²\x001fa_ó\x0003ÈîËv÷È4\x0014E¡ª0\x0005\x0014, I$\x000b\x001eá\çûÿýõè½æ'®Gd\x0001»½z]Ýì\x0018USS3S#Ç\x0014ÝñÉ¹ríÆ-)´©9»\x001dX[\x0010_ÄãÎþ®R´I³76·*³j\x0005ëØ¢\x0001xIm52\x0002¿Ìóþò\x0002d\x0019Òü}Ùk¤õ\x000eÈ4M\x0001la±jE=Ò\x0007Ñ/}üñÇå7¿ùÀ
­oVôùYV\x0017ü²Áêêªüh£J*Óé\x0015ã\x0014TÝC_¨ºàce\x0002!\x0001=þØx
Gy\x0013é\x0019+\x0014pVMÒ\x001dðªI\x0007iñ\x0001¿lÃä}c¬BFþØéË9ÆJ\x001eýLúÕõù¤wm\x0007°×}Gæ\x001cÛ_ãö4ë¸Ï ÉÎBAº\x0001[5°8à´Ü\x000f¨mIé\x0006}qÐÝöëäÌgD«ò%f¸ì3\x00122-·UÕß\x0012nÂÖigSù5@\¯$jò6ª1u^\x0013×\x001b7nsçÎY¦Aâ\x0013\x000eH@ÒK\x001a0ëzI3óì÷S ¹z\x0016</
zÚg\x0001ñEßÚ4fíV??\x000fTú¾q2¯¡ë¯¾ÏG\x0014w××ÊÞöf°RtÔ©ëHrÅ=Fb¶\x000f¿\x001e\x001c\x001eHé:ñ9)Î»ø¢ÒÅ­\x0003¶\x0001/ù\x001cpGÏ}90A:QáS\x001f|Î÷\x0019©r¹z[\x001dQ°\x001c^&
:w=\x001f·q{%CÏLäéØ¡mFËQXY­Åû¶l	\x001b?ê3\x001eêÜaydÑU¦ÐÀ³ÊGCª\x001a\x000f\x0000s\x0012iÉ0à,{?è\x0017¶ëfZ^°\x0014Ì7Ã{>§I']Oü\x0013\x0010\x000e¡ÇeÐ«\x000c¸å
\x0016üàÓ\x001f£c¬L,±I)*RBÇ5pj\x0010\x001c+{erh¿L
\x001fÈMÇá½r,Å*ÎÅi Ô\x001f·ãSÿ»\x001däm¢h\x001c,ÏAF\x001d\x0004
\x0011Ìíd7L£|YtrÖCíÈGGæÁ±\x0003Ñ<13_Î_¾Z®¿ôJ¹|åW­¸(:gk`pLô1TDC¡.]eÔ©XË
\x000f\{;\x0013wÂÀ'W\x00105\x000bË\x001f)MV@c\x0005òà)YøÃ\x000b*X%eë,ÞÎã\x000c\x0012gTLå@[÷xAcwËØÚÙ*Ö\x001eJ¹bå»Ý¤
)\x001cß)T¢MÕ¥hQÂÅ\x0007ó97Ó`§p´;j]Ò °1!áRÓ Rîð¯ða#¶\x000bãð,\x0013'VÖâb\ñ¶§0\x000c8´eÞ>-Ãc\x000c)\x0019[|u\x000f±r\x000er[nÜm¶«úâ
rÄ!ÌBÑÖäÈã\x0010)B\x0010\x000fþz@àyPw^ý:²ß\x0005$)$ \x001bée:2Mg<\x0017gPC\x0016\x0008\x000eYqX[[µ\x0012A\B²ÂLoïòi\x0003Ç54É¶ºß	²¨§üìÛì©Û"\x000eoÁ&\x001düÁT°\x0000äÂa\x001a?·ÝÆN{æíIú\x0016\x0006mVïà\x000bÛÛ(L$\x0012êøFæ~ýìmèõÉÄ\x0016[\x001d¶N£¦·F ~7ÿ«´i)
á¢{þ!3å¸çÐÎ/ËJ(ý.d§{¿°µ\x001bx
Æ9ý
×\x0002è\x000c\x0005I¼Q{ç<îìì¬W°p\x0007\x0001Lh\x0000úæ/¨Ýo_8Í²1d½<\x000bEE¨vý}%P\x0014â%&¤}èÒÒòûû\x001duëR²6wË¸úÜåE1{|Ôc`é(6(:láaJsm¿=±r$Í\x0007;«\x0012'êUù\\x0007Û}\x000cÞÞC±R\x0007½»w\x0018_ïGÁ\x0012
»l\x0007Éß.å¡¸\x001aº¤PÅÜ{ªo¶\x0003½}ÈªÂ\x001e(\x001e\x001f\x001d\x0004\x0003?ÊT\x000c
z\x0016\x001fivyi\x00050yëÎ\x0013À Ã>üìª
D'KT\x00066k¿vØú¹ýâöÜ M¦i
\x000c\x0019è=·Ý1O¡iÏô"m5Ë&\x000fÍ\x0010GT¡*\x0003oe¾ðkzj²¿tÁ¤gg¦Ë¹ù©2?1XfÊÄÀ^\x0019\x0019è¡ã\x001d
ü\x001a÷4\x0000sÀ·;ÕðP¢¬`\x001dùÓ8¼¹	\x001e²ÕraCy2ª22ãã¶ù¸q\x001eåFÄHæLU±jMêeFõ,eû3TÃcåâåkåÚõåúefa	²l¡\\x001c*Üäá;\x0004\ùÑ9 l¶Dø\x0006\x000f\x0000âB\x0011
à¡ÊÅ%Ð/å-¶PÕ	|û\x0015\x000c+\x000fliÊd\x0010A¹ØélJ¦·e²z$ÅigC¦'[k«pãwGZ+k\x001b|Ät¥¬¬ñQÓ\x0015?ohRÃGÐ¹Dc·¸âR¨\x0016 \x001aQw¸¨r\x000c¹\x000c(M
â*¥\x0003ê ÷ØÌÎÌ¨^R§XéRÉ7\x0006RX@\ä}D	rÎ¨xO;®ø\x0001«@4	î±\x0003ôL®xÁÉ\x000c<B±âBÔ#Õw(¥âµ_&QläÚ\x0007ÝpÃDv©#TZgÔ\x0007²&·~\x0018\x0003XÏlÛ)ZÚÿå(p\x0002N¤ÆÏÎ±*\x0013\x000eÛÐäQmiccS¸®z`7ù¤Í±/Æe\x0005PN¢4\x0002l_\x0008ú\x000fípígçÕ@í×/_FB\x00064È{ûX2ÂÏ`U\x000e,ÊÂ«²Ò_
åë¢1ÉbØÝí\x0006(¤Û\x000bh®Ðà\x0016éFúL¾H9ÒpOÛÓL{
ÈB\x001d?¡\x0018LyÙ¾ÏçDÜí§\x0018È¢ÒØÑÚÃvd¸¤\x0019Ïô]\x000eÝÏ\x0004w¬\x0008×ÂäeN*á32ÈÙPoÃêç£\x0014¦\x00177Î^q\x001cçPx	\x0013?g\x001bÿr\x0013¶\x0001·zÐ¯Ám\x0010¬R\x000fô\x001f¾V©ñË¸I?Ð?\x000fÂbëÿblÚY_|¿
O­<\x000búÑ^»Å(FÀ'ÊM~ýy\x0018ò×CÓ[áÀ\x000fßxã³\x001f\x000fï£ÎAyùùòÚ­\x001b\x001aH\x000fÊç_|Q¸Ùû@ì\x000fÂ
YV÷]\x001d,«\x0002G{ûÑ8\x001ed³"áÃ¹\x001a\x0008Q¼Ø:dKpW³º\x000eÓ¥\x001c±ÂÄ\x0004«\x001d)JVØ4\x001e\x0015ÊÁ\\x000eáú
\x0017\x0017QÂh\x0011S`Q\x0005ú\x0010¼&Þèx\x0019.£\x001a\F'Dkl`2X±¢ßÂ\x0005\x0003\x0015Obl{
Ýôµã7PÛ\x0005'!ãôâ\x0016§
øªéã×Å¦,5ÔþÔ
\x001dËÁÔ\x000bKò(\x0007\x001cj¼öÒÍ²tåZ¹~íjyùÂR\x0019?îÇ÷ÊÎ»å`ë¡·\x0005÷4øó1ÍêðHÊ\x0005g¯¨ó\x0003)Ê|}}ï¼Â\x001eoîi\x0010Î-WòÏ-\x000cfjÏ££m7fQ'\x000b\x0006u%a\x0005{c»S6w\x000eÊ\x0011ÚÇ§ËÛï~¯¼pý¥rþÂ\x0015¯XrþÇoÕy\x0015KêÇ!
ZÔ\x0013rRby1ÄL- Ùî=·c°"Oû\x001c:ªd¢F\x0000x½t\x0002x>R|!×#á¼%V§\x0015ñÈ'Ý1½Ú¥B\x001f\x0012ÞJ\x0006dÉ(\x0008mds¥\x001cHù:él1\x0019\x0012ÈF
ï²MHÝÍHâ
êÓ6oj0S³2Owø¸êÁaY]ß°\x0012ÌÊ
«Nl) Ô"\Fº£vÇ·\x001dQá/õE[ám_ø;=¿T.\¼Tæ\x0017ÕÄkÈ7
\x0019È3 ºµ+oðÂ¦\x001b¥Ø­´»n\x0002x\x0011fð¨n\x001fý05äsÏÿ<°\x0006i}AÕ%yã%¨[Ú\x0010²þá\x001f>ú­ËÇW	\x0018\x0008³¾µ¥4Q4x;FÎ3òx\x00164l;\x0013Zìy&V¾ä\x0001U!}¬åÄ3ÂÇªhÍk+XMXpHépþ\x000e>À\x0003øÃJ\x0016Ê\x0015ýL\x000eÚ	¤I|LÐJyã\x000eö³'¤=é\x0001h\x0019>1e¢¶×´3\x0011ãÂà\x0018\x001c3Í&\x000fÅ\x0005¸\x000e¿l¿Ù×$¾|lÇ½Æ\x0004èH3iJ\x001eð2	÷\x0006Öqð~òé²»ÿHT¾Þ­iú¹v¾\x0000î\x0000î?nÔ×&¨¼¬D_zåÊ\x0015#r\x0001@\x0003aÎ:Ý´ÙkÛiö\x000e<'ÌóÒà8É³ ãgÙ\x0001ÜÂ=iïñ¨6ÚÞ\x000fê8@'ßùúÉÎÖzé¬®ù©ò\x0007ß|«¼ýÆ×Êææzù§_}Pî¯¬ús\x001d(YlÙ\x0010ýH³Öc
¸t(\x000c¸N¬éIÆÔÑs¦=}ï\x000cYíà-A¿Ê/ài\x0006\x0018n®f[Õ**½»Ï¯$\x001a2Kï13Ô?ýI(ÔÃ³-C§Àa]n~ÇÎ Á«úÃã\x001axÿó&¼fP¢¤Í¡f\»Ï	\x000e×`a@m\x001e  	\x0019¯\x0017_¢"~ÚÛt`\x001aC6*\x001b]:9:ÔìT	Ç\x001bô_zåÕòÖw¾_n½t½ÜX-G+\x000fË£~UÖï}R\x000e4È\x001f\x001dm{\x001b\x0015)îâP\x001aä¾Ò<êµ);çuèd;\x001aÔQÄLó÷ÁoÍÁ¬\x0000~uRnä
Ççs\x000eåÇ0Û¾(lÒó¥ ÏñéÙòæ7¿SæÏñ²»Óq^ÞàÒQó[\x0000é¹£,RðA\x001cà­GóFyÒ\x0011\x0015)d%.ÏGlbS\x001a\x0001LèðÁh3\x000cnl¹Æ\x0019®^\x001d¸^±gå¸Õô >CÇ\x0005y·>">àr¼·%þ¯IÉ]/CûÛeTî\\x0006<&\x0019\x0018\x001b-³{õ*W¨Ô\x0019ÓIZÞY-f2#\x0005;²x)7qw÷:àP^µ\x0012Rþ-&<jS\x0007FµkÕ\x0004¨-b/\x001a`®IÁ½xù²\x0015dÚ<\x001f\x0006P¬YQì»Ç\x0003×sÊÏ©|\x0013\x000eE¸n\x001fý \x001b¯I·Îë÷\x0005R:Eg\x001bDw3þ;_êÛ«\x000esçÎòÛ\x000fÿ¹¬®­y\x000b1û)®¡H´·=Õ\x0001,\x0004þÿ­`N*W(åm\x0005\x0015\x0012ÊèWfÎû\x0008oÙoú÷¬/&vìb \x0010>ùò	?88MÿS\x0003¼ËA\x001bôÆ\x001dìgO \x000f vk+XuÚõs
Io*X£\x0006&\x0013\x0019ße\x0013(WÒÀê;uÚ°ÃÐM·±\x0003æ]\x000b2]úÆ\x0001%BÐ:mü\x0012~Â\x0010\x0016ô.(£\x001dgü:\x001d\x0000{"éÝpR°Pð(È\x000b\x0017Êµk×º
1y\x0013\x00063Ók\x0000m8éK³_¸³àyaÆÉó\x0015¬,w
¸{`	ÚoåÏÏËÕÅH«W÷5\x000c]\x0018|w«Lh&}ãóå_µÜ¸zE
\x000e\x0003é¾;\x0010\x000e\x001e»\x0003VíÕ§\x001cpÕ\x0018ùÆ\x0019Ûvþ¸.\x001dóf{
k7uÀ\x001d
Ê¼yÄlñÉË3ã\x0003wò\x001a\x000e¦Äa1Ð
Öo[1\x0000PÁ\x001a@ ;Ã¤0a\x000fæ(
J81Ìé¨A(\x0006\x0005T(94
Æ¿Ùñü4dÔpý,è\x0017¾ç\x0006}¤ß<
Úá\x0013ó9¡ë×Ôi;\Ø\x0019Ø¤¤3\x0008òÁÝ-okÍÌLo¼ñzùî\x001f|¯Üúúëåê{|B
Îã;eåÞí²·þ°ð	¥Ñá\x0013u»®\x000fßX+Ær\x0005\x0000o~Hif\x0005êà#ÔÊÐaå\x001egzh|(OÔmsÚAõ\x0010\x001d\x0002\x0007D\x0015NåßW\x001cddgmd)\x0000
;65[&fæ¼\x0012É9¯õÍM6gss«lmm'«¾oÛmn­úJÍ'ÞÛ\x0002·Wk¾A|{[ñØºSù·;Â½\x001dåµ-%dKò¹©A³D¼ñÊýE2\x001b;ß¼dk\x0014ó·(Ù*\x0015\x001e³­¨gìG\x0003¬l\x0004ÒÙr\x0017r
geJmË}¥\x0015.\x000e²r#bÅ+ühl±Êâm\x001b"o>(ìA@i{ñ\x0010ôµ\x0014ê_8óµ«¸¬Rm?ë\x001bÂ­²¹­úfeªi·Ô\x0003\x001d¬ìjÊvM} ìÒn0i\x001c|ç%é.?WÎ]XbE?Àº3\x001dk]\x0013\x001bä-ËÖ`e§llË\x0000!`û\x000c¨e:Í´ÿ¾àTÎJËeÀ\x0014o¤\x0004ÄvVt¦9ðíKÝÜÚ\x0014C©p\x001d°zB'Éäám?Àÿ«`\x001bÈ£6Ûa2\x001eþë-A)U(W©`ù-S\x0005 *\x0003EÄÁßW\x0005XqI\x0011?ÜÁxVÚB¶Ìãª\x0000Òf&\x001cÊU®ÄÑG¾`?;Ð\x001e¼zþ½ð`¾ê9Â=&#\x0004¤ó\x0014ýpFSß\x001eýVíÏ¶#\x0000Cì²4aìÞB\x0000Ói\x0008Ò\x000c@±=ÍW»ÕX9â\x0002v?\x000b_Ó¢\x0014]ýÆiV\x001eùT\x000eõajYOÀ-iq\x0018ú&½4ÿkBLTOó¨ÆÚ\x0013:BÃÉSñÛr×³òÈøCW§\x0006ß\x001fÖ qyq¶¼~ëFyéÊEÃÚÛfkè°¬oly ä;g»¼Í6:]_\x0012Òtò¥^m\x0005åÉwäÐq\x001b9;¥p
à²\x001aT\x001c§\x0003BYb@R¥¹ ÑØkV0`¹\x00116åôàÎã\x0007¶V\x0018\x000eTÍò÷Ð&÷Ù½%%áçm4\x0017¶\x0011Ú&u¶\x0006yE»p\x0005É\x001c°ú¹íw\x0016ôÓsSÞÈoóØ/l
xí\x0007ð\x000cªTK¯\x001cá\x0017
û{ØâÈ;|^|ñjùÎwÞ+?üá\x000fË;ßz·Ì,.I¹\x001a-¥³YVîÜ.ëwoÎF\x0019\x001ePÇÉ9}ÎVÀ_\x0014_ø/»\x0018\x001d
êEy.×y¸3\x0016Ï©JêþPJ8ª3õcå\x000cR\x0015\x001e·8L-w¯2*=Þæ¤¾5£R5>9í7C9¿·ÓéHIÚ)»ê°YÙÞÙ)Û\x001aØ¶¥@p;?
Ñ$>Ãb%é×ä{
R \x0014·r ¼$lÍyî²Ã\x000cZÈêA\x0015¥N£A¯0\x001fJÆ\x000b+FVì§(tÎîè\x0008O\x0019	/þ\x000fÑý(=¹\x000e
X\\x001bBÉÉK<ÔàÌ%¢ðÕÛMÊ`O\x0006
§âï\x0014C.eáørã#í`>{Ó\x0011_Ø:ån¹íÝ²¹»ë·tùl\x000eÊ\x0015ß\x001cÜãò\x000bü¼¬b\x0011*ê6ÊB\x000b¤m²mÈóÐÈPyñÆõòÂ\x000bW\Ç\x001cÐGÉò*2e\x0019\x0006Åo\x0010÷DU·\x0010³c\x000b<@{¡²}U¨;»´öï\x0005h®Ä&í¦î\x0012P\x0010c\x000e$sdÁ6922fú9c×Ñ$#\x000f¸³:H;\x00010<Ë~\x001fx\x001eùé_«Øp
Î
K\x0017\x0002í§+=\x0003ê}¾G(\6\x001b?=#yNK\x000eR¦&Ëds~­k>\x0018\x000cÂ·MMè\x0013\x001c_aÛ\x0010u\x0018Á?Ã´í	u§{ÈXÐ	¦_ú×v ¶;oÆ\x0012Ú­*È>úG8\x000f\x0002ÑäÛÄËô/,¨ò¬ý\x0013Ûrt¢´û\x0015?ðÕ¼Åøú©x
6\x0004\x0005ò 6©Äºù\x0000µ½¤)|I\x0008V\x001cQ°03L®`µ!Ó\x0001\x00193|ÿ5Á;#Ï¾Ó´ze>\x0001gñ²\x0006Âd¸vø¡[³ãïó\x001d¸k\x0017/¯¿X\x0016f§ËîÖVÙÒ\x000c\x0018¡ÛÚfàbPãl\x000c
\x0016[
1à\x001e©p(X\x0007êúÕ«Ð9»VÂ>p%\x0006[uØ(Vê¸cH¡©@
´*.@á³Áp\x0001wf\x000c0Âl¡\x000c4\x0008	ùÐ\x001e÷ÐÈ?ÄFvÜ,³4\x00154å=
ùØ\x0010\x00100C9¡\x0011\x0010î´{m>
u:!\x001d=ì'"Àç\x001b¦_\x0013¯ä÷tå\x0007`¯\x0013Ò
õ%èé!^\x0019A\x0016EÀ\x001b7oÿæOþ¤ü«\x001fý¨¼tëV\x0019\x001c/ÞòPýl<)ë÷¾(»kÊÐÁ^\x0019D¹ÚÛ¶2Bª^"u\x0006d+X(\x0004\x001c¸:ð\x0003[GÔ·ï-a³2 %	\x001c«\x000e\x0007Qj2÷Ä£¡1oéLÍú¾«áÑ)=sKf\x0019Q·ÜHfüaPÑÊ\x0019&ÑqJ ¾¢pN>XÎMýòó\x001bR(\x0001ð\x0019\x001e[\x0019R\åëÕ\x0005Ë\x0014\x0005+;(*H­©<ÝÕ)kÂ(\x001dá	[ÓÁ8ÝaÈ\x000bCM}µgì¬~Ä+ò±\x0014Ïç¦¦U/ÜÚ>¤|;\x001bkeL~¼N®Xæ­/v¥Äâí©\x001d®,ñ\x0019ÇXYf¥ÉÛ bÁ?ÚK ü½µ 74\x0001¤SGõLº(WL¸öÅë×Ë¥K\x001coðíñ£A<v>\x0010\x0005?à\x000fåoêâÉ?êÁ\x000fáG2\x0004ä
³/\x000c~¶×n$\x0017öÿ/1Ó ¾@uÖ\x0006\x0014\x0005Î\x0014R\x0012RW¼5èöµÃÝ_Rè\x0015\x0006\x0005E~OÑ\ïb«lðkC·û;\x0003\x0007\x0016kÂÊDDº¦ü@XÅ\x0018ÌË.\ÉÀ'Å8ÜîÁÜr%E\x000b¥~²Ê0Eºëæ|TÇ\x000b\x0016\x001eøegE|jjÒ_\x0015{Ñv\x0008¨rE½sÇ]&q6Ð9 û¯°\x000e&uÞ®÷À\x0018+L[@m¦ýi@òI;m\x0011ñò97WZøåài:]°\x000f¤¿'¡
Ôñ 7~CÉgÊ|Ë		y\x0012¾ìWøQ\x0007´¥_?¨ó\x0007(3cüÞ^G²1^æægT\x001c­1'ÜÏ\x000e{Bõ#'8¢\x0018¢~UôÊ¤ígzm:ÿk\x0000ôP\x0012lgµó§Çíôç¹W?ý ÇKw^OaÈ¥Â\x0008=I\x0015ø¿ìC__xrd¼\¾p©,LÏÍÍ²¯Ù/\x0015¾-EÈ[\x001b[em}ÓJ\x0014W0 T©?\x0017i#\x001e@ýF\x0004\x0005ÿÜ:Tî\x000cvvw\	\x000cr\x000cä¾ì%wù\x0012¸¿qeëYÿ¢ÓG#mBÂ\x0003=	Ké\x000c\x0019iR\x0007Âç¾FÕqHaP8î·òwî4Óô\x001c¸*\x000bç¼\x0016m!KñÊ'ÁÂ\x000c\x000bL\x001aH\x0008Â´LXIÜl\x0014\x0019\x000fÿT¦X¡\x000b¥J\x0004È
%\x0005>à×L@¤\x0007fg\x0002"ü¾%[<Ã/\x001b!öãã2Ár#+3(\x0001J\x000fÜÎà&|><·¸T¾õíïý§V¾õÝïEÕõøÂE®,Q\x0017Þc\x000bîîåñg½­
u¼J(\x0018i\x00051.\x0000U,ö\x001c7Ç,³} gÓÃÁh\x0006vÕ¹Fø­½#)wekÿ¸ìò©<¡\x0007yéì£\x000c\x001c\x001dÕ]gPJÞÔ|\x0019+Ç~¡b¤\x000cJ¹\x001aÔ`\x0000Bv¨\x0003\x0003Ü\x001c®Á}\x0010¥·ÙX\x001d\x0005	Z!Cf\x000edÑñ	¸á¡þÃwÃè4"jÌ\x0016ã³H\x000f&t~*«ßFrlW¤\x0007%ÕdÔ\x001d<@¦\x001a\x0013GjsØ
¬©g¥ìºAèBæQJ9'561^¤Ø\x000eII¼~ùRPÍÇË¾Úã\x0014ª!ñ\x001c¹?\x0019\x0018S\x0013\x0018.\x0007\x00120®=aëÕ[ó
C;:ô¥«´	êU\x0015ÞèE\x000eC±SB_\x001aò]åW^\x0019S\x001bÖx<\®¾p½¼ùÖ7ËÅKWÊµòùgwÊÊã5}¸,-./\x001e°)\x0012Àäfx²JÏ¤,Âõ_f#S®+Õ'vtæ@d1êÄ,4wâ"H·\x0011ÚìñÖ^\x000f]gw%P\x0017r#|c\x0002§\x0015`d\x0002EÐ6¥OÝFõÅÀö@Ú\x0014
\x0008ÌáM\_Ì©íÎ'f¦|&qM'÷óÅÇëd\x0004?¡!Û¬É	vÈ±ñkí½A*SÉø\x0019Zì¿\x000cx\x0002íVædçÌ~\x0008Ï=\x0017/\(7¤\x0018k&$¥§£8\x0003ezjJu\x0015«$(\VÚ\x0015A¥ëò\x001dô¤IZaTûµð=Ä¤VõãráâR\x0019\x001fWß/Å7rYmå-[¾\x0002réâùÂgµ\x000eäÇ*klSbÊ\x000b\x0015ôc£â§\x0008ÀÏÈÊ-y)OòKz0I\x000baôßrh\x0017×=ac3@ü\x0012Iz\x001a\x001a¡ÛøÉõ1ð\x000f×¨Ma'\x001fj0&Þfx~io~®'¹ñÁôèKD\x000fì3ùç%° ÃY;¹D½2¦z`1"Üx\x000etÔpy\x0015ÈrÒÁ	Åë5\x0010w·wó*Ú+mg.\x0016_Z^R\x001d©OÙß·¬ø"PÚ\x000b|Q{uÙhêv,y|sÊ1>U>WY÷Åaý£øÈ©#?èl`¦;¦\x0017I0õUo¯6~î«EGÛéÇ<aðR9³Ï§ñQnìÑP:Úº\D
¬÷x\x000e\x0003|ùáG\x0018b"SxÛ]XÎ\x001cSGï]¿þþ¾\x0004#¯®>ñÇ7··ð±"pYç\x001a+Z;\x001dwêBî÷äj\x0005Ô$Ó³x2R`+B!\x0002^Ù2ñª\x0016Ù½m\x0008\x000f\x001d+\x001a0aq\x0010ÌºOP@þãJ\x001e~&/=ÆÙ+¹à.\x001a2,ÂEÇC2r¦S!\x001aÒ\x001f dÂ$«&L7¬=\x001d!\x0012{Dè*]?BG°aud\x0016:ÕÓPðA:\x0011::	²+"3\x0015´g<,ÛæÛõ,\x0013tww7-Y\ZrÇzþâ²°´\\x0016\x0016\x0016ËÍ[·Ê{ß~¯üàþ°¼ñæevqQñD\x000c4)

÷g?|PÖïßõ¢jbjdRf\x0014Ô/Ò`
\x0016\x0007#yùÎß
T\x0007î­&Õ-÷X¡LÅu\x001c)É	\x0003?ÛÂ\x001cë<\x000e|V\x000e\x0017\x0019*\x0013s\x001a\x001d¦ÄQ5[É\x000bu¨Î'öh¼nØl\x0007[ÑRÂ\Xé\x0006O=è\x000f\x0016:L\x000b7 ©pkL[\x0015Ö(ÚÍý®?²ÕD\x0006\x001c^Ï\x0008\x001fgå\x0003\x00136±e\x0007éXè\x0006M\x001c\x001a¨¢Ð=àû8tæê¨\x0014vwgÓÃ¹¸´PwwËã;_úÐ»ZXÈwW1Ó¦´ÜM0àXû\x0008yõNÜ+Ü{\x0016|tæfP4åJ2/°òÄ*§¸êA\x0006%KTK\x0018ü¼\n	ùöúÚzùâÎ\x001dßdN\x0007;1®¸WÎeF¶\x0011±Ã\x0015d\x000b0ÏÂJÑå\x001f|Wè\x0008\x0003O\x000cv¶;}HÏ½$ØÔÍç&4ÏrÇ\x0004iC½ô¾*Dxdë.|0XÉpÁ(/aÐ.hÛ\6
ë\x0001±Ëý\x0019h\x001a¼-
$×@m\x0007x$
\x0014\x000bè;3\x0008ncP¢øQ|¸÷âùóåÖK·ÊÍnK\x0017./?ÿ\
Î¾W®¦&&Õ/20|&K=ÈÊ-ø\x0008}ÁSÜêçtK;\x0015xùü²hæÅ\x0016µñÃý²±¾áí{&\x0016\x00134<zôÈDv<R&Ýç©oF\x001bdõ¹!$£tY÷
\x001a{?>Ð²Ø`öµ_ýlþv¥¬±ó}Lj×\x0013ü&:N?Ì0ä\x0007æ§ËÚÏ NÛ 
zÂ¡ÜEÑ\x0010þêßÄÓ¼æ\x0002\x0004ðëÆÇ.\x001aífßð·)Ì¼\x000cU\x001at½<!3È\x000f1|ÕËìéåÎ<óNî§:Â\x0014§\x001cÏÍÆîî»@Ì§÷3ÀU/hÍ4¢\x000fëñ\x000fpyqÆ·i`=\x000e2\x0012ñþ|F®ªä²)_\x0017j;a£Ä\x0011\x0017¿\x001e\x001d\x0004Å
÷Û¹g2Cï½|ë}ÎWmr_\x0014«m\x0006×±¡2»0_¦ægË½ÇOÊúÎNÙ`ûA$íK\x00001Eó·³t!©L\x0006ã-#¸tÖ\x0010°jl6²ÚÄY-Í­5(cÊ\x001fBM\x0008yBDÎn]S\x0005µ\x0019~Ñùaä\x0015AÝ AòÙ AàÆ*Z\x001dWèN+rö³°¶·1ýjà1<\x001d¶\x0019¥F\x0003IIâ?eÌN¥³+%FÞ\x001cD\x0019#<È`¹Êê ù 6|UDw^SefOÝLK/_y¥¼ùæÛåÝo}«|óïHz«|ã\x001boW_}µ¼õö[åå7Ë¨â !q\x0005\x0007Ê
dQ\x0003Gl1)'w¾(ï~Y¤´
++É\x0016T\x001e(ÏÕi~Ä'ÜS%EÊ\x0007¡58óºþ¾Ùô
úR®8¬ÎJ&Í¢{ê½%¥Ý÷hI¦æËÐè¸g#j­i¼MÃ1?1\x001a\x001e6\x001d.Y\x0019âç0\x0011å«?óEÑ-& :ÝÈ#h±¿ü\x001c¦O¸ë ¤f94e¥
Hé$HÖ~ÄwXüà°$]<ÞÞX+Scå\x000bçËÞöf¹÷ÙçeTáåñº¼\x0001ý±¢r\x000c\x001dirÄ\x001ddt'\x001aÜQ¶mÅLvÇ)qÀ?ìþï\x001d\x000eÂ\x0013V4²zµ«4GFÇÊìü|ùæ;ï\x0017®]õçÖÖÖÊ\x0017_|VîÝ½«úÞ÷y
>OÅÝGtÆ@®ÜP,Ú=\x0004{â#úa\x0012<3oø)\x000c&<I~\x0006Oc\x0000 \x0019ê	\x001an`¦\x0019\x0008?I;ì	uZý°î°Û_\x001b\x001eí\x0014>ÐVQ$¶¶ø\x00084qâÜû3x(?ª\x0016K0ß*\x0013 B©¢?¥îFù¢$\x0006Ú$\gEd^\x00131Þ\x0002»¥	Õ\x000b/¼P¦Õ7@ß§Þ¶\x001c0Ac\x0000õ
ÊL}18=
\x0016aSeS¸tK>Õ&òÈç³è»­hvÔ¶áÇøÄTY__/\x000f\x001f>òö)êt(\x001cÙ\x001fÒçÑ&hÇÎ¦\x000b½ôÎ´÷Cz\x000cÂ×q\x0012Ó\x001dÌtÛ&ég\x001eù
'"ièìV¶µ\x000cè\x0015`õ×²£ d8Ò\x0007µòE³8EoU
\x0016
`\x0008\x0006y9?!~¸\x001a\x001b»<
Ýú×õ3ÊN»oÐÒÿÄ333¦¶	}ÄëÆ\x0011Fç%*+;ye>£:n?´PWPû%_Ò=!í\x0011æ´\x0002ÝÆvütK~0Ý#LÊcïÕG<÷ì\x0011Dña\x0016}Â\x000cü\x000fßþæÉÚúJÙßÙ.cC\x0003ert ÌÍNsKs¾Ýõ\x0013u¨+\x001bÛåÉÆVÙekP©vb%k@¬ÁF\x0002ø°,\x0015ß\x0008¥ºy4\x0002J SÉÊpÅ4qÍ.aþ\x001fÂ\x001e»\x0019.{2(·\x001bXªä9:
	±Ìñø¾ÒÂ\x001cß«S|u,\x000cliX0\x0004ÄåßÓ»Ó\x0017d\x0005¥ðº\x000c\x001d°\x0010
2|8`
$\x000cúÃtóÎrG|Ò¤¬ y"ät\x0008|\x001e ÍïEÅLcVÏãåâÅ26>Ræ¦çÊ$aÆ¦Ê \x00145	8?ÀÖÓ\x00083lÕ­\x001cêùëF zØÞ*[÷îÛ?ÿûrû\x001fÿ®\x001co¯å2>>Xö\x000evü&ÚîÞ\x0006\x0010)M\x001d­£d\x0017Ôÿ|°\x000bdwØúS8>´Ý9ô9¬­CUºï}ÒàÏÀ|ÐG§gËÜke@4¢\x0017ÍFfPÅEuDÌÈ9ø\x001füå5gÊüo×CÖÕYþÙÀ»îMý8#Aºg:È\x0010néÎ\x001b©d0ÃxÛ\x0007ñ\x0006ÀÜâV×3È%§¸±­²þäQ¹yýÅòÝ·ß,>û¬üì¯ÿ²Ì±\x001a¥ô´â?û(µ²ÃWø\x0019þQª,lOP\x0016¶ÌÕBÜ\x0016Yõâ\x000c\x0015-åÍ\x0006k¬Fsà?¶\x0012·¶÷¬l]¸òByéæËåû?øa9þ¼Ûí\x001fý¶üíßþmùå/á:ä\Ö/ÞMZVspq¾U»\x000b.{°,ÌV·gÛz@Y²ý$O­\x0007l»\x0000u8Àü¯Ì\x000cfÛ¿
ítÛÀùCêÀÿÒ\x0004õË/¿Ró©Wp¹¾ÁåV\x001aÙ\x0003XÅbÇs¼Æ­6\x0013îç)w\x0000Ê/./KKKåòåË6©\x0007ê³Q?ùÉß>ú
ú\x0012K\x0012£~üíX¥K|ÈòºÏRæÈI¶#ß²¸4ï;¸ªåÁýGeqQ¦ÑòÛßþ¶Ü¹sÏÊÄØø¤ú\x0013VÐâ\x000bfoû±\x0012-y&ÌÛý|Ï\x0003>í\x0004ti\x0012d<çÓ¤þ\x0019¦Î+Û"\x0008 Çð\x000cÅ>8I\x000f|©ÓÁ´À[ÆáMÊôO7 Ã##ù\x000cF¿\x001d´ar8î;¼j\x0015Äal*i·GÒòÿH3Mr\x001e\x001d¼¨\x001c\x000bb·äúõë6éÃ¨·L3¨ìÅÇ>'ú!iø\x0002ò\x000c\x001dØ\x0005L
\x000cWÇN]$ð\x0010gä\x000fY\x000e Nó©	¸e¸Þ]Ñ¿$4I4iÁwq¡éç3ý\x001a\x0006þðåk'[9ïnmI
ÔóÓ\x0013jôbÖ`sß\x0006ú½²ºµS¶\x000f4È*-¶
OÔqû;w\x0012Dwþ\x000cLÍ \x0004ÃÅ[kØ\x001d5b:g±Ú\x0001Á\x0014ó8(\x0019\x001c4P*\x000cÈÓñ\x0002TR=ÃEÙê
)t:\x0010"w\x0014¢Á
V£,-,6Ç¡7Sþ\x000c	
oºÌÉ|ºt4y\x0001Éü´\x0003õ@\x0012\x0010î\x0008\x001fÀ\x0000³\x0016ÒrT\x0015\x0011cãs\x0013lóÑ	òM(î%÷l4;GüI\x0007ÄÎhé¸.\x0004«J¼ÙÉ
\x0013@\x0018Î¤
+\Ñ¬7éR\x0000eªAT
wOñå¯Áýxs½ÜûÍ¯Ë?ûIÙ]¹Wæ&$\x000fC\x001aøw¥(qâ¨tv\x000f¬`\x001dt48kdfKðP\x001ddGiò\x0001n\x0014¬=¶\x0008%'q+?Ê\x0016«o46x\x0011\x001d\x0017uêmO)Xã³Ëe`dÜwA³jÊüae\x0013vùïºÇÉ»¦â<<WõÙ­°×¼\x0006òo\x001aRBÛ¿\x001fà~´\x0001êÏ×8/ÕE£;\x000bD³Ü\x0018@|\x0018\ü`\x001b:§ãóÕ	â\x0005÷hÑ\x0011s]Ê{ß|»|ÿ[ïÏ>øuùéÿy\x001fV\x001dJ\x0019\x0019q9\x0014VeU²rÄ í·3m
\x0007¼\x0005ø¸µePòÎ
\x0016vú"Îla\x0016ÒØQp5¶r¹ÃlWñÌÜ|y÷½o÷¾ýÝrõêJb¨¬¯®ú\x001b|\x001füê×V°Ø\x000e£}]»~£ÌÎÄdlHò\x0008¯¢N?\x0001·¬1÷å[æ\x0005ÉÏ\x001c4ÌKAãU\x0000T\x0001\x0019>!Ók·ßÚ\x00042ÜYÐN·
#c£®Oò\x0001<yR>úäãr÷î]ß7g¾+
¼¼]+°,¨oO\x0005\x000bÈ¬ê,±rN¶AÛá\x0013ct_\x0017.³â{õÒÕ2%% \x0015\x0001ä\x0008zè\x0017éW~üãÿ`È	\x001a7ðC\x000b´\x001eJ\x0006égs\x0002[5\x0015¬äËÐ ²>¦Îrj¼¼òòkî·¶4NÿÝû\x000fÊßÿýß+\x0006/\x0004h256azrÀf'\x0005CtÖ
V¦LMS?h+X`
u§\x001d\x0006\x001eäam\x0014ÛbÒ	\x0010çDeKà9êß-Ñné_ß\x0013\x0007øf§ß£9óöÑ\x000cÑI»à9ó¡Íd\x0018\x0014\x0008ÌZÑ'Åa¾Y*:UäãÆ×]É§\x001c3
â´Ó{õ\`yV@4Ó\x000eÀ£Ú/Í¯\x0005´Ô4\x0003\x0016/q\x0005î'²\x001eR\x001eÒ¿\x000eGdDE<\x0008Ò?Íw.Ìp\x0010/,Î
ËÎ\x0015>²¹±*\x0002J[÷ÛI¬Dlíqyá:d1S/Û0û|\x000c \x0010¤O\x0003b\x0010p§./Îæ ¤²-È2±{\x0007´\x0002)Btû?\x0018u\x001a\x0015Ý\x0014\x000cõÒ¤ÐO¤ò+\x000cïTéQ\x000f(Xl=7
ÖÒ9+TøùLü2+ \x0018f]!M>m¨Lº@/l#üÎE´'¿O×hÌ4@:M(:J>¶ÉìU\x0001f¢Ì"P¬h@ÌJé¤ÔZ\x001dW\x0019\x00070'{\Q°ë&G0ª\x000ewºªìæµ\x001a\x000e\x001f`ÞÞÙ,«+\x000fËÃ{÷ÊX¶ç²N\x000e»/ÎÎ³¥³ú°|ò¿/ë÷¿(3\x001a+YÁâ39tì;\x001axQ°ö¤\í¡\éë9U|¶¸-Ü×åÆ\x0005|î·ÙxÁ/"¨ÜÈ;.=SöIP\x0013heB4Ïh ¦Ô¾÷èCÌ¿>
\x0016|\x001d\x0002Ï@Úëºêëß4$ ?f\x0006["uÑµ&Ë1#¿ä\x0003ÐÈ'·às§\x0018Ï¼\x0006\x001fh#\x0011%qtl°ü·ÿÍ¿²õëý¬üô?ÿ§2­\x000evDü\x001aRG²F§z,¥Õ(¾¬`>5\x0013\x001bþ'­$
¨¹:}øB\x0015gáâÌ\x000e+W;âö®\x0014ä\x000e7¹\x001fñÉÙòêk¯?ü£UÞ}÷Ý2ª:B¶î|ñE¹}ûãòÅg\x000f?úMùòó/\Å¥\x000beaqÉ2JåTe¢Ýâ\x000f_\x0018\x0000hÏG\x00014&Á·Iù\x000cC\?7f\x001b¬`×\x0011/ô\x0012Ú¿¶§ÿYÐN·
Ô¡eVéÐN\x0018\x0010ÙGO\x001eû÷ï;÷ïb¤úwW¦ìÈdÑ1Gª	rUÚ1ÓíAøÌj\x0011W!ß¬@(?x
­îç\¦P¶ÿãü± A'}\x0005@ÿC\x001cMûüL\x0018âØSIHÀ­(Xê7èO.^¸\^yå\x0015u7ûVÄ?ùô³òàÁJ¹v-n\x0007çºàeÐGÿH»\x0018\x0013\x0003<\x0001±_@\x0001|Þ í\x0015\x000cÉ\x0007\x0013j~`R´'À»¬7úY0äKüz\x0005*ë\x0016\x0013$LÍ£,Cm2\x00042ÿ¤\x0001?M<<\x0005M[Îrpö\x0015{nUµkk`AÒilÆ!\x001f KSe'µAuà©¬>"\x001f(XÈVò\x0000å;xùT¨GÛ4ßIÏsA}[]®(kï9!ÓªóÂD\x0001}\x0016´Ã\x0003>&
V<÷dÂq4.`fýÖ+eÛ¹Ð«CÇ­pà½sãÒo\x0018\x0007ËË7ooÝ(\x001bk«åÃß|à{L&¦§\x0004·m³bÁÇY$a«qdD=8gzØ\x0002"3\x0014,_Í #\x001c÷_qØAö@\x0019\x001e\x000fhäVGË
\x0015£A\x001a×éÊ°0ÊSQ5'eµ9È@­\x00199gôìWù)\x001cèL\x0005ô\ñBVÎbæ\x001fè·9ª¼\x0001òM¬¡ý\x000c¤SúåxM§\x0001Ä9¯\x0010z-»9¯Pñ1Ô·Þy×æÕ«WËL\x0011êpÇM£']ÓOE7m0ÍJSù\x001dín\x0015n^?*Ó3¨´jû^©úòóÏ40Þ.\x001eÞ\x0013Þ/+\x001eºìSS3epd²\}áòÚõ«ep»ÜþÕÏÊ;\x0019Íg§FÊ:dÝÝZÉRÇc\x0005Kê\x0012ÕJcRuÍÙ«}rî;$74O\x001a<\x0006c\x001baGvV¯\x0018,\x0016Ï&\x001f:U	(7ÛQ\x0017M\x001d5í ËßJÁ\x0002²\x001eÒ¬å
hû£pÔ\x001dJúg\x0007Ù\x0003øuý\x000e\x0002t\x000bÐ³?t¬øD´óò\x0008\x001fz¼²îï6²¨Ñö\x0002ÿ8ÃÆ*áò¹Åò?ü÷ÿ}yïí7ÊÏþê¯ËOÿâ/Ê¸ø9ÄV\x0006CîÌBØ>C±¥\x001dòV­Úe¤¡=d,è`ÕvÅ+Uâ½Èó\x0016#×0tdnÊaKy\x001f()
Â¯¾öòíï~§¼ñ·ËÒyMNÄ\x001f¶¾>¿ý©·¾<~(eëóòÙ'·ËÊúoØ§1!î®äÌ¶\x0008\x0007Y©
N\x0006d½tùØR¾$.\x0001éÞT|¥\x000f[%U÷\x0005Mz	n7}A©ÃÂ·gA;Ý6 ¤0(S\x000cÔ\x0011ü¦ÿüB)æ£'6	_CM\x001fÐ£Ñx9ávÍàÇÀ÷ÒK/ÙDi!­ýíX\x0011\x0006·T\x0010:13h²EH\x001dÐ¾ m·³ít3þH=yð89¸^<)Ôg}¦¾euu=Ú«úõ
ñAÝüÒÒäa6d@r\x0004eCùò<>Jû}zýª|¦©§(\x0002äí¶Ñ)íu\x001eð	Zà1
\x0011þÄ'Lòg·=ñ9Í:Ú´@ì\x001còÏt(·M¥\x000f\x0010¶`úé*Ú8»
ØÏ\x0018q3_Þ\x0008\x0006|Î²¢\x000fy¬éC\x0011\x0002ò9ÛÜ¡\x001f´1Ég»6<gùikuÜ´SäÇ3ôeÙxnçÕ\x000füV\x0003u¹\x0013pËtê4Óü*
Vm&d^¹Ï½ð5\x0018«òµ{\x000fÏÝ±I@80y2ôêìàû\x000b3Såúåå]uìï|ãë¾ÔðK5'\x000fwËü:\x000cîæàÍLù9)	óêDæÆFËÂøH\x001d\x001bQÁ2£çiÙ§Y=²Û·D\9\x00082ìòYÜxå²¦í]Õð\x0003\x0001P\x0003õ3\x001dy4 ßù"òs¬^:>é¨rãUú¤áT¾\x001e0)\x0004+ÝõO¶ªÃÐ\x0000\x001dZP¨^ºy½|ç;ß)ò'R~ô£\x001f_yµ\ÖtRjÅ
\x0011¯ÈºA2ûi*
^ùÖåL\x0017P¹ÕK'-£`\x0011nfz¦ª4ïlm­òé'\x001f/>¿­Æ´_&Çy³sjêè¤üNåÅÅrAáêêáÝÏËêÊcù\x001fûUn¥\x0004ñC
ô¬LaG¹â\x0012K\x0014å¸7Iþ
ë\x001b\x000cä^ÂÆ]´ÓüR\x001a·hÙªR]ðù\x0016è\x001e¬ÐÙIÙ\x0012w\x0015Cá¨2Sìào\x0014=Ù\x001d\x000e~ÉS<jà,qÔfúóÔ
§zôö´bÏgà\x0003º"Ï«Vj¨Çtª(;Ûews«ììl½rÐéøM.êz\x001c\x001d<·£j#¤\x001bí\x001eóËËå;ß}O³È\x0017Ë{RïÝ÷¶èâøî&²à7gÜ¬£\x0005\x000c(\x0004
)ÊU\x0001~ºÿ(v®\x0017!°¢ÑÙZùR}\x0015ÜÇÆÆË5åû\x0007ðÃòý?øréâåPüöX}Ù/k««ec}Õe`ðèìhPB¡P§L]ñ±_Þ\x001eãvsÎË1qAOæ\x0014\x0017²r&Ì\x0017µB©Â£\x000eRf¿AÛø÷ü?ÐþÔL×KSF0Ê\x001c\x0001í×@Úk·³à«y\x0016°2¢\x0002\x000f\x0018 \x0001¾ÃGß2¿0ï\x0015i\x000f¢î§¢ý2 Ñ\x001fð\x0012·æ\x001d\x0005kÒ«Ûï¼ó_XA%}^V¦ÇUoõÀ,}"î}öÍT\x001c¸wô=pFË±û±\x001eð\x000c\x0012&éIL¿@I¢è_^^ò[¦\x0000eZ\ñ\x001bÍôwù&åNta7­JI\x0012²@ú5À¯çÃiúê4ß@¿0i"ßÔaúQ'Ð
âÏ9h\x0002É,SÖ)2\x001aÈ\x000e\x0005\x000bº*\|¼Aòá"[
úï
È>éÀôÄ\x001bwû\x0005m~»Ð®
TeÎr\x0003\\x0004\x001dôKÔ\x0019t\x0012\x0002RÁêÅèå\x0003Ô\x001e:í¯\x0002u¿Õ\x000fàoæáà7taV¤ô\x0005Â\x0000~ÆO7¨Ó\x000fèÙÃû7ëøM?dPæ\x0001zN´+üOÿïo_9YÔ\x0000ûòË/[/¿äF÷«_ýSùû¿ÿiùüóµrõê·°\x0016\x0016=noq©!w31 \x001cy\x0010àM=
{ê\YTä£ËÜÇ³ÝÙ/«\x001bÝâ£À\x001aðÕ!t¯Wèp$<\x000cÊ\x000c\x0017\x0008KB2\x0010©dESN¢{¦:5/¢Ãn
©Ñ\x0002A¢Á¬zvvÞÏòô\x000cÙ>oü¸Ã\x0016À\x0000ð¬\x0015,òÂLw ¦û©h0¾JÏÃR2³\x001bÕìm\x0017:ÄW^¹UþôOÿ´|óÝwL\x0017\x0011º\x0006Æ£SVdÑ\x001a¸4\x0018{»HþÜì¹\x00112òÏ9à2©ä©~zûcoã°µèÎ\x001cP=²âÑÙÝ.\x001fÿæ7åóÏ>\x0016o\x000eýíÆõ²¦\x00195çª\x0007ÆË\x000føGåÚ\x0015ÍD?þMùÍ?ýCÙ~r¿Ì(àùùÙÒÙÞPZÇ\x001aL9¥²\x0008·ø0\x0003¯¯H\x000e8äKYY©b\x0005Ëgù7x$ºqówñ$\x000b,`11£>à\x001d²4ÊVåârY>wÁ«X\x0014\x000eÙð9?Ó(ªbóZ\x000cÎ\x000eµë'Í¯\x0002Ì\x0018Ã\x0012òÂD|÷\x0002à=3\x00141\x0000Ä2\x0000U\x001eêûPÌþA§é¬÷íNºR4Ët\x000e\x000bâ älíqyï~\x0019(W®\.ÿóÿå*oýëåîg÷ÿüÇYæFFËÂìû^:ÉÖ±ò:ÒÄE¼98\x0011ý'Rf\x001aºÉ\x0007Ú8¨î+1-\\x0014YZ§¯s\x0018f5ú°l#oÃRr¥|]¿þ/¡ý\x001füqY:·,Å:dºùäç?.ëR°8\x000cËÍåw>ÿÂ5\x001eX\x001eÙVÖB
öcÃejbºOÙ\x001c\x001e\x001dR;¥¿M{\x000eYQ[í®äç¶ã+ú\x0007ÊÀø!_®\x001fÕG*¹yÛ2	\x000b6["iS¾gA¦õ/zÐñË5Ê\x00179"/^\x000cÉÁÔ2 9Á?¡mgµ*¡¦%íðïQ"wÔ\x0003ùP.î4zøðaùéßýmwÀ'\x000e«§äMÚæ­ú-§#?\x0010·D»\x0003læ×gM
4v\x0016èºS;'}OªÈ\x001f~¬è¹¼BÏôÔ\x0016\x0000Ü\x0000Ò­ó\x00073\x000eö\x001cX\x0001§#fg80ÜzHØ´\x0003<g\x001fc\x000cÊ*|Kå'Ê\x0011\x0003/aÛ¥»J\x000bÈô4~ö¶rLPû¼H$;ù{\\x0000½(¦¼U@~rOzFý·ÝÏÊÊnù¬q|³ì­Ç\x001aÂïÛo¿m%»íHã6	ÎOEÄLh\x001f\x0012OH{\x001d6íµ\x001bç¥yNÚ\x0001âfýCÃ³!dá, ÝgÁúRÄ)ó£\x001f\x0002 %èò£\x001c®g ¦§gÃÐÿòo¿ëÅ«\x0005(«+åþ_

ÀÇ²(mö¥k×Êk7o\x0017ÕØ¯\<_®¨\x0003âM5
îç4[,ãª\x0013uúÃ¢h|xDÈ=TC\x001a<¸äN AÃ
\x0000­t0TN!ðg°pÍ8Ö-¤\x0019#Ó-A0JH'U¼*Õ\x0005ý·ß¨\x0006%\x0004O9 Ll\x001f\x0012Ô³}ÙsÕJ)uí@¦
\x0002Éø^\x0005ôüÂ=\x001batúÑ\x0007(\4\x0003
nÌ>ÿäO~TÞ|óÍ²´¼l¶\x00015føbÅLÆ×
|»<=\x001b)Ð¿ÝÍÍ²)	M{f6ÎYàÏ'TØÚÝÝ)+\x001f­õué\x0010\x0011½¬¨ìÑ©(\x001f.Ò»pîfsjÜ»åá;eks]¶Ê¥\x000c\x00107\x000eLûÃ \x001aÜ¼Õ«NóU¾×LþÌR½Bb¤ÎèzAÂs$\x001b»f\x000bzàpîÊânßË£A×ý¹«gT
gt$ª'Õ©\x000b) é,\va¸ÛÁþáÖ3Ú~\x00167Ù \x001dxÉ.@^U\x001eVùP\x0012É/å¡n¤¼\x001eË¾ÏJ\x0017.	eE\x0007ó0Ô«\x001a¯\x000b/åm0ë°Ñ\x0006¨_\x001cÊê×­Åo:ø7Þü\x0014­\x0017Ì¨õÕòðÎ=o5r)ä\x0018²¥x|\x000eAu{¨Ø1æ{ 

uB{ÚC®\x0014ç2Ð\x000eèL?\x0007Úw [¥z[òù§ÿÝ÷¾õ27¿ <¢m2{F\x00169c³ªþ\x000bo¹Á:cµjU}E(Á!Ô22ËªµË§¶Ïäb\x001fT]\x001ftvmÂ/Þ\ò\x001eRËÒì6\x000c"´S¥\x001a×<¨BI"\x000e~\x0003î§ÿ@Öw]ïýìÙóù,ü]À±¨^¹\x001dþP×cRt\x0018ÀØJeõkNýkL\x0004ÃlÛë¶4¥]ÿÕFÿ\x0003¿qÏ\x0001\x0005Ò¹&Õmò\x0005ñ_¤ÝÏ®ç°·Ñmðç c¨KH3ú<ä&ä\x001b\x00022ÃK~{ñ/\x0004
hs¸@Úk·~î¹¢p\x0016\x0002Ù.À¤\x0011gÈ8fNzÓ?éÍ4\x0012Úé\x0003µ
.« \x000e[\x0003îIù`¢«_l5óÖ%4\x000196Ôã\x0003÷	2n\x0000\x0003é7=®Êß÷ÉI/]E
G\x0002\x0007ýG¡g\x000cIºë±\x0011à©.ÇlAºe>ÏÚÿ©ôøgñµ\x0007ÏÎ\x000bh§ÙCÕ³¢ËZ¹Åxùö²ïåC¸\x001e<¾¡ÿÇ¿ù÷/jpmnn÷ïÕ'OÊÎÖ¶÷e/J!xáÒåraYa43S¥_Ð¬enr¼i&|õÒEu\x0012RbÑ¡\x0006îãýCÏJøX-\x0003\x0011÷òø³%úA5h5j*\x0013dúJ\x0017$á¢Ù.*\x001dî) \x0012wûÌ\x000c}/ÒbÌòMÄ4\x0008ýèx¹dtTÂÉe\x001eXJÄº\x001d\x0005@ø¬ädrmw¾¤[é\x000fX Tvp##\x0012n
°\x000c<4¹ùÙògö§åþè¬\
De°ò
\x0006¼ÇÈµ©òð7 £to¯õ@&\x001aÈ°ý®<~ì-)>U1;7ãK&Y\x001e\x0016An(Xë«kegcËn\x000cô\x001eè8w Æur<X&§T§ç\x0016ËÐðI¹ïNÙ\_±5 º\x001bU\x0007iÍHm\x0013Y±ðG¾¥lYaR^µÊÍÛzú£Ö²¾á7Ï~ÙAõÍ\x0007ùl\x0012\x0003?qiÓxàf \x0018\x001eÕóh	EÕuÌ\x001fü_¸EÝ`f½dô³æeT¬
9òj\x0019T«\x000e\x000cJß\x0012T\x0019DB¹[öv¥¨ò!èCîöâ@;\x000c`8Ì\x0004½½g~Ä@\x0005ya5² Ò.¦5à¾ó­÷Ê\x001b/úE\x0005JpïË/¤Do»\x001eæU¿l\x000bq¾\x0006@\x001d\x001aî6¤gå#*M\x0003âÆ÷\x001bí¦Äà?«kc\x0015k|rª¼ñÖ[åÛßþvyû·Ê+>1®\x000evt<Û$Þ\x001e\²Ò57-\x0019SÜÕÇåá£\x0007ª÷¨#f¢T>«Â´y®\x0000`µ­Äý½d1Vö@Ë4ÑßñCY¥\x001dS
\x0015GI¡P28À\x001b·Oÿñ\x0003PÄ"\ö\x0011\x0000õYC>×f-+µûYø<ÿ¸]ºr\x000c?¨ÂMùyr'Ä\x001eò&¯\x0006©§ìÐÁö³ã\x0010¿Ië\x0014Â\x0000±lD²AÿáÕ\x0006É:ÕÅúÚ&_\x001bA_|kº_Ða\x0005U#L~¡ !úÊaÑÌ@Íd¼{aA:^Þd\x000eº\x0003±\x0003Y^×*¬½\x00117®çQP\x0000 ë\x000cLÈt#Í\x001eø(¦I#téÚ¡2Ò\x0004Fîà£ïã3lØy\x0001r#ó$qHl5#±Ðécf^¤Ý
c/fÐ\x00174u¸G]E¹è\x001bR¡J¥¾\x0010'îc¬	¾Â\x001bLv8H¨ÉQÿü_vM\x0018ì]%Ë~À\x000bÑÀøH\x001fAÿqùÒ%ç\x0007-È"\x0017\x0007;Ms}\x0008)Ý°·ÌÄðzú9Í¶ÝÔ5n@ºåö4\x0006/~7t5Gñ\x001c\x000cÓ\x0006GÂCGóì±:UÜ÷ýpèÿúo¾Ï÷\x0006y­øË»w¼ÕÄ÷ßÄñ²×Ù×à;íóLt»Û»\x001eÌ\x0019 \x000fÔQ3Sç¶^üö4`w4SåÌ?\x0004\x0010k <ôkL¶\x0006£YQ|zG"cb(·:,\x0014\x0015\x0010\x00194S\x0002£C\x0000#;yÿ\x0014\x0016!EHÆGÇÝAÇ'¯F@Í\x0000ýOævÓ
qíÐ³kSºQ!a\x000ez!ê\x000f~ø\x0007å\x0007?øAY¾pA³÷¸øì½wÄ³\x0014d<yÆ\x0001\x0018\x0005)1)Z\x001d\x0001]n\x0006úÇ÷îZ\x0019cPòK©¼b¡A::P\x001dnh&»½±®Aï@q AZØÙs§s¸ÏêÁï²\x0019\x0019\x001d*÷î}Y66WËÄf¦tÚÀA¶eTÇ(R\x001cÞ×3ëRô]^A\x0011->«år pâ
Bib\x0019yÃîÐ¤4XÁ¢aÐLJ~BÉÐ3gEâíO¶q,bv\x0018þÃ­©§ß\x0005I	D=AdH~P®\x001e¡+±â+E!V\x0019Q¬¤L±\x0002ãUX­beP\x0001­H¹+E!\x0013}n¸z¦\x001e}\x0003+}\x001a5\x0019Û&1Ûü(ìÔÜly÷½oy\x0005³5C
¸½¶^\x001eÞ½'ÙÙ-3\x0013Ác\x001aµÒØÙíø~!\x0014¬\x001a¶x\x0007ß}A¥Ò¦ÝÁ\x0014[^´¸üÂ\x000båæ+¯ï~÷û¾+ncc»|þùçåáGÎÃóP\x001d\x001c)mM¶V×Vä~¨°sêtK¹ÿ®ú;\x0001Ê\x0019+s0-hã36|Î\x0002^ðé\x0018úixâ37ð\x0001\x0019\x0015ïX5EQE69\x001f(6_¨#ËLò \x0007âÒmà¥Aþ\x0011ö4¤{\x001b³mÏ
\x0007>ÏßJKú×{æG¡\x0005LzPxi×ª	ä;!\x0008 V(H«¦¹N\x001f\x001e (Qgî\x001f\x001a·W°ègÈ#ãç\x000eÄsä0m¬i\x0002x\x0006£ÍIµWÒä9WU\x001c¦	Ó\x00086\x0018ocooAµ¡M#û /M5ÐOXèIÀ?éÿÔ\x0007ee\x00058<\x0013\x0016¾aöK7Ívúm NjSáÜ^ªú¥Gjò\x0004SáBéaE\x000bÌ6èKÌrÑ÷\x0013ô8_Ìñl
\x001a2ºu$öÛËóËW<áÍ4\x001c\x0000¶ªÜN»zî£Áú¹ö÷¤¤å\x0006¦[gcvQá³A´Kü2Üéð§ËÆ³]»a<H£	Ó\x000fÞZ\x0018yÿ;wËíÏ¾(wî=({âøðØâ\x000f}
«ë[þJÿ´}Vf666Ë/¿\x0014~QV|g¯¬iD'Ìþ±_or¡¥ý\x000byýÛ\x001f§\x00152æ<\x0017Dèp¨TAY(Lßü#\x000cVù9Ýý_ A¿QO±e\x0010æ7
%$c#ÒþÑù\x0010OíÁ¢CâôÕ+(S\x0018\x0001ÜÜi
H\x0018CPi´\x0013S\x001aÄ®\*ÿæßü\x001b¿Á@Ãëù#\x0012^V¨6Ä3\x001a\x00044Óù*· Y\x0008}\x000cì±²Å`\x0013³yßv¨­¾\x000f¼ÒÄ!e\x001a\x001d7¾SO¾9]òÖæfY[Y)+keog·\x001c«¾\x000e¤\\x001d{õJu p\x000clSS\x0013epx <Y}¤x;R°4c¿
Åp¬`Qo(H{4hÏæxå¡áy\x0008°<g~
z¥ÆW\x0005OÜ\x0014ÎÌ$¹d7Þ$âbØéÉé2;7_fff¥lI©­M%­¬\x0013Ð5~5´\x001b|¤Áa\x000fþz`ðgå\x0015Em.\x000eý\x001fú¼a³bÅJWª8c%ÿã}ñGÒÌ«¾V\x001c°, Çü£Üq¿TÇÆõ¨v¡6\x0000ï\x0014S\x0001Ý&XÁúæ»ïsËç¼\x0005Ü¢ðqÞiíÑcÓ\x000b9\x001cÏjæÒäM]V+i\x0014XþÔ\x0015beÆçnP¬àû8+/\x001b7o_µÜ¼y«\x000f»íÞ¿wßç¬>øàË§·o;m¶ÙG>m´.\x0005]sKË®_+ÎøPnhò Ûß«­H X±Ú\x0015ß
C¾{¨?±'RäÇÛËj7^ù\x0012½¡°ÍÎÅ\x0014Kq¨KÑ\x0010õ\x0007/¨ÛÓõ\x001b,xÚ\x000eÕù?\x000b%? å½õ\x000cêÁÏ(¨l£\x001fm;\x0006>ú#&\x0018(\x0018ÙæÓ0Tª)µÉ¯g\x0002bÓ`0$=çC:j(WìJàæ°¢#'	ÄÃ?1Ë[ÛéUÏ/Å\x0003gø:&\x0002^½B¶\x0013\x001bJãs&§
Ï´âYåS¦§ ä\x000cÈüf\x0013p\x0013×ºþu¸4\x0001ç× îÐMßkDí\x0002\x0013ºP\0ñ'\\x0007ú¥÷U2&F;=Ú	a\x0012gh\x0000"[»|ÃL$<4G¼ '¸®q¶)#+UÊ5òv\x001d¹rì\x0006ÀAÒÊ2óÂ\x0015\x00130dçnY\x001btúéVÙû!éÖiu\x001cúÇNØtO? vë§ãµ1ùÜ\x001fD\x001br	»e´
Lâ@7aæ¨\x0013tñ§w?ÿ\x000c\x0018ZÞ{òþãõò`u­Ü{¼V\x001e<zRhÖüdM\x0003óævYõxu¥¬onùðõ\x001aí£G\x000fõ¼ám"\x0014,:c>¢¾Ä\x0015Æåo¼=?\x0007Ý\x000fU§\x0007"ð@~jn¾®Áß§Cñb[¥Q¤D7@\x0015(;-£\x0010GÊ Ýb@£#ç\x000b\x000b\x001d\x0019\x0003µ¿ /t%òszª|ÂI8ºR\x0012k\x0001É0	aÇ/8\x000cÿqCPËW.ûÀàw¿û]\x001fV§"³!Ðñq°\x0012(óO§M4]\x0011/\x0005Ðo@f¿»JgceUå\x001c(|
ÆÊ*\x0013\x000c ÃÛÝé'\x001fõÕõ²½¾QöU\x0017
 ORÑ\x0003\x0008«ü\x0006GÄ9%Í\x0007¤áãøS9\x000c*½!HT]Ñ@¹Ý
êA\x0011\x0005ËR)`Ð\x0016,.þüá`oF2]èpË»U\x0016V¬\x0016\x0017\x0016üÉÅÅ¥rþÜ\x0005ß»F}ÅáÕ¸#*Ò:Ý\x0008QìfÆcíÕ\x001bÐ\x000b×ó\x0014*\x001cG	U\x000b\x0014\åS\x000bÏÙÒÚbÅ¹*)G\x001a%­´r\x0016
þÈ=V¶äÆ³\x0014\x0001âZÑ¶¢¥?)Yp:\x0016Ûp5½\x000c¬\x0003¬bJùà*RèúÉç©¾õï\x0007\x001c\x001c.) 
³µ¶Z:j\x0003ÔäÍJ\x0011_·¥0oïrÅBo @þà··l&ò°µ³í<_xñZùúo[¯¼\f\x0017\x0017TÏÃecu£¬>Y
\x0019<=yü¤|¡	\x0014\x0017f¢TÍLO+}µñíMÓ~áÂ²ËøÅ\x0017Ç­w\x0006-òFÑ¤¢Ó\x0002/P$Y¶âzAöÆ\x001be\x0011>ÄV³d\x0003üÓn=\x0001ju}+ªiç{@v²aïÕoýÜm?~iþ®H¿ÔÏ]ÿÂ\x0014 (u\x0015
¦¡1y3\x0017\x001eIÈôÒ\x00044ut\x0018Â"k>
\x0016×B0KÈ£\x001ftã	k:±×Ï\x0000é$}3êÛÚ\x0000}'.ð¢iÒA/òaÿªL	éN~Aûé²[ôÑu\x001a\x0008_#ÓL¨ù\ÁÂ­Î»_úu:g\x0001yö\x001e\x001d§Ó\x0015µ6¡\x0007ÿ`Ä¸m\x001cN·
Å%\x000fìÐJ6ç;i?Î_É+\x0017§Ñ-SÁ=ø\x001fÀÅÖ^ÁR2_\x001a:Vè«ì	&Íµ¼Ò­\x000eö:ýîÏÆ^ý0ËÕ\x001fD\x001bPÃ
×þN§í/\x0013ºþµ½\x000f\x000e½0tø>o\x0011qÑúÎIYÛ\x0012nï-
0»\x001aP¸*`ko¿lnëY\x0003\x0007<
¾ìWs0Ë&9ôÌr1_æçí1¾G·ËÝIRº|öFD\x001eJp\x000e!_þ÷mðJ\x0007]\x000b½º36	\x0003\x001dpê®N4¦¬,-ê°åÇÙd°~¡Ìø\x001c\x0016ÝÇâõY¯\x0000Á0ÒR¼TÚ\x0019m\x0004Ò^\x000bOíçí\x0011mÜh\x0004äõõo|½üñ\x001fÿ±ßÀ\x0004ØËæFlÔxk×\x0015OÔæ,UD:Þ@5Æ_\x0012\x0010[X\x0012Îö\x000f·óaf^&\x0018gÖÁÀ
/UnÒ Ç+Þ¾åú\x0000Òd+ql¢«þ&\x0003ål
2\x0000óÉé¹i
ª>ó3ÆÀ'¹\x0018b42¬¶Í\x0016\x0013¸C\x00031(7è±¾£ô£Þ\x0010X5.¹y&%ôù+%°Í
äebjÂo=¾þúËåÊ¥Ëåúõ\x001bjÜWýíH¾ç¶-\x0019´¾By\x0013ýØØ\x001b\x0005Ë
\x000c{ãfÚÛõv
åÏÕ\x0015(NyæÍ[\x001cVR ¹òù)µ\x000fD&Ê\x0014³B\x0014ªp?>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/demarches.html](https://www.associations.gouv.fr/demarches.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
* URL: [https://www.associations.gouv.fr/creer-votre-association.html](https://www.associations.gouv.fr/creer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `$_GET[`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$_GET[</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html](https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/guide-juridique-et-fiscal.html](https://www.associations.gouv.fr/guide-juridique-et-fiscal.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/creer-votre-association.html](https://www.associations.gouv.fr/creer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/documentation.html](https://www.associations.gouv.fr/documentation.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-vie-associative.html](https://www.associations.gouv.fr/la-vie-associative.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/demarches.html](https://www.associations.gouv.fr/demarches.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
* URL: [https://www.associations.gouv.fr/financer-votre-association.html](https://www.associations.gouv.fr/financer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,400italic,300italic,500italic,700,700italic,900,900italic,100italic,100' rel='stylesheet' type='text/css' />`
  
  
  
  
Instances: 11
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library bootstrap, version 3.3.7 is vulnerable.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/bootstrap/js/bootstrap.js](https://www.associations.gouv.fr/squelettes/bootstrap/js/bootstrap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v3.3.7`
  
  
  
  
Instances: 1
  
### Solution
<p>Please upgrade to the latest version of bootstrap.</p>
  
### Other information
<p>CVE-2019-8331</p><p>CVE-2018-14041</p><p>CVE-2018-14040</p><p>CVE-2018-14042</p><p></p>
  
### Reference
* https://github.com/twbs/bootstrap/issues/28236
* https://github.com/twbs/bootstrap/issues/20184
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/la-vie-associative.html](https://www.associations.gouv.fr/la-vie-associative.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="form">`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/financer-votre-association.html](https://www.associations.gouv.fr/financer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/demarches.html](https://www.associations.gouv.fr/demarches.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html](https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/creer-votre-association.html](https://www.associations.gouv.fr/creer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/guide-juridique-et-fiscal.html](https://www.associations.gouv.fr/guide-juridique-et-fiscal.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="spip.php?page=recherche" method="get">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "page" "recherche" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://www.associations.gouv.fr/rubrique237](https://www.associations.gouv.fr/rubrique237)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/E1g99-IOe3w](https://www.associations.gouv.fr/IMG/E1g99-IOe3w)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/ecrire/](https://www.associations.gouv.fr/ecrire/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/rubrique30](https://www.associations.gouv.fr/rubrique30)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/zLPe6diRmyc](https://www.associations.gouv.fr/IMG/zLPe6diRmyc)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/oCxi_FIbXFg](https://www.associations.gouv.fr/IMG/oCxi_FIbXFg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/j9SEOhulm2M](https://www.associations.gouv.fr/IMG/j9SEOhulm2M)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/article11000](https://www.associations.gouv.fr/article11000)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/article11107](https://www.associations.gouv.fr/article11107)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 46 [https://www.associations.gouv.fr/hcva-237.html].</p><p>Predicted response size: 346.</p><p>Response Body Length: 413.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `BIGipServerpool-djepva-association.cegedim.cloud-HTTP`
  
  
  * Evidence: `Set-Cookie: BIGipServerpool-djepva-association.cegedim.cloud-HTTP`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `BIGipServerpool-djepva-association.cegedim.cloud-HTTP`
  
  
  * Evidence: `Set-Cookie: BIGipServerpool-djepva-association.cegedim.cloud-HTTP`
  
  
  
  
* URL: [https://www.associations.gouv.fr/robots.txt](https://www.associations.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `BIGipServerpool-djepva-association.cegedim.cloud-HTTP`
  
  
  * Evidence: `Set-Cookie: BIGipServerpool-djepva-association.cegedim.cloud-HTTP`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/le-guichet-unique-urgencess-est-ouvert.html](https://www.associations.gouv.fr/le-guichet-unique-urgencess-est-ouvert.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/covid.html](https://www.associations.gouv.fr/covid.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/kitgratuit.html](https://www.associations.gouv.fr/kitgratuit.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/qui-peut-representer-l-association-en-justice.html](https://www.associations.gouv.fr/qui-peut-representer-l-association-en-justice.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/resultats-enquete-flash-l-action-benevole-dans-le-cadre-de-la-crise-sanitaire.html](https://www.associations.gouv.fr/resultats-enquete-flash-l-action-benevole-dans-le-cadre-de-la-crise-sanitaire.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/le-guide-du-benevolat-1065.html](https://www.associations.gouv.fr/le-guide-du-benevolat-1065.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/une-association-est-elle-soumise-a-la-taxe-sur-les-bureaux.html](https://www.associations.gouv.fr/une-association-est-elle-soumise-a-la-taxe-sur-les-bureaux.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/disponibilite-des-credits-cec.html](https://www.associations.gouv.fr/disponibilite-des-credits-cec.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/une-mairie-peut-elle-etre-le-siege-social-d-une-association.html](https://www.associations.gouv.fr/une-mairie-peut-elle-etre-le-siege-social-d-une-association.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/fdva-fonctionnement-innovation-les-appels-a-projets-departementaux-2021.html](https://www.associations.gouv.fr/fdva-fonctionnement-innovation-les-appels-a-projets-departementaux-2021.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-reprise-des-activites-associatives-janvier-2021.html](https://www.associations.gouv.fr/la-reprise-des-activites-associatives-janvier-2021.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-dons-au-profit-d-organismes-dont-le-siege-est-situe-dans-l-union-europeenne-donnent-ils-droit-a-reduction-fiscale.html](https://www.associations.gouv.fr/les-dons-au-profit-d-organismes-dont-le-siege-est-situe-dans-l-union-europeenne-donnent-ils-droit-a-reduction-fiscale.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2`
  
  
  * Evidence: `<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-53109861138a71e2"></script>`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/consultation-publique-du-don-en-confiance-sur-le-referentiel-de-deontologie.html](https://www.associations.gouv.fr/consultation-publique-du-don-en-confiance-sur-le-referentiel-de-deontologie.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487](https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/javascript/jquery.columnizer.min.js](https://www.associations.gouv.fr/squelettes/javascript/jquery.columnizer.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-ressources-financieres-et-l-accompagnement-des-pouvoirs-publics.html](https://www.associations.gouv.fr/les-ressources-financieres-et-l-accompagnement-des-pouvoirs-publics.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
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
  
  
  
* URL: [https://www.associations.gouv.fr/guide-juridique-et-fiscal.html](https://www.associations.gouv.fr/guide-juridique-et-fiscal.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/financer-votre-association.html](https://www.associations.gouv.fr/financer-votre-association.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-vie-associative.html](https://www.associations.gouv.fr/la-vie-associative.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/creer-votre-association.html](https://www.associations.gouv.fr/creer-votre-association.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/documentation.html](https://www.associations.gouv.fr/documentation.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html](https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/demarches.html](https://www.associations.gouv.fr/demarches.html)
  
  
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
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/xlsx/associations_nationales_agreees_au_8_sept_2016.xlsx](https://www.associations.gouv.fr/IMG/xlsx/associations_nationales_agreees_au_8_sept_2016.xlsx)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/creer-votre-association.html](https://www.associations.gouv.fr/creer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/sitemap.xml](https://www.associations.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache, must-revalidate`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/docx/logo_place_numerique_dans_le_projet_associatif_en_2019.docx](https://www.associations.gouv.fr/IMG/docx/logo_place_numerique_dans_le_projet_associatif_en_2019.docx)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/robots.txt](https://www.associations.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html](https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/docx/fiche_spd-rna.docx](https://www.associations.gouv.fr/IMG/docx/fiche_spd-rna.docx)
  
  
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

  
  
  
  
### Secure Pages Include Mixed Content
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/dans-une-association-en-france-ou-a-l-etranger-10556.html](https://www.associations.gouv.fr/dans-une-association-en-france-ou-a-l-etranger-10556.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.dailymotion.com/embed/video/x1bvtmr`
  
  
  
  
* URL: [https://www.associations.gouv.fr/aupres-d-une-collectivite-en-france.html](https://www.associations.gouv.fr/aupres-d-une-collectivite-en-france.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.dailymotion.com/embed/video/xxgb71`
  
  
  
  
* URL: [https://www.associations.gouv.fr/seminaire-actifs-engagement-benevolat-mode-d-emploi.html](https://www.associations.gouv.fr/seminaire-actifs-engagement-benevolat-mode-d-emploi.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://www.dailymotion.com/embed/video/x1bvtmr`
  
  
  
  
* URL: [https://www.associations.gouv.fr/une-association-doit-elle-acquitter-la-taxe-d-habitation.html](https://www.associations.gouv.fr/une-association-doit-elle-acquitter-la-taxe-d-habitation.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://logi3.xiti.com/hit.xiti?s=257817&s2=19&p=&di=&an=&ac=`
  
  
  
  
* URL: [https://www.associations.gouv.fr/changement-de-dirigeants.html](https://www.associations.gouv.fr/changement-de-dirigeants.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://logi3.xiti.com/hit.xiti?s=257817&s2=19&p=&di=&an=&ac=`
  
  
  
  
Instances: 5
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=iframe src=http://www.dailymotion.com/embed/video/x1bvtmr</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/](https://www.associations.gouv.fr/squelettes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/plugins/](https://www.associations.gouv.fr/plugins/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/prive/](https://www.associations.gouv.fr/prive/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/cache-css/](https://www.associations.gouv.fr/local/cache-css/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/](https://www.associations.gouv.fr/local/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/youtube.com/watch?time_continue=11](https://www.associations.gouv.fr/IMG/youtube.com/watch?time_continue=11)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/lib/](https://www.associations.gouv.fr/lib/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/plugins-dist/](https://www.associations.gouv.fr/plugins-dist/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes-dist/](https://www.associations.gouv.fr/squelettes-dist/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/CP_5e_Pleniere_HCVA.pdf](https://www.associations.gouv.fr/IMG/pdf/CP_5e_Pleniere_HCVA.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `/Type/Font/Subtype/TrueType/Name/F1/BaseFont/Times`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/0718_-_Discours_VF_remise_rapport_final_Duport_et_Dilain-2.pdf](https://www.associations.gouv.fr/IMG/pdf/0718_-_Discours_VF_remise_rapport_final_Duport_et_Dilain-2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `/Type/Font/Subtype/TrueType/Name/F1/BaseFont/Times`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Bn+LWHTDaMEAu5UqJlLL3fNyljz02agnfv4tZe7DRSgT6ToCg9rlcnTwDEOwhiiZKAWqgCNkbU1A8x7VrHPJ+h9A3GM=`
  
  
  
  
* URL: [https://www.associations.gouv.fr/sitemap.xml](https://www.associations.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/IMG/pdf/benevolat_valorisation_comptable2011`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/115ans_loi1901_associations.pdf](https://www.associations.gouv.fr/IMG/pdf/115ans_loi1901_associations.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `/Type/Font/Subtype/TrueType/Name/F1/BaseFont/Times`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/0718_-_Discours_VF_remise_rapport_final_Duport_et_Dilain.pdf](https://www.associations.gouv.fr/IMG/pdf/0718_-_Discours_VF_remise_rapport_final_Duport_et_Dilain.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `/Type/Font/Subtype/TrueType/Name/F1/BaseFont/Times`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/0926-Invitation_a_la_presse_-_CONFERNCE_DE_PRESSE_PLF2013-2.pdf](https://www.associations.gouv.fr/IMG/pdf/0926-Invitation_a_la_presse_-_CONFERNCE_DE_PRESSE_PLF2013-2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/ColorSpace/DeviceRGB/Filter/DCTDecode/Height`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/CP_appel_projet_FONJEP.pdf](https://www.associations.gouv.fr/IMG/pdf/CP_appel_projet_FONJEP.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/ColorSpace/DeviceRGB/Filter/DCTDecode/Height`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `KZ72csVKpwBo2goqJlLL3fNyljz02Yj5n5ZQWLvUBUCMp5Tfn6iEkS9ViDyEWrqO9w0genAAh+6gnUC797pOsPRZhtQ=`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/17_11_2011_Jeannette_Bougrab-_FRANCE_GENEROSITE-CAREZx.pdf](https://www.associations.gouv.fr/IMG/pdf/17_11_2011_Jeannette_Bougrab-_FRANCE_GENEROSITE-CAREZx.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `1/S/u/i/t/e/space/a/d/eacute/b/q/v/n/s/r/o`
  
  
  
  
* URL: [https://www.associations.gouv.fr/robots.txt](https://www.associations.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `tl0VMnUXRYQTzC4qJlLL3fNyljz02QJufsDK7i/esD/TYh+2csQug8mdPlYI5N6NhwwgrYujzzyxtVNuZOpdCkp+TfA=`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/pdf/appel_a_projets_contre_la_haine_et_les_discriminations_anti-lgbt_2017di.pdf](https://www.associations.gouv.fr/IMG/pdf/appel_a_projets_contre_la_haine_et_les_discriminations_anti-lgbt_2017di.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/ColorSpace/DeviceRGB/Filter/DCTDecode/Height`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�<�{�h��ҹ�r��Ӯ�ʗ�5���]\x0005�\x001e\x0016���8�z</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/lib/](https://www.associations.gouv.fr/lib/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/plugins-dist/](https://www.associations.gouv.fr/plugins-dist/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/youtube.com/watch?time_continue=11](https://www.associations.gouv.fr/IMG/youtube.com/watch?time_continue=11)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/](https://www.associations.gouv.fr/local/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/prive/](https://www.associations.gouv.fr/prive/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes-dist/](https://www.associations.gouv.fr/squelettes-dist/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/plugins/](https://www.associations.gouv.fr/plugins/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/](https://www.associations.gouv.fr/squelettes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/cache-css/](https://www.associations.gouv.fr/local/cache-css/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure each page is setting the specific and appropriate content-type value for the content being delivered.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx

  
#### CWE Id : 345
  
#### WASC Id : 12
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/bootstrap/plugins/bootstrap-accessibility-plugin-tabpanel/js/bootstrap-accessibility.js](https://www.associations.gouv.fr/squelettes/bootstrap/plugins/bootstrap-accessibility-plugin-tabpanel/js/bootstrap-accessibility.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487](https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487](https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/bootstrap/js/bootstrap.js](https://www.associations.gouv.fr/squelettes/bootstrap/js/bootstrap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/bootstrap/js/bootstrap.js](https://www.associations.gouv.fr/squelettes/bootstrap/js/bootstrap.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/javascript/masonry.pkgd.min.js](https://www.associations.gouv.fr/squelettes/javascript/masonry.pkgd.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.associations.gouv.fr/une-association-doit-elle-acquitter-la-taxe-d-habitation.html](https://www.associations.gouv.fr/une-association-doit-elle-acquitter-la-taxe-d-habitation.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/javascript/main.js](https://www.associations.gouv.fr/squelettes/javascript/main.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487](https://www.associations.gouv.fr/local/cache-js/50634197bd906c64a920fbb4b186b8dc.js?1612367487)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.associations.gouv.fr/squelettes/bootstrap/plugins/bootstrap-accessibility-plugin-tabpanel/js/bootstrap-accessibility.js](https://www.associations.gouv.fr/squelettes/bootstrap/plugins/bootstrap-accessibility-plugin-tabpanel/js/bootstrap-accessibility.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://www.associations.gouv.fr/changement-de-dirigeants.html](https://www.associations.gouv.fr/changement-de-dirigeants.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: " * Neither the name of eBay or any of its subsidiaries or affiliates nor the names of its contributors may be used to endorse or", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html](https://www.associations.gouv.fr/la-fiscalite-applicable-aux-associations.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=3&amp;p=guide_juridique_et_fiscal::la_gestion_de_l_association::la_fiscalite_applicable_aux_associations::accueil_la_fiscalite_applicable_aux_associations&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/guide-juridique-et-fiscal.html](https://www.associations.gouv.fr/guide-juridique-et-fiscal.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=3&amp;p=guide_juridique_et_fiscal::accueil_guide_juridique_et_fiscal&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"><i class="zmdi zmdi-close-circle"></i>Fermer l'aide</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/creer-votre-association.html](https://www.associations.gouv.fr/creer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=17&amp;p=vos_demarches::creer_votre_association::accueil_creer_votre_association&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/je-veux-m-engager.html](https://www.associations.gouv.fr/je-veux-m-engager.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=19&amp;p=je_veux_m_engager::accueil_je_veux_m_engager&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/financer-votre-association.html](https://www.associations.gouv.fr/financer-votre-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=17&amp;p=vos_demarches::financer_votre_association::accueil_financer_votre_association&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/IMG/jpg/cravate3.jpg](https://www.associations.gouv.fr/IMG/jpg/cravate3.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a\x000c>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html](https://www.associations.gouv.fr/les-centres-de-ressources-pour-les-responsables-ou-createurs-d-association.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=6&amp;p=la_vie_associative::la_politique_associative_de_l_etat::tous_les_points_ressources_pres_de_chez_vous::tous_les_points_ressources_pres_de_chez_vous/accueil_tous_les_points_ressources_pres_de_chez_vous&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/demarches.html](https://www.associations.gouv.fr/demarches.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=17&amp;p=vos_demarches::accueil_vos_demarches&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#"><i class="zmdi zmdi-close-circle"></i>Fermer l'aide</a>`
  
  
  
  
* URL: [https://www.associations.gouv.fr/la-vie-associative.html](https://www.associations.gouv.fr/la-vie-associative.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
	<div id='xiti-tag-noscript'>
		<img width='1' height='1' src='https://logs4.xiti.com/hit.xiti?s=191503&amp;s2=6&amp;p=la_vie_associative::accueil_la_vie_associative&amp;di=&amp;' alt='XiTi' />
	</div>
</noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/ecrire/](https://www.associations.gouv.fr/ecrire/)
  
  
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

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/lib/](https://www.associations.gouv.fr/lib/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/](https://www.associations.gouv.fr/local/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/robots.txt](https://www.associations.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/local/cache-css/](https://www.associations.gouv.fr/local/cache-css/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/prive/](https://www.associations.gouv.fr/prive/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr](https://www.associations.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/plugins/](https://www.associations.gouv.fr/plugins/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.associations.gouv.fr/plugins-dist/](https://www.associations.gouv.fr/plugins-dist/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://www.associations.gouv.fr/sitemap.xml](https://www.associations.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
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
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1612366337`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1610009043`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1610703804`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1505135207`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1601908755`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1611340574`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1616095062`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1612367487`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1601908757`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1609941301`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1609744127`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1601908756`
  
  
  
  
* URL: [https://www.associations.gouv.fr/](https://www.associations.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1615453348`
  
  
  
  
Instances: 13
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1612366337, which evaluates to: 2021-02-03 15:32:17</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=actualites](https://www.associations.gouv.fr/spip.php?page=actualites)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=actualites](https://www.associations.gouv.fr/spip.php?page=actualites)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=actualites](https://www.associations.gouv.fr/spip.php?page=actualites)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `recherche`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP](https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
* URL: [https://www.associations.gouv.fr/spip.php?page=actualites](https://www.associations.gouv.fr/spip.php?page=actualites)
  
  
  * Method: `GET`
  
  
  * Parameter: `page`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.associations.gouv.fr/spip.php?page=recherche&recherche=ZAP</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>page=recherche</p><p></p><p>The user-controlled value was:</p><p>recherche</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3
