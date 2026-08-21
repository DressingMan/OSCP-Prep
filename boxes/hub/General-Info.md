## Host Info
```
TARGET
```


## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:05 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.072s latency).
Scanned at 2024-07-01 17:33:10 EDT for 33s
Not shown: 996 closed tcp ports (reset)
PORT     STATE SERVICE  REASON         VERSION
22/tcp   open  ssh      syn-ack ttl 61 OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 c9:c3:da:15:28:3b:f1:f8:9a:36:df:4d:36:6b:a7:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDNEbgprJqVJa8R95Wkbo3cemB4fdRzos+v750LtPEnRs+IJQn5jcg5l89Tx4junU+AXzLflrMVo55gbuKeNTDtFRU9ltlIu4AU+f7lRlUlvAHlNjUbU/z3WBZ5ZU9j7Xc9WKjh1Ov7chC0UnDdyr5EGrIwlLzgk8zrWx364+S4JqLtER2/n0rhVxa9RCw0tR/oL24kMep4q7rFK6dThiRtQ9nsJFhh6yw8Fmdg7r4uohqH70UJurVwVNwFqtr/86e4VSSoITlMQPZrZFVvoSsjyL8LEODt1qznoLWudMD95Eo1YFSPID5VcS0kSElfYigjSr+9bNSdlzAof1mU6xJA67BggGNu6qITWWIJySXcropehnDAt2nv4zaKAUKc/T0ij9wkIBskuXfN88cEmZbu+gObKbLgwQSRQJIpQ+B/mA8CD4AiaTmEwGSWz1dVPp5Fgb6YVy6E4oO9ASuD9Q1JWuRmnn8uiHF/nPLs2LC2+rh3nPLXlV+MG/zUfQCrdrE=
|   256 26:03:2b:f6:da:90:1d:1b:ec:8d:8f:8d:1e:7e:3d:6b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCUhhvrIBs53SApXKZYHWBlpH50KO3POt8Y+WvTvHZ5YgRagAEU5eSnGkrnziCUvDWNShFhLHI7kQv+mx+4R6Wk=
|   256 fb:43:b2:b0:19:2f:d3:f6:bc:aa:60:67:ab:c1:af:37 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIN4MSEXnpONsc0ANUT6rFQPWsoVmRW4hrpSRq++xySM9
80/tcp   open  http     syn-ack ttl 61 nginx 1.18.0
|_http-server-header: nginx/1.18.0
|_http-title: 403 Forbidden
| http-methods: 
|_  Supported Methods: GET HEAD POST
8082/tcp open  http     syn-ack ttl 61 Barracuda Embedded Web Server
|_http-title: Home
|_http-favicon: Unknown favicon MD5: FDF624762222B41E2767954032B6F1FF
|_http-server-header: BarracudaServer.com (Posix)
| http-methods: 
|   Supported Methods: OPTIONS GET HEAD PROPFIND PATCH POST PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
|_  Potentially risky methods: PROPFIND PATCH PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
| http-webdav-scan: 
|   Server Date: Mon, 01 Jul 2024 21:33:38 GMT
|   Server Type: BarracudaServer.com (Posix)
|   Allowed Methods: OPTIONS, GET, HEAD, PROPFIND, PATCH, POST, PUT, COPY, DELETE, MOVE, MKCOL, PROPFIND, PROPPATCH, LOCK, UNLOCK
|_  WebDAV type: Unknown
9999/tcp open  ssl/http syn-ack ttl 61 Barracuda Embedded Web Server
|_http-server-header: BarracudaServer.com (Posix)
| http-webdav-scan: 
|   Server Date: Mon, 01 Jul 2024 21:33:37 GMT
|   Server Type: BarracudaServer.com (Posix)
|   Allowed Methods: OPTIONS, GET, HEAD, PROPFIND, PATCH, POST, PUT, COPY, DELETE, MOVE, MKCOL, PROPFIND, PROPPATCH, LOCK, UNLOCK
|_  WebDAV type: Unknown
| ssl-cert: Subject: commonName=FuguHub/stateOrProvinceName=California/countryName=US
| Subject Alternative Name: DNS:FuguHub, DNS:FuguHub.local, DNS:localhost
| Issuer: commonName=Real Time Logic Root CA/organizationName=Real Time Logic LLC/countryName=US/organizationalUnitName=SharkSSL/emailAddress=ginfo@realtimelogic.com
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2019-07-16T19:15:09
| Not valid after:  2074-04-18T19:15:09
| MD5:   6320:2067:19be:be32:18ce:3a61:e872:cc3f
| SHA-1: 503c:a62d:8a8c:f8c1:6555:ec50:77d1:73cc:0865:ec62
| -----BEGIN CERTIFICATE-----
| MIIEfDCCA2SgAwIBAgIBEDANBgkqhkiG9w0BAQsFADCBiDELMAkGA1UEBhMCVVMx
| HDAaBgNVBAoTE1JlYWwgVGltZSBMb2dpYyBMTEMxETAPBgNVBAsTCFNoYXJrU1NM
| MSAwHgYDVQQDExdSZWFsIFRpbWUgTG9naWMgUm9vdCBDQTEmMCQGCSqGSIb3DQEJ
| ARYXZ2luZm9AcmVhbHRpbWVsb2dpYy5jb20wIBcNMTkwNzE2MTkxNTA5WhgPMjA3
| NDA0MTgxOTE1MDlaMDQxCzAJBgNVBAYTAlVTMRMwEQYDVQQIDApDYWxpZm9ybmlh
| MRAwDgYDVQQDDAdGdWd1SHViMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKC
| AQEA2uaLiecelbCvdPpZcmweQmK+rcxjFwKKx+ButcLc/vgDTbbDDsg9Pfn78RNE
| hrM1WsvkGXKgJY2M9tzTB6o27pUipwfYAA8a4mV7wfM+YGOVuC05t3oh3+GtSciQ
| ZNDEX3cSZ5XanKPNe9vNBNtFiC5ujadbsLWJxC4mHR9fnx3fPlhQO25QBcX+0M1h
| vOwsidZaqyl+R1zMOi/6IpJJobTJMRKT23N61q3ZKeJnZM2JK9H2srC8tRlIidpf
| Iu3Sv7St3Hg2VzbtlEDpGdISZTwpB+MIgvcZ2Z5IVfnhYJlQlNGHbg8jnegA07VE
| AsfkNlyMfVO88TCo5fLhE6wZLwIDAQABo4IBQDCCATwwHQYDVR0OBBYEFI5fqYOD
| ozZher2qQbU3//9gzTIyMIG1BgNVHSMEga0wgaqAFHlYmIP3mqIAiKOI3DxqZo3k
| KQKGoYGOpIGLMIGIMQswCQYDVQQGEwJVUzEcMBoGA1UEChMTUmVhbCBUaW1lIExv
| Z2ljIExMQzERMA8GA1UECxMIU2hhcmtTU0wxIDAeBgNVBAMTF1JlYWwgVGltZSBM
| b2dpYyBSb290IENBMSYwJAYJKoZIhvcNAQkBFhdnaW5mb0ByZWFsdGltZWxvZ2lj
| LmNvbYIBADAJBgNVHRMEAjAAMAsGA1UdDwQEAwIDqDAdBgNVHSUEFjAUBggrBgEF
| BQcDAgYIKwYBBQUHAwEwLAYDVR0RBCUwI4IHRnVndUh1YoINRnVndUh1Yi5sb2Nh
| bIIJbG9jYWxob3N0MA0GCSqGSIb3DQEBCwUAA4IBAQBsn2vzaK/2bKmWJ52FiRVw
| K3NxCqQrxHjXp2nJFc0S05XnCUqN5RbTgyhv0a8ODniaiJbXAaJC34Ot+v6UMeWE
| CHmZgjbZUvsrQiEUz+i0fegtwp+zgSOlb6t+g3lPGTzBjlFUfb0gaRSxSoI42apG
| QBwoN1haaHhm6THC7DIYmFiOgRiQfitiTf9FtbwTTfrLnVm3e3dCuwCmkcDgBZE1
| Q0M4pGSS3vWTQxF6oyYNe7mhtvGeG7qYE6amtF9iuiUt0MrH4hXTMfHcjHdRULgc
| 1a3vVPwl5CZsQRz40OPrQVtF7rcXRNWsU/1ze9r1sgeLxvjWmbW0GByKJ+jnHALy
|_-----END CERTIFICATE-----
|_http-favicon: Unknown favicon MD5: FDF624762222B41E2767954032B6F1FF
| http-methods: 
|   Supported Methods: OPTIONS GET HEAD PROPFIND PATCH POST PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
|_  Potentially risky methods: PROPFIND PATCH PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
|_http-title: Home
Device type: firewall|VoIP adapter|general purpose
Running (JUST GUESSING): Fortinet embedded (90%), Cisco embedded (87%), Linux 2.6.X (87%)
OS CPE: cpe:/h:fortinet:fortigate_100d cpe:/h:cisco:unified_call_manager cpe:/o:linux:linux_kernel:2.6.26
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Fortinet FortiGate 100D firewall (90%), Cisco Unified Communications Manager VoIP adapter (87%), Linux 2.6.26 (PCLinuxOS) (87%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/1%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=668320B7%P=x86_64-pc-linux-gnu)
SEQ(TS=A)
SEQ(SP=107%GCD=1%ISR=10A%TI=Z%TS=A)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=N)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=N)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 8.240 days (since Sun Jun 23 11:47:43 2024)
Network Distance: 4 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 256/tcp)
HOP RTT      ADDRESS
1   70.54 ms ATTACKER
2   70.43 ms ATTACKER
3   72.87 ms TARGET
4   74.78 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul  1 17:33:43 2024 -- 1 IP address (1 host up) scanned in 37.85 seconds

