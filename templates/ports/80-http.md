## NMAP

```bash
nmap -sV -sC -p 80 TARGET
```

## CURL

```bash
curl -I http://TARGET
curl -s http://TARGET | head
```

## Nikto

```bash
nikto -h http://TARGET
```

## Whatweb

```bash
whatweb http://TARGET
```

## Screenshot

```bash
# browser or cutycapt / firefox
```

## Gobuster

Self Enumerate these!

Directories ->

```bash
gobuster dir -u http://TARGET -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30
```

Files ->

```bash
gobuster dir -u http://TARGET -w /usr/share/seclists/Discovery/Web-Content/raft-medium-files.txt -k -t 30
```
