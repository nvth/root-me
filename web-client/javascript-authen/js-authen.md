**Vulnerability Exploited** : Authentication

**System Vulnerabilities**: Javascript - Authentication

**Vulnerabilities Explaination** : Javascript using for login contain username and password for access this system

**Previlege Escalation Vulnerabilities**: N/A

**Vulnerabilities Fix** : N/A

**Severity** : Critical

**Details**  
***view***   
View source js file at `http://challenge01.root-me.org/web-client/ch9/login.js` 
We can see at if-else conditional of Login function, username and password be hashed on this javascript to login.  

```javascript
/* <![CDATA[ */

function Login(){
	var pseudo=document.login.pseudo.value;
	var username=pseudo.toLowerCase();
	var password=document.login.password.value;
	password=password.toLowerCase();
	if (pseudo=="4dm1n" && password=="sh.org") {
	    alert("Password accepté, vous pouvez valider le challenge avec ce mot de passe.\nYou an validate the challenge using this password.");
	} else { 
	    alert("Mauvais mot de passe / wrong password"); 
	}
}
/* ]]> */
```
 Use this credential to get flags.