```

#### Full Scan
```

# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:05 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
adjust_timeouts2: packet supposedly had rtt of 9804234 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of 9804234 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of 8253707 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of 8253707 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -588340 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -588340 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -266365 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -266365 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -351985 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -351985 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -358363 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -358363 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -108649 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -108649 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -393031 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -393031 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -194746 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -194746 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.095s latency).
Scanned at 2024-07-01 17:33:06 EDT for 878s
Not shown: 65495 closed tcp ports (reset)
PORT      STATE    SERVICE       REASON         VERSION
22/tcp    open     ssh           syn-ack ttl 61 OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 c9:c3:da:15:28:3b:f1:f8:9a:36:df:4d:36:6b:a7:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDNEbgprJqVJa8R95Wkbo3cemB4fdRzos+v750LtPEnRs+IJQn5jcg5l89Tx4junU+AXzLflrMVo55gbuKeNTDtFRU9ltlIu4AU+f7lRlUlvAHlNjUbU/z3WBZ5ZU9j7Xc9WKjh1Ov7chC0UnDdyr5EGrIwlLzgk8zrWx364+S4JqLtER2/n0rhVxa9RCw0tR/oL24kMep4q7rFK6dThiRtQ9nsJFhh6yw8Fmdg7r4uohqH70UJurVwVNwFqtr/86e4VSSoITlMQPZrZFVvoSsjyL8LEODt1qznoLWudMD95Eo1YFSPID5VcS0kSElfYigjSr+9bNSdlzAof1mU6xJA67BggGNu6qITWWIJySXcropehnDAt2nv4zaKAUKc/T0ij9wkIBskuXfN88cEmZbu+gObKbLgwQSRQJIpQ+B/mA8CD4AiaTmEwGSWz1dVPp5Fgb6YVy6E4oO9ASuD9Q1JWuRmnn8uiHF/nPLs2LC2+rh3nPLXlV+MG/zUfQCrdrE=
|   256 26:03:2b:f6:da:90:1d:1b:ec:8d:8f:8d:1e:7e:3d:6b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCUhhvrIBs53SApXKZYHWBlpH50KO3POt8Y+WvTvHZ5YgRagAEU5eSnGkrnziCUvDWNShFhLHI7kQv+mx+4R6Wk=
|   256 fb:43:b2:b0:19:2f:d3:f6:bc:aa:60:67:ab:c1:af:37 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIN4MSEXnpONsc0ANUT6rFQPWsoVmRW4hrpSRq++xySM9
80/tcp    open     http          syn-ack ttl 61 nginx 1.18.0
|_http-server-header: nginx/1.18.0
|_http-title: 403 Forbidden
| http-methods: 
|_  Supported Methods: GET HEAD POST
1263/tcp  filtered dka           no-response
2718/tcp  filtered pn-requester2 no-response
4450/tcp  filtered camp          no-response
8082/tcp  open     http          syn-ack ttl 61 Barracuda Embedded Web Server
| http-methods: 
|   Supported Methods: OPTIONS GET HEAD PROPFIND PATCH POST PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
|_  Potentially risky methods: PROPFIND PATCH PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
|_http-server-header: BarracudaServer.com (Posix)
| http-webdav-scan: 
|   Server Date: Mon, 01 Jul 2024 21:47:36 GMT
|   WebDAV type: Unknown
|   Allowed Methods: OPTIONS, GET, HEAD, PROPFIND, PATCH, POST, PUT, COPY, DELETE, MOVE, MKCOL, PROPFIND, PROPPATCH, LOCK, UNLOCK
|_  Server Type: BarracudaServer.com (Posix)
9999/tcp  open     ssl/http      syn-ack ttl 61 Barracuda Embedded Web Server
| http-methods: 
|_  Supported Methods: GET HEAD POST
|_http-server-header: BarracudaServer.com (Posix)
| ssl-cert: Subject: commonName=FuguHub/stateOrProvinceName=California/countryName=US
| Subject Alternative Name: DNS:FuguHub, DNS:FuguHub.local, DNS:localhost
| Issuer: commonName=Real Time Logic Root CA/organizationName=Real Time Logic LLC/countryName=US/organizationalUnitName=SharkSSL/emailAddress=ginfo@realtimelogic.com
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2019-07-16T19:15:09
| Not valid after:  2074-04-18T19:15:09
| MD5:   6320:2067:19be:be32:18ce:3a61:e872:cc3f
| SHA-1: 503c:a62d:8a8c:f8c1:6555:ec50:77d1:73cc:0865:ec62
| -----BEGIN CERTIFICATE-----
| MIIEfDCCA2SgAwIBAgIBEDANBgkqhkiG9w0BAQsFADCBiDELMAkGA1UEBhMCVVMx
| HDAaBgNVBAoTE1JlYWwgVGltZSBMb2dpYyBMTEMxETAPBgNVBAsTCFNoYXJrU1NM
| MSAwHgYDVQQDExdSZWFsIFRpbWUgTG9naWMgUm9vdCBDQTEmMCQGCSqGSIb3DQEJ
| ARYXZ2luZm9AcmVhbHRpbWVsb2dpYy5jb20wIBcNMTkwNzE2MTkxNTA5WhgPMjA3
| NDA0MTgxOTE1MDlaMDQxCzAJBgNVBAYTAlVTMRMwEQYDVQQIDApDYWxpZm9ybmlh
| MRAwDgYDVQQDDAdGdWd1SHViMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKC
| AQEA2uaLiecelbCvdPpZcmweQmK+rcxjFwKKx+ButcLc/vgDTbbDDsg9Pfn78RNE
| hrM1WsvkGXKgJY2M9tzTB6o27pUipwfYAA8a4mV7wfM+YGOVuC05t3oh3+GtSciQ
| ZNDEX3cSZ5XanKPNe9vNBNtFiC5ujadbsLWJxC4mHR9fnx3fPlhQO25QBcX+0M1h
| vOwsidZaqyl+R1zMOi/6IpJJobTJMRKT23N61q3ZKeJnZM2JK9H2srC8tRlIidpf
| Iu3Sv7St3Hg2VzbtlEDpGdISZTwpB+MIgvcZ2Z5IVfnhYJlQlNGHbg8jnegA07VE
| AsfkNlyMfVO88TCo5fLhE6wZLwIDAQABo4IBQDCCATwwHQYDVR0OBBYEFI5fqYOD
| ozZher2qQbU3//9gzTIyMIG1BgNVHSMEga0wgaqAFHlYmIP3mqIAiKOI3DxqZo3k
| KQKGoYGOpIGLMIGIMQswCQYDVQQGEwJVUzEcMBoGA1UEChMTUmVhbCBUaW1lIExv
| Z2ljIExMQzERMA8GA1UECxMIU2hhcmtTU0wxIDAeBgNVBAMTF1JlYWwgVGltZSBM
| b2dpYyBSb290IENBMSYwJAYJKoZIhvcNAQkBFhdnaW5mb0ByZWFsdGltZWxvZ2lj
| LmNvbYIBADAJBgNVHRMEAjAAMAsGA1UdDwQEAwIDqDAdBgNVHSUEFjAUBggrBgEF
| BQcDAgYIKwYBBQUHAwEwLAYDVR0RBCUwI4IHRnVndUh1YoINRnVndUh1Yi5sb2Nh
| bIIJbG9jYWxob3N0MA0GCSqGSIb3DQEBCwUAA4IBAQBsn2vzaK/2bKmWJ52FiRVw
| K3NxCqQrxHjXp2nJFc0S05XnCUqN5RbTgyhv0a8ODniaiJbXAaJC34Ot+v6UMeWE
| CHmZgjbZUvsrQiEUz+i0fegtwp+zgSOlb6t+g3lPGTzBjlFUfb0gaRSxSoI42apG
| QBwoN1haaHhm6THC7DIYmFiOgRiQfitiTf9FtbwTTfrLnVm3e3dCuwCmkcDgBZE1
| Q0M4pGSS3vWTQxF6oyYNe7mhtvGeG7qYE6amtF9iuiUt0MrH4hXTMfHcjHdRULgc
| 1a3vVPwl5CZsQRz40OPrQVtF7rcXRNWsU/1ze9r1sgeLxvjWmbW0GByKJ+jnHALy
|_-----END CERTIFICATE-----
|_http-title: Home
14750/tcp filtered unknown       no-response
17339/tcp filtered unknown       no-response
19932/tcp filtered unknown       no-response
23826/tcp filtered unknown       no-response
26537/tcp filtered unknown       no-response
27121/tcp filtered unknown       no-response
27577/tcp filtered unknown       no-response
28306/tcp filtered unknown       no-response
30750/tcp filtered unknown       no-response
31890/tcp filtered unknown       no-response
33095/tcp filtered unknown       no-response
33797/tcp filtered unknown       no-response
34195/tcp filtered unknown       no-response
34927/tcp filtered unknown       no-response
39268/tcp filtered unknown       no-response
39433/tcp filtered unknown       no-response
39721/tcp filtered unknown       no-response
41253/tcp filtered unknown       no-response
43202/tcp filtered unknown       no-response
43402/tcp filtered unknown       no-response
44967/tcp filtered unknown       no-response
47258/tcp filtered unknown       no-response
47934/tcp filtered unknown       no-response
48019/tcp filtered unknown       no-response
48783/tcp filtered unknown       no-response
50461/tcp filtered unknown       no-response
50981/tcp filtered unknown       no-response
54827/tcp filtered unknown       no-response
54863/tcp filtered unknown       no-response
59757/tcp filtered unknown       no-response
61569/tcp filtered unknown       no-response
62990/tcp filtered unknown       no-response
63406/tcp filtered unknown       no-response
Aggressive OS guesses: Linux 2.6.32 (88%), Linux 3.4 (88%), Linux 3.5 (88%), Linux 4.2 (88%), Linux 4.4 (88%), Synology DiskStation Manager 5.1 (88%), WatchGuard Fireware 11.8 (88%), Linux 2.6.35 (87%), Linux 3.10 (87%), Linux 2.6.32 or 3.10 (87%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=7/1%OT=22%CT=1%CU=39753%PV=Y%DS=4%DC=T%G=Y%TM=66832
OS:400%P=x86_64-pc-linux-gnu)SEQ(SP=106%GCD=1%ISR=107%TI=Z%TS=A)SEQ(SP=106%
OS:GCD=1%ISR=109%TI=Z%TS=A)SEQ(SP=106%GCD=1%ISR=109%TI=Z%II=I%TS=A)SEQ(SP=F
OS:C%GCD=1%ISR=103%TI=Z%TS=A)OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11
OS:NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)WIN(W1=FE88%W2=FE88%W3=FE8
OS:8%W4=FE88%W5=FE88%W6=FE88)ECN(R=Y%DF=Y%T=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
OS:T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=N)T5(R=Y%DF=Y%
OS:T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=N)T7(R=N)U1(R=Y%DF=N%T=40%IPL=164
OS:%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=BF25%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 8.250 days (since Sun Jun 23 11:47:44 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 3306/tcp)
HOP RTT       ADDRESS
1   141.61 ms ATTACKER
2   140.27 ms ATTACKER
3   144.12 ms TARGET
4   145.91 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul  1 17:47:44 2024 -- 1 IP address (1 host up) scanned in 878.81 seconds

```

#### UDP scan
```

# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:05 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
Increasing send delay for TARGET from 100 to 200 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 11 dropped probes since last increase.
Nmap scan report for TARGET
Host is up, received user-set (0.17s latency).
Scanned at 2024-07-01 17:33:10 EDT for 254s
Not shown: 83 closed udp ports (port-unreach)
PORT      STATE         SERVICE      REASON      VERSION
69/udp    open|filtered tftp         no-response
139/udp   open|filtered netbios-ssn  no-response
427/udp   open|filtered svrloc       no-response
500/udp   open|filtered isakmp       no-response
997/udp   open|filtered maitrd       no-response
999/udp   open|filtered applix       no-response
1022/udp  open|filtered exp2         no-response
1025/udp  open|filtered blackjack    no-response
1433/udp  open|filtered ms-sql-s     no-response
1701/udp  open|filtered L2TP         no-response
1813/udp  open|filtered radacct      no-response
2000/udp  open|filtered cisco-sccp   no-response
2222/udp  open|filtered msantipiracy no-response
5353/udp  open|filtered zeroconf     no-response
10000/udp open|filtered ndmp         no-response
32815/udp open|filtered unknown      no-response
33281/udp open|filtered unknown      no-response
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.18
OS details: Linux 2.6.18, Linux 2.6.30
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=7/1%OT=%CT=%CU=7%PV=Y%DS=4%DC=T%G=N%TM=66832194%P=x
OS:86_64-pc-linux-gnu)SEQ(II=I)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q
OS:=)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=3434%RUD=G)IE(
OS:R=Y%DFI=N%T=40%CD=S)

Network Distance: 4 hops

TRACEROUTE (using port 49/udp)
HOP RTT      ADDRESS
1   52.81 ms ATTACKER
2   52.38 ms ATTACKER
3   54.14 ms TARGET
4   53.70 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul  1 17:37:24 2024 -- 1 IP address (1 host up) scanned in 259.64 seconds

```

