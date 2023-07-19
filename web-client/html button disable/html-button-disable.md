**Vulnerability Exploited** : HTML Button Disable

**System Vulnerabilities**: HTML Button Disable

**Vulnerabilities Explaination** : Website `disable` input and button html form

**Previlege Escalation Vulnerabilities**: N/A

**Vulnerabilities Fix** : N/A

**Severity** : <span style="color: red">Critical</span> 

**Detail**  
Website disabled input form and button 
```html
<form action="" method="post" name="authform">
            <div>
                <input disabled type="text" name="auth-login" value="" />
                <input disabled type="submit" value="Member access" name="authbutton" />
            </div>
        </form>
```
try delete "disable" html tags - exploit success!