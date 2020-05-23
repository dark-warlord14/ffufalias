# ffufalias
Alias for storing results every time you run ffuf.

```
dirs(){
	name=$(echo $1 | unfurl -u domains)
	x=$(date +%Y%m%d%H%M%S)
	mkdir -p ~/Reports/$name
	mkdir -p /root/tools/Reports/$name
	ffuf -w /path/to/wordlist -u $1FUZZ -D -e asp,aspx,cgi,cfml,CFM,htm,html,json,jsp,php,phtml,pl,py,sh,shtml,sql,txt,xml,xhtml,tar,tar.gz,tgz,war,zip,swp,src,jar,java,log,bin,js,db -t 150 -o ~/Reports/$name/$name_$x.json
}
```

Copy this alias to your bash profile and next time you want to run ffuf just type the following command

`dirs https://yahoo.com/`
