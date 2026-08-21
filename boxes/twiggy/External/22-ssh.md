## NMAP 
```
# Nmap 7.94SVN scan initiated Sat Jun 29 16:34:23 2024 as: nmap -vv --reason -Pn -T4 -sV -p 22 --script=banner,ssh2-enum-algos,ssh-hostkey,ssh-auth-methods TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.054s latency).
Scanned at 2024-06-29 16:34:23 EDT for 4s
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.4 (protocol 2.0)
# Nmap done at Sat Jun 29 16:34:27 2024 -- 1 IP address (1 host up) scanned in 4.33 seconds
```

## SSH-AUDIT

```
# general
(gen) banner: SSH-2.0-OpenSSH_7.4
(gen) software: OpenSSH 7.4
(gen) compatibility: OpenSSH 7.4+ (some functionality from 6.6), Dropbear SSH 2018.76+ (some functionality from 0.52)
(gen) compression: enabled (zlib@openssh.com)

# security
(cve) CVE-2021-41617                        -- (CVSSv2: 7.0) privilege escalation via supplemental groups
(cve) CVE-2020-15778                        -- (CVSSv2: 7.8) command injection via anomalous argument transfers
(cve) CVE-2018-15919                        -- (CVSSv2: 5.3) username enumeration via GS2
(cve) CVE-2018-15473                        -- (CVSSv2: 5.3) enumerate usernames due to timing discrepancies
(cve) CVE-2016-20012                        -- (CVSSv2: 5.3) enumerate usernames via challenge response

# key exchange algorithms
(kex) curve25519-sha256                     -- [info] available since OpenSSH 7.4, Dropbear SSH 2018.76
                                            `- [info] default key exchange since OpenSSH 6.4
(kex) curve25519-sha256@libssh.org          -- [info] available since OpenSSH 6.4, Dropbear SSH 2013.62
                                            `- [info] default key exchange since OpenSSH 6.4
(kex) ecdh-sha2-nistp256                    -- [fail] using elliptic curves that are suspected as being backdoored by the U.S. National Security Agency
                                            `- [info] available since OpenSSH 5.7, Dropbear SSH 2013.62
(kex) ecdh-sha2-nistp384                    -- [fail] using elliptic curves that are suspected as being backdoored by the U.S. National Security Agency
                                            `- [info] available since OpenSSH 5.7, Dropbear SSH 2013.62
(kex) ecdh-sha2-nistp521                    -- [fail] using elliptic curves that are suspected as being backdoored by the U.S. National Security Agency
                                            `- [info] available since OpenSSH 5.7, Dropbear SSH 2013.62
(kex) diffie-hellman-group-exchange-sha256 (1024-bit) -- [fail] using small 1024-bit modulus
                                                      `- [info] available since OpenSSH 4.4
(kex) diffie-hellman-group16-sha512         -- [info] available since OpenSSH 7.3, Dropbear SSH 2016.73
(kex) diffie-hellman-group18-sha512         -- [info] available since OpenSSH 7.3
(kex) diffie-hellman-group-exchange-sha1 (1024-bit) -- [fail] using small 1024-bit modulus
                                                    `- [info] available since OpenSSH 2.3.0
(kex) diffie-hellman-group14-sha256         -- [warn] 2048-bit modulus only provides 112-bits of symmetric strength
                                            `- [info] available since OpenSSH 7.3, Dropbear SSH 2016.73
(kex) diffie-hellman-group14-sha1           -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] 2048-bit modulus only provides 112-bits of symmetric strength
                                            `- [info] available since OpenSSH 3.9, Dropbear SSH 0.53
(kex) diffie-hellman-group1-sha1            -- [fail] using small 1024-bit modulus
                                            `- [fail] vulnerable to the Logjam attack: https://en.wikipedia.org/wiki/Logjam_(computer_security)
                                            `- [fail] using broken SHA-1 hash algorithm
                                            `- [info] available since OpenSSH 2.3.0, Dropbear SSH 0.28
                                            `- [info] removed in OpenSSH 6.9: https://www.openssh.com/txt/release-6.9

# host-key algorithms
(key) ssh-rsa (2048-bit)                    -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] 2048-bit modulus only provides 112-bits of symmetric strength
                                            `- [info] available since OpenSSH 2.5.0, Dropbear SSH 0.28
                                            `- [info] deprecated in OpenSSH 8.8: https://www.openssh.com/txt/release-8.8
(key) rsa-sha2-512 (2048-bit)               -- [warn] 2048-bit modulus only provides 112-bits of symmetric strength
                                            `- [info] available since OpenSSH 7.2
(key) rsa-sha2-256 (2048-bit)               -- [warn] 2048-bit modulus only provides 112-bits of symmetric strength
                                            `- [info] available since OpenSSH 7.2
(key) ecdsa-sha2-nistp256                   -- [fail] using elliptic curves that are suspected as being backdoored by the U.S. National Security Agency
                                            `- [warn] using weak random number generator could reveal the key
                                            `- [info] available since OpenSSH 5.7, Dropbear SSH 2013.62
(key) ssh-ed25519                           -- [info] available since OpenSSH 6.5

