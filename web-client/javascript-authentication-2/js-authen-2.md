**Vulnerability Exploited** : Authentication

**System Vulnerabilities**: Javascript - Authentication - 2

**Vulnerabilities Explaination** : Javascript using for login contain username and password for access this system

**Previlege Escalation Vulnerabilities**: N/A

**Vulnerabilities Fix** : N/A

**Severity** : Critical

**Details**  
***view***   
View source js file at `view-source:http://challenge01.root-me.org/web-client/ch11/login.js` 
We can see 
```
function connexion(){
    var username = prompt("Username :", "");
    var password = prompt("Password :", "");
    var TheLists = ["GOD:HIDDEN"];
    for (i = 0; i < TheLists.length; i++)
    {
        if (TheLists[i].indexOf(username) == 0)
        {
            var TheSplit = TheLists[i].split(":");
            var TheUsername = TheSplit[0];
            var ThePassword = TheSplit[1];
            if (username == TheUsername && password == ThePassword)
            {
                alert("Vous pouvez utiliser ce mot de passe pour valider ce challenge (en majuscules) / You can use this password to validate this challenge (uppercase)");
            }
        }
        else
        {
            alert("Nope, you're a naughty hacker.")
        }
    }
}
```
at the connexion() function `var TheLists=[GOD:HIDDEN]`  
at the for() conditional, it contain 
```
if (TheLists[i].indexOf(username) == 0)
        {
            var TheSplit = TheLists[i].split(":");
            var TheUsername = TheSplit[0];
            var ThePassword = TheSplit[1];
```
According to Code in above, the credentials used to access the system is formatted 
`[TheUsername:ThePassword]` and this information is taken on variable `TheList`
Use this credential to get flags.