**Vulnerability Exploited** : Authentication

**System Vulnerabilities**: Javascript - Offucation

**Vulnerabilities Explaination** : Javascript using for login contain username and password for access this system

**Previlege Escalation Vulnerabilities**: N/A

**Vulnerabilities Fix** : N/A

**Severity** : Critical

**Details**  
***view***  
View source js file at `vview-source:http://challenge01.root-me.org/web-client/ch4/ch4.html` 
We can see script html tags
```  
<script type="text/javascript">
              /* <![CDATA[ */

              pass = '%63%70%61%73%62%69%65%6e%64%75%72%70%61%73%73%77%6f%72%64';
              h = window.prompt('Entrez le mot de passe / Enter password');
              if(h == unescape(pass)) {
                  alert('Password accepté, vous pouvez valider le challenge avec ce mot de passe.\nYou an validate the challenge using this pass.');
              } else {
                  alert('Mauvais mot de passe / wrong password');
              }

              /* ]]> */
          </script>
```

on if-else conditional, this script trying offucate code using unescape() javascript function `h = unescape()`. Decode string pass `%63%70%61%73%62%69%65%6e%64%75%72%70%61%73%73%77%6f%72%64` by unescape() it's throw flags