# encryption algorithms (ciphers)
(enc) chacha20-poly1305@openssh.com         -- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 6.5
                                            `- [info] default cipher since OpenSSH 6.9
(enc) aes128-ctr                            -- [info] available since OpenSSH 3.7, Dropbear SSH 0.52
(enc) aes192-ctr                            -- [info] available since OpenSSH 3.7
(enc) aes256-ctr                            -- [info] available since OpenSSH 3.7, Dropbear SSH 0.52
(enc) aes128-gcm@openssh.com                -- [info] available since OpenSSH 6.2
(enc) aes256-gcm@openssh.com                -- [info] available since OpenSSH 6.2
(enc) aes128-cbc                            -- [warn] using weak cipher mode
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 2.3.0, Dropbear SSH 0.28
(enc) aes192-cbc                            -- [warn] using weak cipher mode
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 2.3.0
(enc) aes256-cbc                            -- [warn] using weak cipher mode
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 2.3.0, Dropbear SSH 0.47
(enc) blowfish-cbc                          -- [fail] using weak & deprecated Blowfish cipher
                                            `- [warn] using weak cipher mode
                                            `- [warn] using small 64-bit block size
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 1.2.2, Dropbear SSH 0.28
(enc) cast128-cbc                           -- [fail] using weak & deprecated CAST cipher
                                            `- [warn] using weak cipher mode
                                            `- [warn] using small 64-bit block size
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 2.1.0
(enc) 3des-cbc                              -- [fail] using broken & deprecated 3DES cipher
                                            `- [warn] using weak cipher mode
                                            `- [warn] using small 64-bit block size
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 1.2.2, Dropbear SSH 0.28

# message authentication code algorithms
(mac) umac-64-etm@openssh.com               -- [warn] using small 64-bit tag size
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 6.2
(mac) umac-128-etm@openssh.com              -- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 6.2
(mac) hmac-sha2-256-etm@openssh.com         -- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 6.2
(mac) hmac-sha2-512-etm@openssh.com         -- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 6.2
(mac) hmac-sha1-etm@openssh.com             -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] vulnerable to the Terrapin attack (CVE-2023-48795), allowing message prefix truncation
                                            `- [info] available since OpenSSH 6.2
(mac) umac-64@openssh.com                   -- [warn] using encrypt-and-MAC mode
                                            `- [warn] using small 64-bit tag size
                                            `- [info] available since OpenSSH 4.7
(mac) umac-128@openssh.com                  -- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 6.2
(mac) hmac-sha2-256                         -- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 5.9, Dropbear SSH 2013.56
(mac) hmac-sha2-512                         -- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 5.9, Dropbear SSH 2013.56
(mac) hmac-sha1                             -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 2.1.0, Dropbear SSH 0.28

# fingerprints
(fin) ssh-ed25519: SHA256:uYMZFN9vYkxFeoZ23/Znor6lCrABMH4HLFk4qNAIkB4
(fin) ssh-rsa: SHA256:LQNuGXT1aAMR0tM26b7Mw7RM4W9YybidN9yQFlwgqbI

# algorithm recommendations (for OpenSSH 7.4)
(rec) !diffie-hellman-group-exchange-sha256 -- kex algorithm to change (increase modulus size to 3072 bits or larger) 
(rec) -3des-cbc                             -- enc algorithm to remove 
(rec) -blowfish-cbc                         -- enc algorithm to remove 
(rec) -cast128-cbc                          -- enc algorithm to remove 
(rec) -diffie-hellman-group-exchange-sha1   -- kex algorithm to remove 
(rec) -diffie-hellman-group1-sha1           -- kex algorithm to remove 
(rec) -diffie-hellman-group14-sha1          -- kex algorithm to remove 
(rec) -ecdh-sha2-nistp256                   -- kex algorithm to remove 
(rec) -ecdh-sha2-nistp384                   -- kex algorithm to remove 
(rec) -ecdh-sha2-nistp521                   -- kex algorithm to remove 
(rec) -ecdsa-sha2-nistp256                  -- key algorithm to remove 
(rec) -hmac-sha1                            -- mac algorithm to remove 
(rec) -hmac-sha1-etm@openssh.com            -- mac algorithm to remove 
(rec) -ssh-rsa                              -- key algorithm to remove 
(rec) !rsa-sha2-256                         -- key algorithm to change (increase modulus size to 3072 bits or larger) 
(rec) !rsa-sha2-512                         -- key algorithm to change (increase modulus size to 3072 bits or larger) 
(rec) -aes128-cbc                           -- enc algorithm to remove 
(rec) -aes192-cbc                           -- enc algorithm to remove 
(rec) -aes256-cbc                           -- enc algorithm to remove 
(rec) -chacha20-poly1305@openssh.com        -- enc algorithm to remove 
(rec) -diffie-hellman-group14-sha256        -- kex algorithm to remove 
(rec) -hmac-sha2-256                        -- mac algorithm to remove 
(rec) -hmac-sha2-256-etm@openssh.com        -- mac algorithm to remove 
(rec) -hmac-sha2-512                        -- mac algorithm to remove 
(rec) -hmac-sha2-512-etm@openssh.com        -- mac algorithm to remove 
(rec) -umac-128-etm@openssh.com             -- mac algorithm to remove 
(rec) -umac-128@openssh.com                 -- mac algorithm to remove 
(rec) -umac-64-etm@openssh.com              -- mac algorithm to remove 
(rec) -umac-64@openssh.com                  -- mac algorithm to remove 

# additional info
(nfo) For hardening guides on common OSes, please see: <https://www.ssh-audit.com/hardening_guides.html>

```
