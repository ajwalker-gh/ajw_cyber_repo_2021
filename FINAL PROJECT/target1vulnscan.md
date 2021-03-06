nmap -sV --script vulscan/vulscan.nse -oN vulscan_target1.txt 192.168.1.110
Nmap scan report for 192.168.1.110
Host is up (0.00092s latency).
Not shown: 995 closed ports
PORT    STATE SERVICE     VERSION
22/tcp  open  ssh         OpenSSH 6.7p1 Debian 5+deb8u4 (protocol 2.0)
| vulscan: VulDB - https://vuldb.com:
| [76870] OpenSSH up to 6.9 auth2-chall.c kbdint_next_device privilege escalation
| [76326] OpenSSH 6.8 XSECURITY privilege escalation
| [12724] OpenSSH up to 6.6 Fingerprint Record Check sshconnect.c verify_host_key HostCertificate weak authentication
| [12683] OpenBSD OpenSSH up to 6.5 Configuration child_set_env Wildcard privilege escalation
| [12124] OpenSSH 6.4 J-PAKE Protocol schnorr.c hash_buffer denial of service
| [11124] OpenSSH 6.2/6.3 Post Authentication sshd process initialize mm_newkeys_from_blob privilege escalation
| 
| MITRE CVE - https://cve.mitre.org:
| [CVE-2012-5975] The SSH USERAUTH CHANGE REQUEST feature in SSH Tectia Server 6.0.4 through 6.0.20, 6.1.0 through 6.1.12, 6.2.0 through 6.2.5, and 6.3.0 through 6.3.2 on UNIX and Linux, when old-style password authentication is enabled, allows remote attackers to bypass authentication via a crafted session involving entry of blank passwords, as demonstrated by a root login session from a modified OpenSSH client with an added input_userauth_passwd_changereq call in sshconnect2.c.
| [CVE-2012-5536] A certain Red Hat build of the pam_ssh_agent_auth module on Red Hat Enterprise Linux (RHEL) 6 and Fedora Rawhide calls the glibc error function instead of the error function in the OpenSSH codebase, which allows local users to obtain sensitive information from process memory or possibly gain privileges via crafted use of an application that relies on this module, as demonstrated by su and sudo.
| [CVE-2010-5107] The default configuration of OpenSSH through 6.1 enforces a fixed time limit between establishing a TCP connection and completing a login, which makes it easier for remote attackers to cause a denial of service (connection-slot exhaustion) by periodically making many new TCP connections.
| [CVE-2008-1483] OpenSSH 4.3p2, and probably other versions, allows local users to hijack forwarded X connections by causing ssh to set DISPLAY to :10, even when another process is listening on the associated port, as demonstrated by opening TCP port 6010 (IPv4) and sniffing a cookie sent by Emacs.
| [CVE-2007-3102] Unspecified vulnerability in the linux_audit_record_event function in OpenSSH 4.3p2, as used on Fedora Core 6 and possibly other systems, allows remote attackers to write arbitrary characters to an audit log via a crafted username.  NOTE: some of these details are obtained from third party information.
| [CVE-2004-2414] Novell NetWare 6.5 SP 1.1, when installing or upgrading using the Overlay CDs and performing a custom installation with OpenSSH, includes sensitive password information in the (1) NIOUTPUT.TXT and (2) NI.LOG log files, which might allow local users to obtain the passwords.
| 
| SecurityFocus - https://www.securityfocus.com/bid/:
| [102780] OpenSSH CVE-2016-10708 Multiple Denial of Service Vulnerabilities
| [101552] OpenSSH 'sftp-server.c' Remote Security Bypass Vulnerability
| [94977] OpenSSH CVE-2016-10011 Local Information Disclosure Vulnerability
| [94975] OpenSSH CVE-2016-10012 Security Bypass Vulnerability
| [94972] OpenSSH CVE-2016-10010 Privilege Escalation Vulnerability
| [94968] OpenSSH CVE-2016-10009 Remote Code Execution Vulnerability
| [93776] OpenSSH 'ssh/kex.c' Denial of Service Vulnerability
| [92212] OpenSSH CVE-2016-6515 Denial of Service Vulnerability
| [92210] OpenSSH CBC Padding Weak Encryption Security Weakness
| [92209] OpenSSH MAC Verification Security Bypass Vulnerability
| [91812] OpenSSH CVE-2016-6210 User Enumeration Vulnerability
| [90440] OpenSSH CVE-2004-1653 Remote Security Vulnerability
| [90340] OpenSSH CVE-2004-2760 Remote Security Vulnerability
| [89385] OpenSSH CVE-2005-2666 Local Security Vulnerability
| [88655] OpenSSH CVE-2001-1382 Remote Security Vulnerability
| [88513] OpenSSH CVE-2000-0999 Remote Security Vulnerability
| [88367] OpenSSH CVE-1999-1010 Local Security Vulnerability
| [87789] OpenSSH CVE-2003-0682 Remote Security Vulnerability
| [86187] OpenSSH 'session.c' Local Security Bypass Vulnerability
| [86144] OpenSSH CVE-2007-2768 Remote Security Vulnerability
| [84427] OpenSSH CVE-2016-1908 Security Bypass Vulnerability
| [84314] OpenSSH CVE-2016-3115 Remote Command Injection Vulnerability
| [84185] OpenSSH CVE-2006-4925 Denial-Of-Service Vulnerability
| [81293] OpenSSH CVE-2016-1907 Denial of Service Vulnerability
| [80698] OpenSSH CVE-2016-0778 Heap Based Buffer Overflow Vulnerability
| [80695] OpenSSH CVE-2016-0777 Information Disclosure Vulnerability
| [76497] OpenSSH CVE-2015-6565 Local Security Bypass Vulnerability
| [76317] OpenSSH PAM Support Multiple Remote Code Execution Vulnerabilities
| [75990] OpenSSH Login Handling Security Bypass Weakness
| [75525] OpenSSH 'x11_open_helper()' Function Security Bypass Vulnerability
| [71420] Portable OpenSSH 'gss-serv-krb5.c' Security Bypass Vulnerability
| [68757] OpenSSH Multiple Remote Denial of Service Vulnerabilities
| [66459] OpenSSH Certificate Validation Security Bypass Vulnerability
| [66355] OpenSSH 'child_set_env()' Function Security Bypass Vulnerability
| [65674] OpenSSH 'ssh-keysign.c' Local Information Disclosure Vulnerability
| [65230] OpenSSH 'schnorr.c' Remote Memory Corruption Vulnerability
| [63605] OpenSSH 'sshd' Process Remote Memory Corruption Vulnerability
| [61286] OpenSSH Remote Denial of Service Vulnerability
| [58894] GSI-OpenSSH PAM_USER Security Bypass Vulnerability
| [58162] OpenSSH CVE-2010-5107 Denial of Service Vulnerability
| [54114] OpenSSH 'ssh_gssapi_parse_ename()' Function Denial of Service Vulnerability
| [51702] Debian openssh-server Forced Command Handling Information Disclosure Vulnerability
| [50416] Linux Kernel 'kdump' and 'mkdumprd' OpenSSH Integration Remote Information Disclosure Vulnerability
| [49473] OpenSSH Ciphersuite Specification Information Disclosure Weakness
| [48507] OpenSSH 'pam_thread()' Remote Buffer Overflow Vulnerability
| [47691] Portable OpenSSH 'ssh-keysign' Local Unauthorized Access Vulnerability
| [46155] OpenSSH Legacy Certificate Signing Information Disclosure Vulnerability
| [45304] OpenSSH J-PAKE Security Bypass Vulnerability
| [36552] Red Hat Enterprise Linux OpenSSH 'ChrootDirectory' Option Local Privilege Escalation Vulnerability
| [32319] OpenSSH CBC Mode Information Disclosure Vulnerability
| [30794] Red Hat OpenSSH Backdoor Vulnerability
| [30339] OpenSSH 'X11UseLocalhost' X11 Forwarding Session Hijacking Vulnerability
| [30276] Debian OpenSSH SELinux Privilege Escalation Vulnerability
| [28531] OpenSSH ForceCommand Command Execution Weakness
| [28444] OpenSSH X Connections Session Hijacking Vulnerability
| [26097] OpenSSH LINUX_AUDIT_RECORD_EVENT Remote Log Injection Weakness
| [25628] OpenSSH X11 Cookie Local Authentication Bypass Vulnerability
| [23601] OpenSSH S/Key Remote Information Disclosure Vulnerability
| [20956] OpenSSH Privilege Separation Key Signature Weakness
| [20418] OpenSSH-Portable Existing Password Remote Information Disclosure Weakness
| [20245] OpenSSH-Portable GSSAPI Authentication Abort Information Disclosure Weakness
| [20241] Portable OpenSSH GSSAPI Remote Code Execution Vulnerability
| [20216] OpenSSH Duplicated Block Remote Denial of Service Vulnerability
| [16892] OpenSSH Remote PAM Denial Of Service Vulnerability
| [14963] OpenSSH LoginGraceTime Remote Denial Of Service Vulnerability
| [14729] OpenSSH GSSAPI Credential Disclosure Vulnerability
| [14727] OpenSSH DynamicForward Inadvertent GatewayPorts Activation Vulnerability
| [11781] OpenSSH-portable PAM Authentication Remote Information Disclosure Vulnerability
| [9986] RCP, OpenSSH SCP Client File Corruption Vulnerability
| [9040] OpenSSH PAM Conversation Memory Scrubbing Weakness
| [8677] Multiple Portable OpenSSH PAM Vulnerabilities
| [8628] OpenSSH Buffer Mismanagement Vulnerabilities
| [7831] OpenSSH Reverse DNS Lookup Access Control Bypass Vulnerability
| [7482] OpenSSH Remote Root Authentication Timing Side-Channel Weakness
| [7467] OpenSSH-portable Enabled PAM Delay Information Disclosure Vulnerability
| [7343] OpenSSH Authentication Execution Path Timing Information Leakage Weakness
| [6168] OpenSSH Visible Password Vulnerability
| [5374] OpenSSH Trojan Horse Vulnerability
| [5093] OpenSSH Challenge-Response Buffer Overflow Vulnerabilities
| [4560] OpenSSH Kerberos 4 TGT/AFS Token Buffer Overflow Vulnerability
| [4241] OpenSSH Channel Code Off-By-One Vulnerability
| [3614] OpenSSH UseLogin Environment Variable Passing Vulnerability
| [3560] OpenSSH Kerberos Arbitrary Privilege Elevation Vulnerability
| [3369] OpenSSH Key Based Source IP Access Control Bypass Vulnerability
| [3345] OpenSSH SFTP Command Restriction Bypassing Vulnerability
| [2917] OpenSSH PAM Session Evasion Vulnerability
| [2825] OpenSSH Client X11 Forwarding Cookie Removal File Symbolic Link Vulnerability
| [2356] OpenSSH Private Key Authentication Check Vulnerability
| [1949] OpenSSH Client Unauthorized Remote Forwarding Vulnerability
| [1334] OpenSSH UseLogin Vulnerability
| 
| IBM X-Force - https://exchange.xforce.ibmcloud.com:
| [83258] GSI-OpenSSH auth-pam.c security bypass
| [82781] OpenSSH time limit denial of service
| [82231] OpenSSH pam_ssh_agent_auth PAM code execution
| [74809] OpenSSH ssh_gssapi_parse_ename denial of service
| [72756] Debian openssh-server commands information disclosure
| [68339] OpenSSH pam_thread buffer overflow
| [67264] OpenSSH ssh-keysign unauthorized access
| [65910] OpenSSH remote_glob function denial of service
| [65163] OpenSSH certificate information disclosure
| [64387] OpenSSH J-PAKE security bypass
| [63337] Cisco Unified Videoconferencing OpenSSH weak security
| [46620] OpenSSH and multiple SSH Tectia products CBC mode information disclosure
| [45202] OpenSSH signal handler denial of service
| [44747] RHEL OpenSSH backdoor
| [44280] OpenSSH PermitRootLogin information disclosure
| [44279] OpenSSH sshd weak security
| [44037] OpenSSH sshd SELinux role unauthorized access
| [43940] OpenSSH X11 forwarding information disclosure
| [41549] OpenSSH ForceCommand directive security bypass
| [41438] OpenSSH sshd session hijacking
| [40897] OpenSSH known_hosts weak security
| [40587] OpenSSH username weak security
| [37371] OpenSSH username data manipulation
| [37118] RHSA update for OpenSSH privilege separation monitor authentication verification weakness not installed
| [37112] RHSA update for OpenSSH signal handler race condition not installed
| [37107] RHSA update for OpenSSH identical block denial of service not installed
| [36637] OpenSSH X11 cookie privilege escalation
| [35167] OpenSSH packet.c newkeys[mode] denial of service
| [34490] OpenSSH OPIE information disclosure
| [33794] OpenSSH ChallengeResponseAuthentication information disclosure
| [32975] Apple Mac OS X OpenSSH denial of service
| [32387] RHSA-2006:0738 updates for openssh not installed
| [32359] RHSA-2006:0697 updates for openssh not installed
| [32230] RHSA-2006:0298 updates for openssh not installed
| [32132] RHSA-2006:0044 updates for openssh not installed
| [30120] OpenSSH privilege separation monitor authentication verification weakness
| [29255] OpenSSH GSSAPI user enumeration
| [29254] OpenSSH signal handler race condition
| [29158] OpenSSH identical block denial of service
| [28147] Apple Mac OS X OpenSSH nonexistent user login denial of service
| [25116] OpenSSH OpenPAM denial of service
| [24305] OpenSSH SCP shell expansion command execution
| [22665] RHSA-2005:106 updates for openssh not installed
| [22117] OpenSSH GSSAPI allows elevated privileges
| [22115] OpenSSH GatewayPorts security bypass
| [20930] OpenSSH sshd.c LoginGraceTime denial of service
| [19441] Sun Solaris OpenSSH LDAP (1) client authentication denial of service
| [17213] OpenSSH allows port bouncing attacks
| [16323] OpenSSH scp file overwrite
| [13797] OpenSSH PAM information leak
| [13271] OpenSSH could allow an attacker to corrupt the PAM conversion stack
| [13264] OpenSSH PAM code could allow an attacker to gain access
| [13215] OpenSSH buffer management errors could allow an attacker to execute code
| [13214] OpenSSH memory vulnerabilities
| [13191] OpenSSH large packet buffer overflow
| [12196] OpenSSH could allow an attacker to bypass login restrictions
| [11970] OpenSSH could allow an attacker to obtain valid administrative account
| [11902] OpenSSH PAM support enabled information leak
| [9803] OpenSSH &quot
| [9763] OpenSSH downloaded from the OpenBSD FTP site or OpenBSD FTP mirror sites could contain a Trojan Horse
| [9307] OpenSSH is running on the system
| [9169] OpenSSH &quot
| [8896] OpenSSH Kerberos 4 TGT/AFS buffer overflow
| [8697] FreeBSD libutil in OpenSSH fails to drop privileges prior to using the login class capability database
| [8383] OpenSSH off-by-one error in channel code
| [7647] OpenSSH UseLogin option arbitrary code execution
| [7634] OpenSSH using sftp and restricted keypairs could allow an attacker to bypass restrictions
| [7598] OpenSSH with Kerberos allows attacker to gain elevated privileges
| [7179] OpenSSH source IP access control bypass
| [6757] OpenSSH &quot
| [6676] OpenSSH X11 forwarding symlink attack could allow deletion of arbitrary files
| [6084] OpenSSH 2.3.1 allows remote users to bypass authentication
| [5517] OpenSSH allows unauthorized access to resources
| [4646] OpenSSH UseLogin option allows remote users to execute commands as root
| 
| Exploit-DB - https://www.exploit-db.com:
| [14866] Novell Netware 6.5 - OpenSSH Remote Stack Overflow
| 
| OpenVAS (Nessus) - http://www.openvas.org:
| [902488] OpenSSH 'sshd' GSSAPI Credential Disclosure Vulnerability
| [900179] OpenSSH CBC Mode Information Disclosure Vulnerability
| [881183] CentOS Update for openssh CESA-2012:0884 centos6 
| [880802] CentOS Update for openssh CESA-2009:1287 centos5 i386
| [880746] CentOS Update for openssh CESA-2009:1470 centos5 i386
| [870763] RedHat Update for openssh RHSA-2012:0884-04
| [870129] RedHat Update for openssh RHSA-2008:0855-01
| [861813] Fedora Update for openssh FEDORA-2010-5429
| [861319] Fedora Update for openssh FEDORA-2007-395
| [861170] Fedora Update for openssh FEDORA-2007-394
| [861012] Fedora Update for openssh FEDORA-2007-715
| [840345] Ubuntu Update for openssh vulnerability USN-597-1
| [840300] Ubuntu Update for openssh update USN-612-5
| [840271] Ubuntu Update for openssh vulnerability USN-612-2
| [840268] Ubuntu Update for openssh update USN-612-7
| [840259] Ubuntu Update for openssh vulnerabilities USN-649-1
| [840214] Ubuntu Update for openssh vulnerability USN-566-1
| [831074] Mandriva Update for openssh MDVA-2010:162 (openssh)
| [830929] Mandriva Update for openssh MDVA-2010:090 (openssh)
| [830807] Mandriva Update for openssh MDVA-2010:026 (openssh)
| [830603] Mandriva Update for openssh MDVSA-2008:098 (openssh)
| [830523] Mandriva Update for openssh MDVSA-2008:078 (openssh)
| [830317] Mandriva Update for openssh-askpass-qt MDKA-2007:127 (openssh-askpass-qt)
| [830191] Mandriva Update for openssh MDKSA-2007:236 (openssh)
| [802407] OpenSSH 'sshd' Challenge Response Authentication Buffer Overflow Vulnerability
| [103503] openssh-server Forced Command Handling Information Disclosure Vulnerability
| [103247] OpenSSH Ciphersuite Specification Information Disclosure Weakness
| [103064] OpenSSH Legacy Certificate Signing Information Disclosure Vulnerability
| [100584] OpenSSH X Connections Session Hijacking Vulnerability
| [100153] OpenSSH CBC Mode Information Disclosure Vulnerability
| [66170] CentOS Security Advisory CESA-2009:1470 (openssh)
| [65987] SLES10: Security update for OpenSSH
| [65819] SLES10: Security update for OpenSSH
| [65514] SLES9: Security update for OpenSSH
| [65513] SLES9: Security update for OpenSSH
| [65334] SLES9: Security update for OpenSSH
| [65248] SLES9: Security update for OpenSSH
| [65218] SLES9: Security update for OpenSSH
| [65169] SLES9: Security update for openssh,openssh-askpass
| [65126] SLES9: Security update for OpenSSH
| [65019] SLES9: Security update for OpenSSH
| [65015] SLES9: Security update for OpenSSH
| [64931] CentOS Security Advisory CESA-2009:1287 (openssh)
| [61639] Debian Security Advisory DSA 1638-1 (openssh)
| [61030] Debian Security Advisory DSA 1576-2 (openssh)
| [61029] Debian Security Advisory DSA 1576-1 (openssh)
| [60840] FreeBSD Security Advisory (FreeBSD-SA-08:05.openssh.asc)
| [60803] Gentoo Security Advisory GLSA 200804-03 (openssh)
| [60667] Slackware Advisory SSA:2008-095-01 openssh 
| [59014] Slackware Advisory SSA:2007-255-01 openssh 
| [58741] Gentoo Security Advisory GLSA 200711-02 (openssh)
| [57919] Gentoo Security Advisory GLSA 200611-06 (openssh)
| [57895] Gentoo Security Advisory GLSA 200609-17 (openssh)
| [57585] Debian Security Advisory DSA 1212-1 (openssh (1:3.8.1p1-8.sarge.6))
| [57492] Slackware Advisory SSA:2006-272-02 openssh 
| [57483] Debian Security Advisory DSA 1189-1 (openssh-krb5)
| [57476] FreeBSD Security Advisory (FreeBSD-SA-06:22.openssh.asc)
| [57470] FreeBSD Ports: openssh
| [56352] FreeBSD Security Advisory (FreeBSD-SA-06:09.openssh.asc)
| [56330] Gentoo Security Advisory GLSA 200602-11 (OpenSSH)
| [56294] Slackware Advisory SSA:2006-045-06 openssh 
| [53964] Slackware Advisory SSA:2003-266-01 New OpenSSH packages 
| [53885] Slackware Advisory SSA:2003-259-01 OpenSSH Security Advisory 
| [53884] Slackware Advisory SSA:2003-260-01 OpenSSH updated again 
| [53788] Debian Security Advisory DSA 025-1 (openssh)
| [52638] FreeBSD Security Advisory (FreeBSD-SA-03:15.openssh.asc)
| [52635] FreeBSD Security Advisory (FreeBSD-SA-03:12.openssh.asc)
| [11343] OpenSSH Client Unauthorized Remote Forwarding
| [10954] OpenSSH AFS/Kerberos ticket/token passing
| [10883] OpenSSH Channel Code Off by 1
| [10823] OpenSSH UseLogin Environment Variables
| 
| SecurityTracker - https://www.securitytracker.com:
| [1028187] OpenSSH pam_ssh_agent_auth Module on Red Hat Enterprise Linux Lets Remote Users Execute Arbitrary Code
| [1026593] OpenSSH Lets Remote Authenticated Users Obtain Potentially Sensitive Information
| [1025739] OpenSSH on FreeBSD Has Buffer Overflow in pam_thread() That Lets Remote Users Execute Arbitrary Code
| [1025482] OpenSSH ssh-keysign Utility Lets Local Users Gain Elevated Privileges
| [1025028] OpenSSH Legacy Certificates May Disclose Stack Contents to Remote Users
| [1022967] OpenSSH on Red Hat Enterprise Linux Lets Remote Authenticated Users Gain Elevated Privileges
| [1021235] OpenSSH CBC Mode Error Handling May Let Certain Remote Users Obtain Plain Text in Certain Cases
| [1020891] OpenSSH on Debian Lets Remote Users Prevent Logins
| [1020730] OpenSSH for Red Hat Enterprise Linux Packages May Have Been Compromised
| [1020537] OpenSSH on HP-UX Lets Local Users Hijack X11 Sessions
| [1019733] OpenSSH Unsafe Default Configuration May Let Local Users Execute Arbitrary Commands
| [1019707] OpenSSH Lets Local Users Hijack Forwarded X Sessions in Certain Cases
| [1017756] Apple OpenSSH Key Generation Process Lets Remote Users Deny Service
| [1017183] OpenSSH Privilege Separation Monitor Validation Error May Cause the Monitor to Fail to Properly Control the Unprivileged Process
| [1016940] OpenSSH Race Condition in Signal Handler Lets Remote Users Deny Service and May Potentially Permit Code Execution
| [1016939] OpenSSH GSSAPI Authentication Abort Error Lets Remote Users Determine Valid Usernames
| [1016931] OpenSSH SSH v1 CRC Attack Detection Implementation Lets Remote Users Deny Service
| [1016672] OpenSSH on Mac OS X Lets Remote Users Deny Service
| [1015706] OpenSSH Interaction With OpenPAM Lets Remote Users Deny Service
| [1015540] OpenSSH scp Double Shell Character Expansion During Local-to-Local Copying May Let Local Users Gain Elevated Privileges in Certain Cases
| [1014845] OpenSSH May Unexpectedly Activate GatewayPorts and Also May Disclose GSSAPI Credentials in Certain Cases
| [1011193] OpenSSH scp Directory Traversal Flaw Lets Remote SSH Servers Overwrite Files in Certain Cases
| [1011143] OpenSSH Default Configuration May Be Unsafe When Used With Anonymous SSH Services
| [1007791] Portable OpenSSH PAM free() Bug May Let Remote Users Execute Root Code
| [1007716] OpenSSH buffer_append_space() and Other Buffer Management Errors May Let Remote Users Execute Arbitrary Code
| [1006926] OpenSSH Host Access Restrictions Can Be Bypassed By Remote Users
| [1006688] OpenSSH Timing Flaw With Pluggable Authentication Modules Can Disclose Valid User Account Names to Remote Users
| [1004818] OpenSSH's Secure Shell (SSH) Implementation Weakness May Disclose User Passwords to Remote Users During Man-in-the-Middle Attacks
| [1004616] OpenSSH Integer Overflow and Buffer Overflow May Allow Remote Users to Gain Root Access to the System
| [1004391] OpenSSH 'BSD_AUTH' Access Control Bug May Allow Unauthorized Remote Users to Authenticated to the System
| [1004115] OpenSSH Buffer Overflow in Kerberos Ticket and AFS Token Processing Lets Local Users Execute Arbitrary Code With Root Level Permissions
| [1003758] OpenSSH Off-by-one 'Channels' Bug May Let Authorized Remote Users Execute Arbitrary Code with Root Privileges
| [1002895] OpenSSH UseLogin Environment Variable Bug Lets Local Users Execute Commands and Gain Root Access
| [1002748] OpenSSH 3.0 Denial of Service Condition May Allow Remote Users to Crash the sshd Daemon and KerberosV Configuration Error May Allow Remote Users to Partially Authenticate When Authentication Should Not Be Permitted
| [1002734] OpenSSH's S/Key Implementation Information Disclosure Flaw Provides Remote Users With Information About Valid User Accounts
| [1002455] OpenSSH May Fail to Properly Restrict IP Addresses in Certain Configurations
| [1002432] OpenSSH's Sftp-server Subsystem Lets Authorized Remote Users with Restricted Keypairs Obtain Additional Access on the Server
| [1001683] OpenSSH Allows Authorized Users to Delete Other User Files Named Cookies
| 
| OSVDB - http://www.osvdb.org:
| [92034] GSI-OpenSSH auth-pam.c Memory Management Authentication Bypass
| [90474] Red Hat / Fedora PAM Module for OpenSSH Incorrect error() Function Calling Local Privilege Escalation
| [90007] OpenSSH logingracetime / maxstartup Threshold Connection Saturation Remote DoS
| [81500] OpenSSH gss-serv.c ssh_gssapi_parse_ename Function Field Length Value Parsing Remote DoS
| [78706] OpenSSH auth-options.c sshd auth_parse_options Function authorized_keys Command Option Debug Message Information Disclosure
| [75753] OpenSSH PAM Module Aborted Conversation Local Information Disclosure
| [75249] OpenSSH sftp-glob.c remote_glob Function Glob Expression Parsing Remote DoS
| [75248] OpenSSH sftp.c process_put Function Glob Expression Parsing Remote DoS
| [72183] Portable OpenSSH ssh-keysign ssh-rand-helper Utility File Descriptor Leak Local Information Disclosure
| [70873] OpenSSH Legacy Certificates Stack Memory Disclosure
| [69658] OpenSSH J-PAKE Public Parameter Validation Shared Secret Authentication Bypass
| [67743] Novell NetWare OpenSSH SSHD.NLM Absolute Path Handling Remote Overflow
| [59353] OpenSSH sshd Local TCP Redirection Connection Masking Weakness
| [58495] OpenSSH sshd ChrootDirectory Feature SetUID Hard Link Local Privilege Escalation
| [56921] OpenSSH Unspecified Remote Compromise
| [53021] OpenSSH on ftp.openbsd.org Trojaned Distribution
| [50036] OpenSSH CBC Mode Chosen Ciphertext 32-bit Chunk Plaintext Context Disclosure
| [49386] OpenSSH sshd TCP Connection State Remote Account Enumeration
| [48791] OpenSSH on Debian sshd Crafted Username Arbitrary Remote SELinux Role Access
| [47635] OpenSSH Packages on Red Hat Enterprise Linux Compromised Distribution
| [47227] OpenSSH X11UseLocalhost X11 Forwarding Port Hijacking
| [45873] Cisco WebNS SSHield w/ OpenSSH Crafted Large Packet Remote DoS
| [43911] OpenSSH ~/.ssh/rc ForceCommand Bypass Arbitrary Command Execution
| [43745] OpenSSH X11 Forwarding Local Session Hijacking
| [43371] OpenSSH Trusted X11 Cookie Connection Policy Bypass
| [39214] OpenSSH linux_audit_record_event Crafted Username Audit Log Injection
| [37315] pam_usb OpenSSH Authentication Unspecified Issue
| [34850] OpenSSH on Mac OS X Key Generation Remote Connection DoS
| [34601] OPIE w/ OpenSSH Account Enumeration
| [34600] OpenSSH S/KEY Authentication Account Enumeration
| [32721] OpenSSH Username Password Complexity Account Enumeration
| [30232] OpenSSH Privilege Separation Monitor Weakness
| [29494] OpenSSH packet.c Invalid Protocol Sequence Remote DoS
| [29266] OpenSSH GSSAPI Authentication Abort Username Enumeration
| [29264] OpenSSH Signal Handler Pre-authentication Race Condition Code Execution
| [29152] OpenSSH Identical Block Packet DoS
| [27745] Apple Mac OS X OpenSSH Nonexistent Account Login Enumeration DoS
| [23797] OpenSSH with OpenPAM Connection Saturation Forked Process Saturation DoS
| [22692] OpenSSH scp Command Line Filename Processing Command Injection
| [20216] OpenSSH with KerberosV Remote Authentication Bypass
| [19142] OpenSSH Multiple X11 Channel Forwarding Leaks
| [19141] OpenSSH GSSAPIAuthentication Credential Escalation
| [18236] OpenSSH no pty Command Execution Local PAM Restriction Bypass
| [16567] OpenSSH Privilege Separation LoginGraceTime DoS
| [16039] Solaris 108994 Series Patch OpenSSH LDAP Client Authentication DoS
| [9562] OpenSSH Default Configuration Anon SSH Service Port Bounce Weakness
| [9550] OpenSSH scp Traversal Arbitrary File Overwrite
| [6601] OpenSSH *realloc() Unspecified Memory Errors
| [6245] OpenSSH SKEY/BSD_AUTH Challenge-Response Remote Overflow
| [6073] OpenSSH on FreeBSD libutil Arbitrary File Read
| [6072] OpenSSH PAM Conversation Function Stack Modification
| [6071] OpenSSH SSHv1 PAM Challenge-Response Authentication Privilege Escalation
| [5536] OpenSSH sftp-server Restricted Keypair Restriction Bypass
| [5408] OpenSSH echo simulation Information Disclosure
| [5113] OpenSSH NIS YP Netgroups Authentication Bypass
| [4536] OpenSSH Portable AIX linker Privilege Escalation
| [3938] OpenSSL and OpenSSH /dev/random Check Failure
| [3456] OpenSSH buffer_append_space() Heap Corruption
| [2557] OpenSSH Multiple Buffer Management Multiple Overflows
| [2140] OpenSSH w/ PAM Username Validity Timing Attack
| [2112] OpenSSH Reverse DNS Lookup Bypass
| [2109] OpenSSH sshd Root Login Timing Side-Channel Weakness
| [1853] OpenSSH Symbolic Link 'cookies' File Removal
| [839] OpenSSH PAMAuthenticationViaKbdInt Challenge-Response Remote Overflow
| [781] OpenSSH Kerberos TGT/AFS Token Passing Remote Overflow
| [730] OpenSSH Channel Code Off by One Remote Privilege Escalation
| [688] OpenSSH UseLogin Environment Variable Local Command Execution
| [642] OpenSSH Multiple Key Type ACL Bypass
| [504] OpenSSH SSHv2 Public Key Authentication Bypass
| [341] OpenSSH UseLogin Local Privilege Escalation
|_
80/tcp  open  http        Apache httpd 2.4.10 ((Debian))
|_http-server-header: Apache/2.4.10 (Debian)
| vulscan: VulDB - https://vuldb.com:
| [68575] Apache HTTP Server up to 2.4.10 LuaAuthzProvider mod_lua.c privilege escalation
| [68435] Apache HTTP Server 2.4.10 mod_proxy_fcgi.c handle_headers denial of service
| [88747] Apache HTTP Server 2.4.17/2.4.18 mod_http2 denial of service
| [76731] Apache HTTP Server 2.4.12 ErrorDocument 400 Crash denial of service
| [74367] Apache HTTP Server up to 2.4.12 mod_lua lua_request.c wsupgrade denial of service
| [13300] Apache HTTP Server 2.4.1/2.4.2 mod_wsgi setuid privilege escalation
| [13299] Apache HTTP Server 2.4.1/2.4.2 mod_wsgi Content-Type Header information disclosure
| 
| MITRE CVE - https://cve.mitre.org:
| [CVE-2013-2249] mod_session_dbd.c in the mod_session_dbd module in the Apache HTTP Server before 2.4.5 proceeds with save operations for a session without considering the dirty flag and the requirement for a new session ID, which has unspecified impact and remote attack vectors.
| [CVE-2012-4558] Multiple cross-site scripting (XSS) vulnerabilities in the balancer_handler function in the manager interface in mod_proxy_balancer.c in the mod_proxy_balancer module in the Apache HTTP Server 2.2.x before 2.2.24-dev and 2.4.x before 2.4.4 allow remote attackers to inject arbitrary web script or HTML via a crafted string.
| [CVE-2012-3502] The proxy functionality in (1) mod_proxy_ajp.c in the mod_proxy_ajp module and (2) mod_proxy_http.c in the mod_proxy_http module in the Apache HTTP Server 2.4.x before 2.4.3 does not properly determine the situations that require closing a back-end connection, which allows remote attackers to obtain sensitive information in opportunistic circumstances by reading a response that was intended for a different client.
| [CVE-2012-3499] Multiple cross-site scripting (XSS) vulnerabilities in the Apache HTTP Server 2.2.x before 2.2.24-dev and 2.4.x before 2.4.4 allow remote attackers to inject arbitrary web script or HTML via vectors involving hostnames and URIs in the (1) mod_imagemap, (2) mod_info, (3) mod_ldap, (4) mod_proxy_ftp, and (5) mod_status modules.
| [CVE-2012-3451] Apache CXF before 2.4.9, 2.5.x before 2.5.5, and 2.6.x before 2.6.2 allows remote attackers to execute unintended web-service operations by sending a header with a SOAP Action String that is inconsistent with the message body.
| [CVE-2012-2687] Multiple cross-site scripting (XSS) vulnerabilities in the make_variant_list function in mod_negotiation.c in the mod_negotiation module in the Apache HTTP Server 2.4.x before 2.4.3, when the MultiViews option is enabled, allow remote attackers to inject arbitrary web script or HTML via a crafted filename that is not properly handled during construction of a variant list.
| [CVE-2012-2379] Apache CXF 2.4.x before 2.4.8, 2.5.x before 2.5.4, and 2.6.x before 2.6.1, when a Supporting Token specifies a child WS-SecurityPolicy 1.1 or 1.2 policy, does not properly ensure that an XML element is signed or encrypted, which has unspecified impact and attack vectors.
| [CVE-2012-2378] Apache CXF 2.4.5 through 2.4.7, 2.5.1 through 2.5.3, and 2.6.x before 2.6.1, does not properly enforce child policies of a WS-SecurityPolicy 1.1 SupportingToken policy on the client side, which allows remote attackers to bypass the (1) AlgorithmSuite, (2) SignedParts, (3) SignedElements, (4) EncryptedParts, and (5) EncryptedElements policies.
| [CVE-2012-0883] envvars (aka envvars-std) in the Apache HTTP Server before 2.4.2 places a zero-length directory name in the LD_LIBRARY_PATH, which allows local users to gain privileges via a Trojan horse DSO in the current working directory during execution of apachectl.
| [CVE-2011-2516] Off-by-one error in the XML signature feature in Apache XML Security for C++ 1.6.0, as used in Shibboleth before 2.4.3 and possibly other products, allows remote attackers to cause a denial of service (crash) via a signature using a large RSA key, which triggers a buffer overflow.
| 
| SecurityFocus - https://www.securityfocus.com/bid/:
| [42102] Apache 'mod_proxy_http' 2.2.9 for Unix Timeout Handling Information Disclosure Vulnerability
| [27237] Apache HTTP Server 2.2.6, 2.0.61 and 1.3.39 'mod_status' Cross-Site Scripting Vulnerability
| [15413] PHP Apache 2 Virtual() Safe_Mode and Open_Basedir Restriction Bypass Vulnerability
| [15177] PHP Apache 2 Local Denial of Service Vulnerability
| [6065] Apache 2 WebDAV CGI POST Request Information Disclosure Vulnerability
| [5816] Apache 2 mod_dav Denial Of Service Vulnerability
| [5486] Apache 2.0 CGI Path Disclosure Vulnerability
| [5485] Apache 2.0 Path Disclosure Vulnerability
| [5434] Apache 2.0 Encoded Backslash Directory Traversal Vulnerability
| [5256] Apache httpd 2.0 CGI Error Path Disclosure Vulnerability
| [4057] Apache 2 for Windows OPTIONS request Path Disclosure Vulnerability
| [4056] Apache 2 for Windows php.exe Path Disclosure Vulnerability
| 
| IBM X-Force - https://exchange.xforce.ibmcloud.com:
| [75211] Debian GNU/Linux apache 2 cross-site scripting
| 
| Exploit-DB - https://www.exploit-db.com:
| [31052] Apache <= 2.2.6 'mod_negotiation' HTML Injection and HTTP Response Splitting Vulnerability
| [30901] Apache HTTP Server 2.2.6 Windows Share PHP File Extension Mapping Information Disclosure Vulnerability
| [30835] Apache HTTP Server <= 2.2.4 413 Error HTTP Request Method Cross-Site Scripting Weakness
| [28424] Apache 2.x HTTP Server Arbitrary HTTP Request Headers Security Weakness
| [28365] Apache 2.2.2 CGI Script Source Code Information Disclosure Vulnerability
| [27915] Apache James 2.2 SMTP Denial of Service Vulnerability
| [27135] Apache Struts 2 DefaultActionMapper Prefixes OGNL Code Execution
| [26710] Apache CXF prior to 2.5.10, 2.6.7 and 2.7.4 - Denial of Service
| [24590] Apache 2.0.x mod_ssl Remote Denial of Service Vulnerability
| [23581] Apache 2.0.4x mod_perl Module File Descriptor Leakage Vulnerability
| [23482] Apache 2.0.4x mod_php Module File Descriptor Leakage Vulnerability (2)
| [23481] Apache 2.0.4x mod_php Module File Descriptor Leakage Vulnerability (1)
| [23296] Red Hat Apache 2.0.40 Directory Index Default Configuration Error
| [23282] apache cocoon 2.14/2.2 - Directory Traversal vulnerability
| [22191] Apache Web Server 2.0.x MS-DOS Device Name Denial of Service Vulnerability
| [21854] Apache 2.0.39/40 Oversized STDERR Buffer Denial of Service Vulnerability
| [21719] Apache 2.0 Path Disclosure Vulnerability
| [21697] Apache 2.0 Encoded Backslash Directory Traversal Vulnerability
| [20272] Apache 1.2.5/1.3.1,UnityMail 2.0 MIME Header DoS Vulnerability
| [19828] Cobalt RaQ 2.0/3.0 Apache .htaccess Disclosure Vulnerability
| [18984] Apache Struts <= 2.2.1.1 - Remote Command Execution
| [18329] Apache Struts2 <= 2.3.1 - Multiple Vulnerabilities
| [17691] Apache Struts < 2.2.0 - Remote Command Execution
| [15319] Apache 2.2 (Windows) Local Denial of Service
| [14617] Apache JackRabbit 2.0.0 webapp XPath Injection
| [11650] Apache 2.2.14 mod_isapi Dangling Pointer Remote SYSTEM Exploit
| [8458] Apache Geronimo <= 2.1.3 - Multiple Directory Traversal Vulnerabilities
| [5330] Apache 2.0 mod_jk2 2.0.2 - Remote Buffer Overflow Exploit (win32)
| [3996] Apache 2.0.58 mod_rewrite Remote Overflow Exploit (win2k3)
| [2237] Apache < 1.3.37, 2.0.59, 2.2.3 (mod_rewrite) Remote Overflow PoC
| [1056] Apache <= 2.0.49 Arbitrary Long HTTP Headers Denial of Service
| [855] Apache <= 2.0.52 HTTP GET request Denial of Service Exploit
| [132] Apache 1.3.x - 2.0.48 - mod_userdir Remote Users Disclosure Exploit
| [38] Apache <= 2.0.45 APR Remote Exploit -Apache-Knacker.pl
| [34] Webfroot Shoutbox < 2.32 (Apache) Remote Exploit
| [11] Apache <= 2.0.44 Linux Remote Denial of Service Exploit
| [9] Apache HTTP Server 2.x Memory Leak Exploit
| 
| OpenVAS (Nessus) - http://www.openvas.org:
| [855524] Solaris Update for Apache 2 120544-14
| [855077] Solaris Update for Apache 2 120543-14
| [100858] Apache 'mod_proxy_http' 2.2.9 for Unix Timeout Handling Information Disclosure Vulnerability
| [72626] Debian Security Advisory DSA 2579-1 (apache2)
| [71551] Gentoo Security Advisory GLSA 201206-25 (apache)
| [71550] Gentoo Security Advisory GLSA 201206-24 (apache tomcat)
| [71485] Debian Security Advisory DSA 2506-1 (libapache-mod-security)
| [71256] Debian Security Advisory DSA 2452-1 (apache2)
| [71238] Debian Security Advisory DSA 2436-1 (libapache2-mod-fcgid)
| [70724] Debian Security Advisory DSA 2405-1 (apache2)
| [70235] Debian Security Advisory DSA 2298-2 (apache2)
| [70233] Debian Security Advisory DSA 2298-1 (apache2)
| [69988] Debian Security Advisory DSA 2279-1 (libapache2-mod-authnz-external)
| [69338] Debian Security Advisory DSA 2202-1 (apache2)
| [65131] SLES9: Security update for Apache 2 oes/CORE
| [64426] Gentoo Security Advisory GLSA 200907-04 (apache)
| [61381] Gentoo Security Advisory GLSA 200807-06 (apache)
| [60582] Gentoo Security Advisory GLSA 200803-19 (apache)
| [58745] Gentoo Security Advisory GLSA 200711-06 (apache)
| [57851] Gentoo Security Advisory GLSA 200608-01 (apache)
| [56246] Gentoo Security Advisory GLSA 200602-03 (Apache)
| [55392] Gentoo Security Advisory GLSA 200509-12 (Apache)
| [55129] Gentoo Security Advisory GLSA 200508-15 (apache)
| [54739] Gentoo Security Advisory GLSA 200411-18 (apache)
| [54724] Gentoo Security Advisory GLSA 200411-03 (apache)
| [54712] Gentoo Security Advisory GLSA 200410-21 (apache)
| [54689] Gentoo Security Advisory GLSA 200409-33 (net=www/apache)
| [54677] Gentoo Security Advisory GLSA 200409-21 (apache)
| [54610] Gentoo Security Advisory GLSA 200407-03 (Apache)
| [54601] Gentoo Security Advisory GLSA 200406-16 (Apache)
| [54590] Gentoo Security Advisory GLSA 200406-05 (Apache)
| [54582] Gentoo Security Advisory GLSA 200405-22 (Apache)
| [54529] Gentoo Security Advisory GLSA 200403-04 (Apache)
| [54499] Gentoo Security Advisory GLSA 200310-04 (Apache)
| [54498] Gentoo Security Advisory GLSA 200310-03 (Apache)
| [11092] Apache 2.0.39 Win32 directory traversal
| [66081] SLES11: Security update for Apache 2
| [66074] SLES10: Security update for Apache 2
| [66070] SLES9: Security update for Apache 2
| [65893] SLES10: Security update for Apache 2
| [65888] SLES10: Security update for Apache 2
| [65510] SLES9: Security update for Apache 2
| [65249] SLES9: Security update for Apache 2
| [65230] SLES9: Security update for Apache 2
| [65228] SLES9: Security update for Apache 2
| [65207] SLES9: Security update for Apache 2
| [65136] SLES9: Security update for Apache 2
| [65017] SLES9: Security update for Apache 2
| 
| SecurityTracker - https://www.securitytracker.com:
| [1008196] Apache 2.x on Windows May Return Unexpected Files For URLs Ending With Certain Characters
| [1007143] Apache 2.0 Web Server May Use a Weaker Encryption Implementation Than Specified in Some Cases
| [1006444] Apache 2.0 Web Server Line Feed Buffer Allocation Flaw Lets Remote Users Deny Service
| [1005963] Apache Web Server 2.x Windows Device Access Flaw Lets Remote Users Crash the Server or Possibly Execute Arbitrary Code
| [1004770] Apache 2.x Web Server ap_log_rerror() Function May Disclose Full Installation Path to Remote Users
| 
| OSVDB - http://www.osvdb.org:
| [20897] PHP w/ Apache 2 SAPI virtual() Function Unspecified INI Setting Disclosure
|_
111/tcp open  rpcbind     2-4 (RPC #100000)
| rpcinfo: 
|   program version    port/proto  service
|   100000  2,3,4        111/tcp   rpcbind
|   100000  2,3,4        111/udp   rpcbind
|   100000  3,4          111/tcp6  rpcbind
|   100000  3,4          111/udp6  rpcbind
|   100024  1          36368/udp   status
|   100024  1          39976/udp6  status
|   100024  1          53047/tcp   status
|_  100024  1          57152/tcp6  status
139/tcp open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
| vulscan: VulDB - https://vuldb.com:
| [69204] Samba 3.6.24/4.0.24/4.1.16/4.2.0 smbd _netr_ServerPasswordSet privilege escalation
| [4585] Samba smbd up to 3.6.3 Connection Request Parser denial of service
| [82409] Samba 3.0/4.2.9/4.3.6/4.4.0 IPC Traffic privilege escalation
| [82406] Samba 3.6/4.2.9/4.3.6/4.4.0 LDAP Client privilege escalation
| [82405] Samba 3.6/4.2.9/4.3.6/4.4.0 Netlogon Service spoofing
| [82404] Samba 3.6/4.2.9/4.3.6/4.4.0 NTLMSSP privilege escalation
| [82403] Samba 3.6/4.2.9/4.3.6/4.4.0 DCE-RPC CPU Exhaustion denial of service
| [13388] Samba up to 3.6.23/4.0.17/4.1.7 vfs Shadow Copy information disclosure
| [65614] Samba up to 3.0.2a Access Restriction winbind_name_list_to_sid_string_list unknown vulnerability
| [9859] Samba up to 3.5.21 Packet nttrans.c read_nttrans_ea_list denial of service
| [7995] Asus RT-N66U Router 3.0.0.4.270 Samba Root Share Eingabe unknown vulnerability
| [8152] Samba up to 3.6.5 SMB2 Implementation privilege escalation
| [63488] Samba up to 3.5.18 Web Administration Tool cross site request forgery
| [5335] Samba Server up to 3.6.4 Remote Procedural Calls unknown vulnerability
| [5285] Samba up to 3.6.x ReportEventW memory corruption
| [5284] Samba up to 3.6.x ndr_ValidatePassword memory corruption
| [5283] Samba up to 3.6.x lsa_LookupNames memory corruption
| [5282] Samba up to 3.6.x SetInfoPolicy AuditEventsInfo memory corruption
| [5281] Samba up to 3.6.x GetAliasMembership memory corruption
| [5280] Samba up to 3.6.x NDR PULL DFS EnumArray1 memory corruption
| [5279] Samba up to 3.6.x NDR PULL SVCCTL StartServiceW memory corruption
| [5278] Samba up to 3.6.x NDR PULL LSA TrustDomainInfoControllers memory corruption
| [5277] Samba up to 3.6.x ndr_pull_dfs_Info3 memory corruption
| [58136] Samba up to 3.2.12 Web Administration Tool chg_passwd cross site scripting
| [58135] Samba up to 3.2.12 Web Administration Tool cross site request forgery
| [56965] Samba rsync up to 3.0.7 memory corruption
| [56653] Samba up to 3.2.12 File Descriptors Stack-Based memory corruption
| [4178] Samba up to 3.5.4 SID Parser sid_parse memory corruption
| [53698] Samba up to 3.2.12 sesssetup.c reply_sesssetup_and_X_spnego denial of service
| [53697] Samba up to 3.2.12 process.c chain_reply denial of service
| [53701] Samba up to 3.2.12 process.c chain_reply memory corruption
| [52112] Samba up to 3.5.0 Default Configuration Symlink directory traversal
| [52109] Samba 3.3.11/3.4.6/3.5.0 File Permission privilege escalation
| [50373] Samba up to 3.0.24 Infinite Loop denial of service
| [50022] Samba up to 3.0.25 User Account information disclosure
| [48739] Samba up to 3.0.24 Access Control List acl_group_override denial of service
| [48738] Samba up to 3.2.12 memory corruption
| [45775] Samba up to 3.2.6 Filesystem unknown vulnerability
| [45239] Samba up to 3.2.4 denial of service
| [9982] Samba up to 3.2.5 Failed Login weak authentication
| [42567] Samba 3.0.28a/3.0.29 receive_smb_raw memory corruption
| 
| MITRE CVE - https://cve.mitre.org:
| [CVE-2013-4124] Integer overflow in the read_nttrans_ea_list function in nttrans.c in smbd in Samba 3.x before 3.5.22, 3.6.x before 3.6.17, and 4.x before 4.0.8 allows remote attackers to cause a denial of service (memory consumption) via a malformed packet.
| [CVE-2011-0719] Samba 3.x before 3.3.15, 3.4.x before 3.4.12, and 3.5.x before 3.5.7 does not perform range checks for file descriptors before use of the FD_SET macro, which allows remote attackers to cause a denial of service (stack memory corruption, and infinite loop or daemon crash) by opening a large number of files, related to (1) Winbind or (2) smbd.
| [CVE-2013-0214] Cross-site request forgery (CSRF) vulnerability in the Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.21, 3.6.x before 3.6.12, and 4.x before 4.0.2 allows remote attackers to hijack the authentication of arbitrary users by leveraging knowledge of a password and composing requests that perform SWAT actions.
| [CVE-2013-0213] The Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.21, 3.6.x before 3.6.12, and 4.x before 4.0.2 allows remote attackers to conduct clickjacking attacks via a (1) FRAME or (2) IFRAME element.
| [CVE-2012-1182] The RPC code generator in Samba 3.x before 3.4.16, 3.5.x before 3.5.14, and 3.6.x before 3.6.4 does not implement validation of an array length in a manner consistent with validation of array memory allocation, which allows remote attackers to execute arbitrary code via a crafted RPC call.
| [CVE-2011-2694] Cross-site scripting (XSS) vulnerability in the chg_passwd function in web/swat.c in the Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.10 allows remote authenticated administrators to inject arbitrary web script or HTML via the username parameter to the passwd program (aka the user field to the Change Password page).
| [CVE-2011-2522] Multiple cross-site request forgery (CSRF) vulnerabilities in the Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.10 allow remote attackers to hijack the authentication of administrators for requests that (1) shut down daemons, (2) start daemons, (3) add shares, (4) remove shares, (5) add printers, (6) remove printers, (7) add user accounts, or (8) remove user accounts, as demonstrated by certain start, stop, and restart parameters to the status program.
| [CVE-2004-0186] smbmnt in Samba 2.x and 3.x on Linux 2.6, when installed setuid, allows local users to gain root privileges by mounting a Samba share that contains a setuid root program, whose setuid attributes are not cleared when the share is mounted.
| 
| SecurityFocus - https://www.securityfocus.com/bid/:
| [36250] Samba 3.x Multiple Unspecified Remote Vulnerabilities
| 
| IBM X-Force - https://exchange.xforce.ibmcloud.com:
| [46975] Samba smbd information disclosure
| [37092] RHSA update for Samba smbd share connection request denial of service not installed
| [32301] Samba smbd file rename denial of service
| [27648] Samba smbd share connection request denial of service
| [17325] Samba ASN.1 smbd denial of service
| [86185] Samba read_nttrans_ea_list denial of service
| [82955] Samba Active Directory Domain Controller unauthorized access
| [81694] Samba SWAT clickjacking
| [81693] Samba Samba Web Administration Tool cross-site request forgery
| [81326] Samba objectClass based LDAP security bypass
| [78811] Samba unspecified code execution
| [75277] Samba LSA security bypass
| [74721] Samba RPC code execution
| [74438] Samba mount.cifs information disclosure
| [73361] BlackBerry PlayBook Samba code execution
| [72775] Samba connection request denial of service
| [70317] Samba mtab denial of service
| [69662] Samba check_mtab denial of service
| [68844] Samba user cross-site scripting
| [68843] Samba SWAT cross-site request forgery
| [66702] Samba smbfs security bypass
| [65724] Samba FD_SET denial of service
| [61773] Samba sid_parse() buffer overflow
| [59481] Samba SMB1 packet code execution
| [58565] Samba Negotiate Protocol Request denial of service
| [58564] Samba Session Setup AndX denial of service
| [58393] Samba mount.cifs symlink
| [56758] Samba CAP_DAC_OVERRIDE flag security bypass
| [56123] Samba mount.cifs.c denial of service
| [56111] Samba symlink directory traversal
| [55944] samba-client mount.cifs utility symlink
| [53575] Samba SMB denial of service
| [53574] Samba mount.cifs information disclosure
| [51328] Samba smbclient format string
| [51327] Samba ACL security bypass
| [50439] Samba winbind daemon denial of service
| [47733] Samba file system security bypass
| [45251] Xerox ESS/Network Controller Samba code execution
| [44678] Samba group_mapping.tdb security bypass
| [42664] Samba receive_smb_raw() buffer overflow
| [38965] Samba send_mailslot function buffer overflow
| [38502] Samba reply_netbios_packet() buffer overflow
| [38501] Samba nmbd buffer overflow
| [38123] GoSamba include_path file include
| [36893] SmbFTPD SMBDirList format string
| [36560] Samba smb.conf privilege escalation
| [35738] Apple Mac OS X Samba file system security bypass
| [35401] GSAMBAD populate_conns function symlink
| [34506] Samba version detected
| [34316] Samba lsa_io_trans_names buffer overflow
| [34315] Samba SID name translation privilege escalation
| [34314] Samba sec_io_acl buffer overflow
| [34312] Samba smb_io_notify_option_type_data buffer overflow
| [34311] Samba netdfs_io_dfs_EnumInfo_d buffer overflow
| [34309] Samba lsa_io_privilege_set buffer overflow
| [34307] Samba smb.conf shell command execution
| [32979] Apple Mac OS X Samba module (SMB File Server) buffer overflow
| [32304] Samba afsacl.so VFS plugin format string
| [32231] Samba nss_winbind.so.1 library gethostbyname and getipnodebyname buffer overflow
| [32151] Samba multiple unspecified buffer overflows
| [30920] Sambar FTP Server SIZE denial of service
| [29169] HP-UX CIFS Samba privilege escalation
| [25575] Samba clear text machine trust account credentials
| [22943] Sambar Server proxy.asp allows cross-site scripting
| [20710] Sambar Server search/results.stm and session/logout scripts cross-site scripting
| [18519] Samba MS-RPC request heap corruption
| [18070] Samba QFILEPATHINFO buffer overflow
| [17987] Samba ms_fnmatch denial of service
| [17556] Samba allows file access outside of the share`s defined path
| [17454] Samba samba-vscan denial of service
| [17326] Samba nmbd mailslot denial of service
| [17139] Samba memory leak information disclosure
| [17138] Samba FindNextPrintChangeNotify request denial of service
| [16786] Samba mangling method buffer overflow
| [16785] Samba SWAT invalid base64 character causes buffer overflow
| [16287] Sambar showlog.asp and showini.asp scripts directory traversal
| [16286] Sambar show.asp and showperf.asp scripts cross-site scripting
| [16059] Sambar Server HTTP POST code execution
| [16056] Sambar Server multiple script cross-site scripting
| [16054] Sambar Server HTTP keep-alive allows unauthorized access
| [15545] Samba smbprint.log symlink attack
| [15132] Samba mksmbpasswd.sh could allow an attacker to gain access to user`s account
| [15131] Samba smbmnt allows elevated privileges
| [15071] Sambar Server HTTP POST request buffer overflow
| [13305] Sambar Server multiple vulnerabilities
| [12749] Samba reply_nttrans function buffer overflow
| [12402] Sambar Server search.pl denial of service
| [11845] Sambar Server Pro Server WebMail interface transmits password and username in plain text
| [11726] Samba and Samba-TNG call_trans2open() function buffer overflow
| [11634] Sambar Server remote file cross-site scripting
| [11633] Sambar Server dot dot directory traversal
| [11631] Sambar Server multiple scripts cross-site scripting
| [11630] Sambar Server textcgi.exe and environ.pl path disclosure
| [11616] Samba-TNG security context management code could allow root access
| [11551] Samba .reg file code race condition
| [11550] Samba SMB/CIFS packet fragment re-assembly code buffer overflow
| [11128] Sambar Server search request cross-site scripting
| [10683] Samba encrypted password change request buffer overflow
| [10010] Samba enum_csc_policy memory structure buffer overflow
| [8876] Sambar Server Perl script source disclosure
| [8710] Sambar Server Pbcgi.exe denial of service
| [8709] Sambar Server testcgi.exe denial of service
| [8707] Sambar Server long HTTP header field denial of service
| [8705] Sambar Server MSVCRT.dll long username and password buffer overflow
| [7894] Sambar Server cgitest.exe example script denial of service
| [6973] Sambar Server Telnet proxy long password buffer overflow
| [6972] Sambar Server Telnet proxy continuous connections denial of service
| [6916] Sambar Server &quot
| [6909] Sambar Server insecure password protection
| [6731] samba NetBIOS name allows remote attackers to create symlink to SMB log file
| [6396] Samba tmpfile symlink attack could allow elevated privileges
| [5445] Samba swat logfile information retrieval
| [5444] Samba swat URL filename denial of service
| [5443] Samba swat logging symbolic link
| [5442] Samba swat brute force attack
| [5247] Sambar search.dll allows attacker to view folders on the system
| [4592] Sambar Server 4.3 buffer overflow
| [3999] Sambar Server hello.bat and echo.bat CGI scripts
| [3227] Samba smbmnt utility could allow mounting to arbitrary mount points
| [3225] Samba message service potential buffer overflow
| [3224] Samba nmbd daemon can be remotely crashed or caused to enter an infinite loop
| [3223] Sambar server allows remote viewing of environment information
| [1672] Sambar Server logging code buffer overflow
| [1671] Sambar mailit client allows script execution
| [1669] Sambar Server ships with default accounts
| [1406] Samba wsmbconf binary allows users access to the group root
| [1311] Samba open share
| [1237] Samba .. Bug
| [337] Samba SMB password buffer overflow
| [9] Samba .. bug
| 
| Exploit-DB - https://www.exploit-db.com:
| [20223] Sambar Server 4.3/4.4 beta 3 Search CGI Vulnerability
| [10095] Samba 3.0.10 - 3.3.5 Format String And Security Bypass Vulnerabilities
| [9950] Samba 3.0.21-3.0.24 LSA trans names Heap Overflow
| [7701] Samba < 3.0.20 - Remote Heap Overflow Exploit
| [4732] Samba 3.0.27a send_mailslot() Remote Buffer Overflow PoC
| [364] Samba <= 3.0.4 SWAT Authorization Buffer Overflow Exploit
| 
| OpenVAS (Nessus) - http://www.openvas.org:
| [90028] Samba 3.0.0 > 3.0.29 vulnerability
| 
| SecurityTracker - https://www.securitytracker.com:
| [1028882] Samba smbd CPU Processing Loop Lets Remote Users Deny Service
| [1026595] Samba smbd Memory Leak Lets Remote Users Deny Service
| [1022976] Samba smbd Processing Flaw Lets Remote Authenticated Users Deny Service
| [1022442] Samba smbd Access Control Bug Lets Remote Authenticated Users Bypass Certain Access Controls
| [1017587] Samba smbd Deferred File Open Processing Bug Lets Remote Users Deny Service
| [1016459] Samba smbd Memory Limit Error in make_connection() Lets Remote Users Deny Service
| [1012587] Samba smbd Integer Overflow in Allocating Security Descriptors May Let Remote Users Execute Arbitrary Code
| [1011223] Samba smbd Infinite Loop Lets Remote Users Consume All Available Memory
| [1011097] Samba FindNextPrintChangeNotify() Error Lets Remote Authenticated Users Crash smbd
| [1006290] Samba 'smbd' Buffer Overflow May Let Remote Users Gain Root Access
| [1028389] Samba Bug Lets Remote Authenticated Users Modify Files
| [1028365] IBM Storwize V7000 Unified Samba Bug Lets Remote Authenticated Users Modify Files
| [1028312] Samba Active Directory Domain Controller File Permission Flaw Lets Remote Authenticated Users Access Files
| [1028006] Samba Active Directory Domain Controller Access Control Flaw Lets Remote Authenticated Gain Write Access to Certain Objects
| [1026988] Samba Local Security Authority Bug Lets Remote Authenticated Users Gain Elevated Privileges
| [1026913] Samba Buffer Overflow in NDR Marshalling Code Lets Remote Users Execute Arbitrary Code
| [1026739] Samba Bug in chain_reply()/construct_reply() Lets Remote Users Execute Arbitrary Code
| [1026727] Blackberry PlayBook Samba File Sharing Lets Remote Users Execute Arbitrary Code
| [1025984] Samba 'mount.cifs' check_newline() Error Lets Local Users Deny Service
| [1025852] Samba Web Administration Tool (SWAT) Input Validation Flaws Permit Cross-Site Request Forgery and Cross-Site Scripting Attacks
| [1025132] Samba FD_SET Stack Corruption Flaw Lets Remote and Local Users Deny Service
| [1024434] Samba Buffer Overflow in sid_parse() Lets Remote Users Execute Arbitrary Code
| [1024107] Samba SMB1 Packet Chaining Memory Corruption Error Lets Remote Users Execute Arbitrary Code
| [1023700] Samba Access Control Flaw Lets Remote Authenticated Users Gain Elevated Privileges
| [1023547] Samba 'mount.cifs' Race Condition Lets Local Users Gain Elevated Privileges
| [1023546] Samba Symlink Configuration Error Lets Remote Users Access Arbitrary Files
| [1022975] Samba 'mount.cifs' Lets Local Users View Portions of Files on the Target System
| [1022441] Samba smbclient Format String Bug May Let Users Execute Arbitrary Code
| [1021513] Samba Grants Remote Authenticated Users Access to the Root Filesystem in Certain Cases
| [1021287] Samba 'trans', 'trans2', and 'nttrans' Requests Let Remote Users Obtain Memory Contents
| [1020770] Samba 'group_mapping.ldb' Has Unsafe Permissions That Let Local Users Gain Elevated Privileges
| [1020123] Samba Buffer Overflow in receive_smb_raw() Lets Remote Users Execute Arbitrary Code
| [1019065] Samba Buffer Overflow in nmbd send_mailslot() Lets Remote Users Execute Arbitrary Code
| [1018954] Samba nmbd Buffer Overflow in Processing GETDC mailslot Requests Lets Remote Users Execute Arbitrary Code
| [1018953] Samba nmbd Buffer Overflow in reply_netbios_packet() Lets Remote Users Execute Arbitrary Code
| [1018681] Samba Winbind SFU/RFC2307 GID Error Lets Local Users Gain Elevated Privileges
| [1018051] Samba 'smb.conf' Scripts Input Validation Flaw Lets Remote Users Inject Arbitrary Commands
| [1018050] Samba Heap Overflows in Parsing NDR Data Let Remote Users Execute Arbitrary Code
| [1018049] Samba SID/Name Translation Bug Lets Local Users Gain Root Privileges
| [1017589] Samba Solaris winbindd Daemon Name Resolution Query Buffer Overflows May Let Remtoe Users Execute Arbitrary Code
| [1017588] Samba Format String Bug in 'afsacl.so' VFS Plugin May Let Remote Users Execute Arbitrary Code
| [1017393] Sambar Server FTP SIZE Command Lets Remote Authenticated Users Deny Service
| [1015850] Samba winbindd Daemon Discloses Server Password to Local Users
| [1012235] Samba QFILEPATHINFO Buffer Overflow Lets Remote Authenticated Users Execute Arbitrary Code
| [1012133] Samba Input Validation Error in ms_fnmatch() Lets Remote Authenticated Users Deny Service
| [1011949] Samba pppd Callback Control Protocol Pointer Dereference May Let Remote Users Deny Service
| [1011469] Samba DOS Path Conversion Flaw Discloses Files to Remote Users
| [1011222] Samba Input Validation Error in nmbd process_logon_packet() Lets Remote Users Crash the nmbd Service
| [1010753] Samba Buffer Overflows in Web Administration Tool and in 'hash' Mangling Method May Let Remote Users Execute Arbitrary Code
| [1010353] Sambar Server 'showini.asp' and 'showlog.asp' Disclose Files to Remote Authenticated Administrators
| [1009503] Samba 'smbprint' Unsafe Temporary File May Let Local Users Gain Elevated Privileges
| [1009000] Samba 'smbmnt' Permissions May Let Local Users Gain Root Privileges
| [1008990] Samba May Let Remote Users Access SMB Accounts That Have Invalid Passwords
| [1008979] Sambar Server 'results.stm' POST Request Buffer Overflow  May Permit Remote Code Execution
| [1007819] Sambar Server Contains Multiple Unspecified Vulnerabilities
| [1007016] Sambar Server Buffer Overflow in 'search.pl' Lets Remote Users Crash the Service
| [1006934] Sambar Server Discloses Files on the System to Remote Users
| [1006637] Sambar Server WebMail Discloses User Passwords Transmitted Via the Network
| [1006498] Samba-TNG Buffer Overflow in call_trans2open() Function Lets Remote Users Execute Arbitrary Code With Root Privileges
| [1006497] Samba Buffer Overflow in call_trans2open() Function Lets Remote Users Execute Arbitrary Code With Root Privileges
| [1006390] Sambar Server Input Validation Flaws Disclose Files on the System to Remote Users and Permit Cross-Site Scripting Attacks
| [1005946] Sambar Server Input Validation Hole in Query Feature Lets Remote Users Conduct Cross-Site Scripting Attacks
| [1005677] Samba Buffer Overflow in User Input Routine May Let Remote Users Execute Arbitrary Code with Root Privileges
| [1004624] HP-UX Samba Common Internet File System (CIFS) Client Buffer Overflow May Let Local Users Obtain Elevated Privileges on the System
| [1004084] Sambar Server Discloses Script Source Code to Remote Users and Can Be Crashed By Remote Users via Malformed URLs
| [1003941] Sambar Server Buffer Overflow Holes Let Remote Users Crash the Service or Execute Arbitrary Code on the System
| [1003246] Sambar Web Server Sample CGI Allows Remote Users to Crash the Web Server
| [1002302] HP CIFS/9000 (Samba) Server Lets Authenticated Remote Users Change Another User's Password
| [1002187] Sambar Telnet Proxy/Server Password Buffer Overflow May Allow Remote Users to Execute Arbitrary Code on the Server
| [1002082] Sambar Web Server Lets Remote Users Modify Files on the Server
| [1002079] Sambar Server Password File Can Be Decrypted By Local Users
| [1002038] Sambar Server's Web Server Lets Local Users Disclose Files Outside of the Documents Directory
| [1002037] Sambar Server's SMTP Mail Server May Allow Remote Users to Relay Mail Through the Server
| [1001826] Samba Common Internet File System (CIFS) Lets Remote Users Obtain Root Level Access
| [1001339] Samba SMB Networking Software Allows Local Users to Destroy Data on Local Devices
| 
| OSVDB - http://www.osvdb.org:
| [95969] Samba smbd nttrans.c read_nttrans_ea_list Function Malformed Packet Handling Remote DoS
| [78651] Samba smbd Connection Request Parsing Remote DoS
| [65518] Samba smbd process.c chain_reply Function SMB1 Packet Chaining Memory Corruption
| [65436] Samba smbd sesssetup.c Session Setup AndX Security Blob Length Value Uninitialized Variable Out-of-bounds DoS
| [65435] Samba smbd process.c chain_reply Function Session Setup AndX Request NULL Dereference Remote DoS
| [58519] Samba smbd Crafted SMB Request Remote CPU Consumption DoS
| [57651] Samba smbd Unspecified Heap Overflow
| [55411] Samba smbd/posix_acls.c acl_group_override Function Remote Access Control List Modification
| [50230] Samba smbd *trans* Request Arbitrary Remote Memory Disclosure
| [33100] Samba smbd Deferred Open Code Infinite Loop DoS
| [12422] Samba smbd Security Descriptor Parsing Remote Overflow
| [9362] Samba smbd FindNextPrintChangeNotify() Request Remote DoS
| [6323] Samba smbd SMB/CIFS Packet Fragment Reassembly Remote Overflow
| [93189] HP MPE/iX with Samba/iX Unspecified Remote Issue
| [92247] Red Hat Storage Management Console GlusterFS extras/hook-scripts/S30samba-stop.sh Symlink Arbitrary File Overwrite
| [91889] Samba SMB2 Implementation CIFS Share Attribute Enforcement Weakness
| [91503] Samba Active Directory Domain Controller CIFS Shares World-writeable Files Creation Weakness
| [91255] ASUS RT-N66U Router root$ Samba Share Export Remote Information Disclosure
| [89627] Samba Web Administration Tool (SWAT) Manipulation CSRF
| [89626] Samba Web Administration Tool (SWAT) Clickjacking Weakness
| [89180] Samba AD DC LDAP Directory Objects Erroneous Write Access Permissions
| [83446] Samba smbmount Multiple Variable Username Handling Local Overflow
| [81648] Samba Multiple Remote Procedural Calls (RPC) Local Security Authority (LSA) Arbitrary File Manipulation
| [81490] Samba mount.cifs chdir() Call File Enumeration
| [81303] Samba RPC Code Generator Network Data Representation (NDR) Multiple Request Parsing Remote Overflow
| [79443] Samba process.c Any Batched (AndX) Request Packet Parsing Remote Overflow
| [79041] Webmin Samba Windows File Sharing Module /tmp/.webmin Local Password Disclosure
| [76058] Samba mtab Lock File Handling Local DoS
| [74872] Samba smbfs mount.cifs / umount.cifs RLIMIT_FSIZE Value Handling mtab Local Corruption DoS
| [74871] Samba mount.cifs Tool Share / Directory Name Newline Injection mtab Corruption Local DoS
| [74072] Samba Web Administration Tool (SWAT) Change Password Page user Field XSS
| [74071] Samba Web Administration Tool (SWAT) Multiple Function CSRF
| [71268] Samba FD_SET Macro Memory Corruption
| [69288] VLC Media Player Samba Network Share Module Incorrect Calling Convention Stack Corruption
| [67994] Samba sid_parse() Function SID Parsing Remote Overflow
| [62803] Samba CAP_DAC_OVERRIDE Capability Flag File Permission Restriction Bypass
| [62187] Samba sid_parse Stack Overflow
| [62186] Samba mount.cifs Symlink Arbitrary File Access
| [62155] Samba smbfs mount.cifs client/mount.cifs.c Crafted String mtab Corruption Local DoS
| [62145] Samba Guest Account Symlink Traversal Arbitrary File Access
| [60587] Windows File Sharing Samba Client Resource Exhaustion DoS
| [59810] Samba reply_nttrans Function Remote Overflow
| [59511] HP-UX CIFS/9000 Server (SAMBA) Unspecified Resource Modification Arbitrary File Overwrite
| [59350] Samba Web Administration Tool (SWAT) Malformed HTTP Request Saturation Remote DoS
| [58520] Samba SUID mount.cifs --verbose Argument Arbitrary File Portion Disclosure
| [57955] Samba Unconfigured Home Directory Windows File Share Directory Access Restriction Bypass
| [57653] Samba Unspecified Heap Overflow
| [57652] Samba --enable-developer Functionality Unspecified Heap Overflow
| [57172] Samba-TNG Unspecified Remote Privilege Escalation
| [55412] Samba smbclient client/client.c Filename Specifiers Multiple Format Strings
| [55370] Sambar Server Pbcgi.exe Remote Overflow
| [55369] Sambar Server testcgi.exe Remote Overflow
| [54378] Samba winbind Daemon Unresponsive Child Process Race Condition DoS
| [53074] Sambar Server /session/sendmail Arbitrary Mail Relay
| [51152] Samba Crafted Connection Request Remote Root File System Access
| [48699] CUPS cupsaddsmb Temporary File Cleartext Samba Credential Disclosure
| [47786] Samba group_mapping.tdb Permission Weakness Privilege Escalation
| [45657] Samba lib/util_sock.c receive_smb_raw() Function Crafted Packet Handling Overflow
| [42884] Sambar Server with IndigoPerl /cgi-bin/com1.pl Arbitrary Command Execution
| [42305] Samba Unspecified Remote Issue
| [42251] Sambar Server Unspecified Remote Command Execution
| [41385] SmbFTPD SMBDirList() Function Directory Name Remote Format String
| [40714] GoSamba main.php include_path Parameter Remote File Inclusion
| [40713] GoSamba inc_user.php include_path Parameter Remote File Inclusion
| [40712] GoSamba inc_smb_conf.php include_path Parameter Remote File Inclusion
| [40711] GoSamba inc_newgroup.php include_path Parameter Remote File Inclusion
| [40710] GoSamba inc_manager.php include_path Parameter Remote File Inclusion
| [40709] GoSamba inc_group.php include_path Parameter Remote File Inclusion
| [40708] GoSamba inc_freigabe3.php include_path Parameter Remote File Inclusion
| [40707] GoSamba inc_freigabe1.php include_path Parameter Remote File Inclusion
| [40706] GoSamba inc_freigabe.php include_path Parameter Remote File Inclusion
| [40705] GoSamba HTML_oben.php include_path Parameter Remote File Inclusion
| [39191] Samba nmdb send_mailslot() Function GETDC mailslot Request Remote Overflow
| [39180] Samba nmbd Crafted GETDC mailslot Request Remote Overflow
| [39179] Samba nmbd nmbd/nmbd_packets.c reply_netbios_packet Function Remote Overflow
| [39178] Samba idmap_ad.so Winbind nss_info Extension (nsswitch/idmap_ad.c) Local Privilege Escalation
| [37795] GSAMBAD /tmp/gsambadtmp Symlink Arbitrary File Overwrite
| [36971] Apple Mac OS X Samba Server Disk Quota Bypass
| [34852] Apple Mac OS X Apple-specific Samba Module (SMB File Server) ACL Handling Overflow
| [34733] Samba DFS RPC Interface DFSEnum Request Remote Overflow
| [34732] Samba SPOOLSS RPC Interface RFNPCNEX Request Remote Overflow
| [34731] Samba SRVSVC RPC Interface NetSetFileSecurity Request Remote Overflow
| [34700] Samba Unfiltered MS-RPC Calls Arbitrary Remote Command Execution
| [34699] Samba LSA RPC Interface Multiple Function Remote Overflow
| [34698] Samba SID/Name Translation Privileged SMB/CIFS Protocol Operation Execution
| [33101] Samba VFS Plugin afsacl.so Format String
| [33098] Samba nss_winbind.so.1 Multiple Function Overflow
| [32336] Sambar FTP Server Malformed SIZE Command DoS
| [27130] Samba smdb Share Connection Saturation DoS
| [24263] Samba winbindd Debug Log Server Credentials Local Disclosure
| [23282] Samba Unspecified Remote Memory Leak Information Disclosure
| [20434] Sambar Server proxy.asp Multiple Field XSS
| [16751] Sambar Server Referer XSS
| [16750] Sambar Server logout RCredirect XSS
| [16749] Sambar Server results.stm indexname XSS
| [14525] Samba Encrypted Password String Conversion Decryption Overflow DoS
| [14233] Sambar Telnet Proxy/Server Long Password Overflow
| [13872] Samba smbclient mput Symlink Arbitrary File Overwrite
| [13871] Samba smbclient more Symlink Arbitrary File Overwrite
| [13870] Samba Printer Queue Query Symlink Arbitrary File Overwrite
| [13397] Samba Multiple Unspecified Overflows
| [12642] Samba .reg File Race Condition Arbitrary File Overwrite
| [11794] Sambar Server whois Script Hostname Remote Overflow
| [11793] Sambar Server finger Script Hostname Remote Overflow
| [11782] Samba QFILEPATHINFO Unicode Filename Request Handler Overflow
| [11555] Samba ms_fnmatch() Function Wildcard Matching Remote DoS
| [11521] Samba Password Field Handling Remote Overflow
| [11479] Microsoft Windows NT Double Dot Samba Client DoS
| [10886] Sambar Web Server Long HTTP GET Request Overflow
| [10464] Samba MS-DOS Path Request Arbitrary File Retrieval
| [9917] Samba nmbd process_logon_packet Function Remote DoS
| [9916] Samba ASN.1 Parsing Function Malformed Request DoS
| [8860] Samba NETBIOS Name Service Daemon DoS
| [8859] Samba smbmnt Race Condition Arbitrary Mount Point
| [8191] Samba Mangling Method Hash Overflow
| [8190] Samba Web Administration Tool (SWAT) HTTP Basic Auth base64 Decoding Remote Overflow
| [7529] Samba wsmbconf Command Execution and Privilege Escalation
| [6585] Sambar Server showini.asp Arbitrary File Access
| [6584] Sambar Server showperf.asp title Parameter XSS
| [6583] Sambar Server show.asp show Parameter XSS
| [5820] Sambar Server vchist.stm Multiple Parameter XSS
| [5819] Sambar Server vccreate.stm Multiple Parameter XSS
| [5818] Sambar Server vccheckin.stm Multiple Parameter XSS
| [5817] Sambar Server update.stm Multiple Parameter XSS
| [5816] Sambar Server template.stm path Parameter XSS
| [5815] Sambar Server sendmail.stm Multiple Parameter XSS
| [5814] Sambar Server rename.stm Multiple Parameter XSS
| [5813] Sambar Server mkdir.stm path Parameter XSS
| [5812] Sambar Server htaccess.stm path Parameter XSS
| [5811] Sambar Server ftp.stm path Parameter XSS
| [5810] Sambar Server info.stm Multiple Parameter XSS
| [5809] Sambar Server create.stm path Parameter XSS
| [5808] Sambar Server iecreate.stm path Parameter XSS
| [5807] Sambar Server edit.stm Multiple Parameter XSS
| [5806] Sambar Server ieedit.stm Multiple Parameter XSS
| [5805] Sambar Server search.dll query Parameter XSS
| [5804] Sambar Server environ.pl param1 Parameter XSS
| [5803] Sambar Server testisa.dll check1 Parameter XSS
| [5802] Sambar Server echo.bat Code Execution
| [5786] Sambar Server results.stm Overflow
| [5785] Sambar Server book.pl E-mail Field XSS
| [5784] Sambar Server dumpenv.pl XSS
| [5783] Sambar Server ssienv.shtml XSS
| [5782] Sambar Server mortgage.pl price Parameter XSS
| [5781] Sambar Server DOS Device Name Code Execution
| [5780] Sambar Server Proxy IP Filter Bypass
| [5468] Sambar Server Password Encryption Scheme Weakness
| [5123] Sambar DOS Device Name DoS
| [5122] Sambar Server Null Terminated URL Arbitrary File Source Disclosure
| [5108] Sambar Server search.stm Multiple Parameter XSS
| [5107] Sambar Server findata.stm Multiple Parameter XSS
| [5106] Sambar Server whodata.stm sitename Parameter XSS
| [5105] Sambar Server showfnc.stm pkg Parameter XSS
| [5104] Sambar Server showfncs.stm pkg Parameter XSS
| [5103] Sambar Server showfunc.stm func Parameter XSS
| [5102] Sambar Server stmex.stm XSS
| [5101] Sambar Server ipdata.stm ipaddr Parameter XSS
| [5100] Sambar Server testcgi.exe XSS
| [5097] Sambar Server index.stm wwwsite Parameter XSS
| [5096] Sambar Server iecreate.stm Directory Listing
| [5095] Sambar Server ieedit.stm Directory Listing
| [5094] Sambar Server testcgi.exe Environment Variable Disclosure
| [5093] Sambar Server environ.pl Environment Variable Disclosure
| [4469] Samba trans2.c call_trans2open() Function Overflow
| [3919] Samba mksmbpasswd.sh Uninitialized Passwords
| [3916] Samba smbmnt Local Privilege Escalation
| [2204] Sambar Server search.pl results.stm Overflow DoS
| [1626] Samba Web Administration Tool (SWAT) cgi.log Permission Weakness Information Disclosure
| [1625] Samba Web Administration Tool (SWAT) Failed Login Logging Failure Weakness
| [1025] Samba smdb Malformed Message Handling Remote Overflow
| [861] Samba enum_csc_policy Data Structure Termination Remote Overflow
| [656] Samba NETBIOS Name Traversal Arbitrary Remote File Creation
| [589] Sambar Web Server pagecount CGI Traversal Arbitrary File Overwrite
| [487] Samba Web Administration Tool (SWAT) Error Message Username Enumeration
| [413] Sambar Server ISAPI Search Utility search.dll Query Parameter Parsing Folder Name Disclosure
| [319] Sambar Server mailit.pl Arbitrary Mail Relay
| [318] Sambar Server Sysadmin Web Interface Default Account
| [317] Sambar sendmail CGI Arbitrary Mail Relay
| [215] Samba Web Administration Tool (SWAT) cgi.log Symlink Arbitrary File Modification
| [194] Sambar Server hello.bat Code Execution
| [52] Sambar Server dumpenv.pl Information Disclosure
| [34] Sambar Server cgitest.exe Crafted GET Request Parsing Remote Overflow
|_
445/tcp open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
| vulscan: VulDB - https://vuldb.com:
| [69204] Samba 3.6.24/4.0.24/4.1.16/4.2.0 smbd _netr_ServerPasswordSet privilege escalation
| [4585] Samba smbd up to 3.6.3 Connection Request Parser denial of service
| [82409] Samba 3.0/4.2.9/4.3.6/4.4.0 IPC Traffic privilege escalation
| [82406] Samba 3.6/4.2.9/4.3.6/4.4.0 LDAP Client privilege escalation
| [82405] Samba 3.6/4.2.9/4.3.6/4.4.0 Netlogon Service spoofing
| [82404] Samba 3.6/4.2.9/4.3.6/4.4.0 NTLMSSP privilege escalation
| [82403] Samba 3.6/4.2.9/4.3.6/4.4.0 DCE-RPC CPU Exhaustion denial of service
| [13388] Samba up to 3.6.23/4.0.17/4.1.7 vfs Shadow Copy information disclosure
| [65614] Samba up to 3.0.2a Access Restriction winbind_name_list_to_sid_string_list unknown vulnerability
| [9859] Samba up to 3.5.21 Packet nttrans.c read_nttrans_ea_list denial of service
| [7995] Asus RT-N66U Router 3.0.0.4.270 Samba Root Share Eingabe unknown vulnerability
| [8152] Samba up to 3.6.5 SMB2 Implementation privilege escalation
| [63488] Samba up to 3.5.18 Web Administration Tool cross site request forgery
| [5335] Samba Server up to 3.6.4 Remote Procedural Calls unknown vulnerability
| [5285] Samba up to 3.6.x ReportEventW memory corruption
| [5284] Samba up to 3.6.x ndr_ValidatePassword memory corruption
| [5283] Samba up to 3.6.x lsa_LookupNames memory corruption
| [5282] Samba up to 3.6.x SetInfoPolicy AuditEventsInfo memory corruption
| [5281] Samba up to 3.6.x GetAliasMembership memory corruption
| [5280] Samba up to 3.6.x NDR PULL DFS EnumArray1 memory corruption
| [5279] Samba up to 3.6.x NDR PULL SVCCTL StartServiceW memory corruption
| [5278] Samba up to 3.6.x NDR PULL LSA TrustDomainInfoControllers memory corruption
| [5277] Samba up to 3.6.x ndr_pull_dfs_Info3 memory corruption
| [58136] Samba up to 3.2.12 Web Administration Tool chg_passwd cross site scripting
| [58135] Samba up to 3.2.12 Web Administration Tool cross site request forgery
| [56965] Samba rsync up to 3.0.7 memory corruption
| [56653] Samba up to 3.2.12 File Descriptors Stack-Based memory corruption
| [4178] Samba up to 3.5.4 SID Parser sid_parse memory corruption
| [53698] Samba up to 3.2.12 sesssetup.c reply_sesssetup_and_X_spnego denial of service
| [53697] Samba up to 3.2.12 process.c chain_reply denial of service
| [53701] Samba up to 3.2.12 process.c chain_reply memory corruption
| [52112] Samba up to 3.5.0 Default Configuration Symlink directory traversal
| [52109] Samba 3.3.11/3.4.6/3.5.0 File Permission privilege escalation
| [50373] Samba up to 3.0.24 Infinite Loop denial of service
| [50022] Samba up to 3.0.25 User Account information disclosure
| [48739] Samba up to 3.0.24 Access Control List acl_group_override denial of service
| [48738] Samba up to 3.2.12 memory corruption
| [45775] Samba up to 3.2.6 Filesystem unknown vulnerability
| [45239] Samba up to 3.2.4 denial of service
| [9982] Samba up to 3.2.5 Failed Login weak authentication
| [42567] Samba 3.0.28a/3.0.29 receive_smb_raw memory corruption
| 
| MITRE CVE - https://cve.mitre.org:
| [CVE-2013-4124] Integer overflow in the read_nttrans_ea_list function in nttrans.c in smbd in Samba 3.x before 3.5.22, 3.6.x before 3.6.17, and 4.x before 4.0.8 allows remote attackers to cause a denial of service (memory consumption) via a malformed packet.
| [CVE-2011-0719] Samba 3.x before 3.3.15, 3.4.x before 3.4.12, and 3.5.x before 3.5.7 does not perform range checks for file descriptors before use of the FD_SET macro, which allows remote attackers to cause a denial of service (stack memory corruption, and infinite loop or daemon crash) by opening a large number of files, related to (1) Winbind or (2) smbd.
| [CVE-2013-0214] Cross-site request forgery (CSRF) vulnerability in the Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.21, 3.6.x before 3.6.12, and 4.x before 4.0.2 allows remote attackers to hijack the authentication of arbitrary users by leveraging knowledge of a password and composing requests that perform SWAT actions.
| [CVE-2013-0213] The Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.21, 3.6.x before 3.6.12, and 4.x before 4.0.2 allows remote attackers to conduct clickjacking attacks via a (1) FRAME or (2) IFRAME element.
| [CVE-2012-1182] The RPC code generator in Samba 3.x before 3.4.16, 3.5.x before 3.5.14, and 3.6.x before 3.6.4 does not implement validation of an array length in a manner consistent with validation of array memory allocation, which allows remote attackers to execute arbitrary code via a crafted RPC call.
| [CVE-2011-2694] Cross-site scripting (XSS) vulnerability in the chg_passwd function in web/swat.c in the Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.10 allows remote authenticated administrators to inject arbitrary web script or HTML via the username parameter to the passwd program (aka the user field to the Change Password page).
| [CVE-2011-2522] Multiple cross-site request forgery (CSRF) vulnerabilities in the Samba Web Administration Tool (SWAT) in Samba 3.x before 3.5.10 allow remote attackers to hijack the authentication of administrators for requests that (1) shut down daemons, (2) start daemons, (3) add shares, (4) remove shares, (5) add printers, (6) remove printers, (7) add user accounts, or (8) remove user accounts, as demonstrated by certain start, stop, and restart parameters to the status program.
| [CVE-2004-0186] smbmnt in Samba 2.x and 3.x on Linux 2.6, when installed setuid, allows local users to gain root privileges by mounting a Samba share that contains a setuid root program, whose setuid attributes are not cleared when the share is mounted.
| 
| SecurityFocus - https://www.securityfocus.com/bid/:
| [36250] Samba 3.x Multiple Unspecified Remote Vulnerabilities
| 
| IBM X-Force - https://exchange.xforce.ibmcloud.com:
| [46975] Samba smbd information disclosure
| [37092] RHSA update for Samba smbd share connection request denial of service not installed
| [32301] Samba smbd file rename denial of service
| [27648] Samba smbd share connection request denial of service
| [17325] Samba ASN.1 smbd denial of service
| [86185] Samba read_nttrans_ea_list denial of service
| [82955] Samba Active Directory Domain Controller unauthorized access
| [81694] Samba SWAT clickjacking
| [81693] Samba Samba Web Administration Tool cross-site request forgery
| [81326] Samba objectClass based LDAP security bypass
| [78811] Samba unspecified code execution
| [75277] Samba LSA security bypass
| [74721] Samba RPC code execution
| [74438] Samba mount.cifs information disclosure
| [73361] BlackBerry PlayBook Samba code execution
| [72775] Samba connection request denial of service
| [70317] Samba mtab denial of service
| [69662] Samba check_mtab denial of service
| [68844] Samba user cross-site scripting
| [68843] Samba SWAT cross-site request forgery
| [66702] Samba smbfs security bypass
| [65724] Samba FD_SET denial of service
| [61773] Samba sid_parse() buffer overflow
| [59481] Samba SMB1 packet code execution
| [58565] Samba Negotiate Protocol Request denial of service
| [58564] Samba Session Setup AndX denial of service
| [58393] Samba mount.cifs symlink
| [56758] Samba CAP_DAC_OVERRIDE flag security bypass
| [56123] Samba mount.cifs.c denial of service
| [56111] Samba symlink directory traversal
| [55944] samba-client mount.cifs utility symlink
| [53575] Samba SMB denial of service
| [53574] Samba mount.cifs information disclosure
| [51328] Samba smbclient format string
| [51327] Samba ACL security bypass
| [50439] Samba winbind daemon denial of service
| [47733] Samba file system security bypass
| [45251] Xerox ESS/Network Controller Samba code execution
| [44678] Samba group_mapping.tdb security bypass
| [42664] Samba receive_smb_raw() buffer overflow
| [38965] Samba send_mailslot function buffer overflow
| [38502] Samba reply_netbios_packet() buffer overflow
| [38501] Samba nmbd buffer overflow
| [38123] GoSamba include_path file include
| [36893] SmbFTPD SMBDirList format string
| [36560] Samba smb.conf privilege escalation
| [35738] Apple Mac OS X Samba file system security bypass
| [35401] GSAMBAD populate_conns function symlink
| [34506] Samba version detected
| [34316] Samba lsa_io_trans_names buffer overflow
| [34315] Samba SID name translation privilege escalation
| [34314] Samba sec_io_acl buffer overflow
| [34312] Samba smb_io_notify_option_type_data buffer overflow
| [34311] Samba netdfs_io_dfs_EnumInfo_d buffer overflow
| [34309] Samba lsa_io_privilege_set buffer overflow
| [34307] Samba smb.conf shell command execution
| [32979] Apple Mac OS X Samba module (SMB File Server) buffer overflow
| [32304] Samba afsacl.so VFS plugin format string
| [32231] Samba nss_winbind.so.1 library gethostbyname and getipnodebyname buffer overflow
| [32151] Samba multiple unspecified buffer overflows
| [30920] Sambar FTP Server SIZE denial of service
| [29169] HP-UX CIFS Samba privilege escalation
| [25575] Samba clear text machine trust account credentials
| [22943] Sambar Server proxy.asp allows cross-site scripting
| [20710] Sambar Server search/results.stm and session/logout scripts cross-site scripting
| [18519] Samba MS-RPC request heap corruption
| [18070] Samba QFILEPATHINFO buffer overflow
| [17987] Samba ms_fnmatch denial of service
| [17556] Samba allows file access outside of the share`s defined path
| [17454] Samba samba-vscan denial of service
| [17326] Samba nmbd mailslot denial of service
| [17139] Samba memory leak information disclosure
| [17138] Samba FindNextPrintChangeNotify request denial of service
| [16786] Samba mangling method buffer overflow
| [16785] Samba SWAT invalid base64 character causes buffer overflow
| [16287] Sambar showlog.asp and showini.asp scripts directory traversal
| [16286] Sambar show.asp and showperf.asp scripts cross-site scripting
| [16059] Sambar Server HTTP POST code execution
| [16056] Sambar Server multiple script cross-site scripting
| [16054] Sambar Server HTTP keep-alive allows unauthorized access
| [15545] Samba smbprint.log symlink attack
| [15132] Samba mksmbpasswd.sh could allow an attacker to gain access to user`s account
| [15131] Samba smbmnt allows elevated privileges
| [15071] Sambar Server HTTP POST request buffer overflow
| [13305] Sambar Server multiple vulnerabilities
| [12749] Samba reply_nttrans function buffer overflow
| [12402] Sambar Server search.pl denial of service
| [11845] Sambar Server Pro Server WebMail interface transmits password and username in plain text
| [11726] Samba and Samba-TNG call_trans2open() function buffer overflow
| [11634] Sambar Server remote file cross-site scripting
| [11633] Sambar Server dot dot directory traversal
| [11631] Sambar Server multiple scripts cross-site scripting
| [11630] Sambar Server textcgi.exe and environ.pl path disclosure
| [11616] Samba-TNG security context management code could allow root access
| [11551] Samba .reg file code race condition
| [11550] Samba SMB/CIFS packet fragment re-assembly code buffer overflow
| [11128] Sambar Server search request cross-site scripting
| [10683] Samba encrypted password change request buffer overflow
| [10010] Samba enum_csc_policy memory structure buffer overflow
| [8876] Sambar Server Perl script source disclosure
| [8710] Sambar Server Pbcgi.exe denial of service
| [8709] Sambar Server testcgi.exe denial of service
| [8707] Sambar Server long HTTP header field denial of service
| [8705] Sambar Server MSVCRT.dll long username and password buffer overflow
| [7894] Sambar Server cgitest.exe example script denial of service
| [6973] Sambar Server Telnet proxy long password buffer overflow
| [6972] Sambar Server Telnet proxy continuous connections denial of service
| [6916] Sambar Server &quot
| [6909] Sambar Server insecure password protection
| [6731] samba NetBIOS name allows remote attackers to create symlink to SMB log file
| [6396] Samba tmpfile symlink attack could allow elevated privileges
| [5445] Samba swat logfile information retrieval
| [5444] Samba swat URL filename denial of service
| [5443] Samba swat logging symbolic link
| [5442] Samba swat brute force attack
| [5247] Sambar search.dll allows attacker to view folders on the system
| [4592] Sambar Server 4.3 buffer overflow
| [3999] Sambar Server hello.bat and echo.bat CGI scripts
| [3227] Samba smbmnt utility could allow mounting to arbitrary mount points
| [3225] Samba message service potential buffer overflow
| [3224] Samba nmbd daemon can be remotely crashed or caused to enter an infinite loop
| [3223] Sambar server allows remote viewing of environment information
| [1672] Sambar Server logging code buffer overflow
| [1671] Sambar mailit client allows script execution
| [1669] Sambar Server ships with default accounts
| [1406] Samba wsmbconf binary allows users access to the group root
| [1311] Samba open share
| [1237] Samba .. Bug
| [337] Samba SMB password buffer overflow
| [9] Samba .. bug
| 
| Exploit-DB - https://www.exploit-db.com:
| [20223] Sambar Server 4.3/4.4 beta 3 Search CGI Vulnerability
| [10095] Samba 3.0.10 - 3.3.5 Format String And Security Bypass Vulnerabilities
| [9950] Samba 3.0.21-3.0.24 LSA trans names Heap Overflow
| [7701] Samba < 3.0.20 - Remote Heap Overflow Exploit
| [4732] Samba 3.0.27a send_mailslot() Remote Buffer Overflow PoC
| [364] Samba <= 3.0.4 SWAT Authorization Buffer Overflow Exploit
| 
| OpenVAS (Nessus) - http://www.openvas.org:
| [90028] Samba 3.0.0 > 3.0.29 vulnerability
| 
| SecurityTracker - https://www.securitytracker.com:
| [1028882] Samba smbd CPU Processing Loop Lets Remote Users Deny Service
| [1026595] Samba smbd Memory Leak Lets Remote Users Deny Service
| [1022976] Samba smbd Processing Flaw Lets Remote Authenticated Users Deny Service
| [1022442] Samba smbd Access Control Bug Lets Remote Authenticated Users Bypass Certain Access Controls
| [1017587] Samba smbd Deferred File Open Processing Bug Lets Remote Users Deny Service
| [1016459] Samba smbd Memory Limit Error in make_connection() Lets Remote Users Deny Service
| [1012587] Samba smbd Integer Overflow in Allocating Security Descriptors May Let Remote Users Execute Arbitrary Code
| [1011223] Samba smbd Infinite Loop Lets Remote Users Consume All Available Memory
| [1011097] Samba FindNextPrintChangeNotify() Error Lets Remote Authenticated Users Crash smbd
| [1006290] Samba 'smbd' Buffer Overflow May Let Remote Users Gain Root Access
| [1028389] Samba Bug Lets Remote Authenticated Users Modify Files
| [1028365] IBM Storwize V7000 Unified Samba Bug Lets Remote Authenticated Users Modify Files
| [1028312] Samba Active Directory Domain Controller File Permission Flaw Lets Remote Authenticated Users Access Files
| [1028006] Samba Active Directory Domain Controller Access Control Flaw Lets Remote Authenticated Gain Write Access to Certain Objects
| [1026988] Samba Local Security Authority Bug Lets Remote Authenticated Users Gain Elevated Privileges
| [1026913] Samba Buffer Overflow in NDR Marshalling Code Lets Remote Users Execute Arbitrary Code
| [1026739] Samba Bug in chain_reply()/construct_reply() Lets Remote Users Execute Arbitrary Code
| [1026727] Blackberry PlayBook Samba File Sharing Lets Remote Users Execute Arbitrary Code
| [1025984] Samba 'mount.cifs' check_newline() Error Lets Local Users Deny Service
| [1025852] Samba Web Administration Tool (SWAT) Input Validation Flaws Permit Cross-Site Request Forgery and Cross-Site Scripting Attacks
| [1025132] Samba FD_SET Stack Corruption Flaw Lets Remote and Local Users Deny Service
| [1024434] Samba Buffer Overflow in sid_parse() Lets Remote Users Execute Arbitrary Code
| [1024107] Samba SMB1 Packet Chaining Memory Corruption Error Lets Remote Users Execute Arbitrary Code
| [1023700] Samba Access Control Flaw Lets Remote Authenticated Users Gain Elevated Privileges
| [1023547] Samba 'mount.cifs' Race Condition Lets Local Users Gain Elevated Privileges
| [1023546] Samba Symlink Configuration Error Lets Remote Users Access Arbitrary Files
| [1022975] Samba 'mount.cifs' Lets Local Users View Portions of Files on the Target System
| [1022441] Samba smbclient Format String Bug May Let Users Execute Arbitrary Code
| [1021513] Samba Grants Remote Authenticated Users Access to the Root Filesystem in Certain Cases
| [1021287] Samba 'trans', 'trans2', and 'nttrans' Requests Let Remote Users Obtain Memory Contents
| [1020770] Samba 'group_mapping.ldb' Has Unsafe Permissions That Let Local Users Gain Elevated Privileges
| [1020123] Samba Buffer Overflow in receive_smb_raw() Lets Remote Users Execute Arbitrary Code
| [1019065] Samba Buffer Overflow in nmbd send_mailslot() Lets Remote Users Execute Arbitrary Code
| [1018954] Samba nmbd Buffer Overflow in Processing GETDC mailslot Requests Lets Remote Users Execute Arbitrary Code
| [1018953] Samba nmbd Buffer Overflow in reply_netbios_packet() Lets Remote Users Execute Arbitrary Code
| [1018681] Samba Winbind SFU/RFC2307 GID Error Lets Local Users Gain Elevated Privileges
| [1018051] Samba 'smb.conf' Scripts Input Validation Flaw Lets Remote Users Inject Arbitrary Commands
| [1018050] Samba Heap Overflows in Parsing NDR Data Let Remote Users Execute Arbitrary Code
| [1018049] Samba SID/Name Translation Bug Lets Local Users Gain Root Privileges
| [1017589] Samba Solaris winbindd Daemon Name Resolution Query Buffer Overflows May Let Remtoe Users Execute Arbitrary Code
| [1017588] Samba Format String Bug in 'afsacl.so' VFS Plugin May Let Remote Users Execute Arbitrary Code
| [1017393] Sambar Server FTP SIZE Command Lets Remote Authenticated Users Deny Service
| [1015850] Samba winbindd Daemon Discloses Server Password to Local Users
| [1012235] Samba QFILEPATHINFO Buffer Overflow Lets Remote Authenticated Users Execute Arbitrary Code
| [1012133] Samba Input Validation Error in ms_fnmatch() Lets Remote Authenticated Users Deny Service
| [1011949] Samba pppd Callback Control Protocol Pointer Dereference May Let Remote Users Deny Service
| [1011469] Samba DOS Path Conversion Flaw Discloses Files to Remote Users
| [1011222] Samba Input Validation Error in nmbd process_logon_packet() Lets Remote Users Crash the nmbd Service
| [1010753] Samba Buffer Overflows in Web Administration Tool and in 'hash' Mangling Method May Let Remote Users Execute Arbitrary Code
| [1010353] Sambar Server 'showini.asp' and 'showlog.asp' Disclose Files to Remote Authenticated Administrators
| [1009503] Samba 'smbprint' Unsafe Temporary File May Let Local Users Gain Elevated Privileges
| [1009000] Samba 'smbmnt' Permissions May Let Local Users Gain Root Privileges
| [1008990] Samba May Let Remote Users Access SMB Accounts That Have Invalid Passwords
| [1008979] Sambar Server 'results.stm' POST Request Buffer Overflow  May Permit Remote Code Execution
| [1007819] Sambar Server Contains Multiple Unspecified Vulnerabilities
| [1007016] Sambar Server Buffer Overflow in 'search.pl' Lets Remote Users Crash the Service
| [1006934] Sambar Server Discloses Files on the System to Remote Users
| [1006637] Sambar Server WebMail Discloses User Passwords Transmitted Via the Network
| [1006498] Samba-TNG Buffer Overflow in call_trans2open() Function Lets Remote Users Execute Arbitrary Code With Root Privileges
| [1006497] Samba Buffer Overflow in call_trans2open() Function Lets Remote Users Execute Arbitrary Code With Root Privileges
| [1006390] Sambar Server Input Validation Flaws Disclose Files on the System to Remote Users and Permit Cross-Site Scripting Attacks
| [1005946] Sambar Server Input Validation Hole in Query Feature Lets Remote Users Conduct Cross-Site Scripting Attacks
| [1005677] Samba Buffer Overflow in User Input Routine May Let Remote Users Execute Arbitrary Code with Root Privileges
| [1004624] HP-UX Samba Common Internet File System (CIFS) Client Buffer Overflow May Let Local Users Obtain Elevated Privileges on the System
| [1004084] Sambar Server Discloses Script Source Code to Remote Users and Can Be Crashed By Remote Users via Malformed URLs
| [1003941] Sambar Server Buffer Overflow Holes Let Remote Users Crash the Service or Execute Arbitrary Code on the System
| [1003246] Sambar Web Server Sample CGI Allows Remote Users to Crash the Web Server
| [1002302] HP CIFS/9000 (Samba) Server Lets Authenticated Remote Users Change Another User's Password
| [1002187] Sambar Telnet Proxy/Server Password Buffer Overflow May Allow Remote Users to Execute Arbitrary Code on the Server
| [1002082] Sambar Web Server Lets Remote Users Modify Files on the Server
| [1002079] Sambar Server Password File Can Be Decrypted By Local Users
| [1002038] Sambar Server's Web Server Lets Local Users Disclose Files Outside of the Documents Directory
| [1002037] Sambar Server's SMTP Mail Server May Allow Remote Users to Relay Mail Through the Server
| [1001826] Samba Common Internet File System (CIFS) Lets Remote Users Obtain Root Level Access
| [1001339] Samba SMB Networking Software Allows Local Users to Destroy Data on Local Devices
| 
| OSVDB - http://www.osvdb.org:
| [95969] Samba smbd nttrans.c read_nttrans_ea_list Function Malformed Packet Handling Remote DoS
| [78651] Samba smbd Connection Request Parsing Remote DoS
| [65518] Samba smbd process.c chain_reply Function SMB1 Packet Chaining Memory Corruption
| [65436] Samba smbd sesssetup.c Session Setup AndX Security Blob Length Value Uninitialized Variable Out-of-bounds DoS
| [65435] Samba smbd process.c chain_reply Function Session Setup AndX Request NULL Dereference Remote DoS
| [58519] Samba smbd Crafted SMB Request Remote CPU Consumption DoS
| [57651] Samba smbd Unspecified Heap Overflow
| [55411] Samba smbd/posix_acls.c acl_group_override Function Remote Access Control List Modification
| [50230] Samba smbd *trans* Request Arbitrary Remote Memory Disclosure
| [33100] Samba smbd Deferred Open Code Infinite Loop DoS
| [12422] Samba smbd Security Descriptor Parsing Remote Overflow
| [9362] Samba smbd FindNextPrintChangeNotify() Request Remote DoS
| [6323] Samba smbd SMB/CIFS Packet Fragment Reassembly Remote Overflow
| [93189] HP MPE/iX with Samba/iX Unspecified Remote Issue
| [92247] Red Hat Storage Management Console GlusterFS extras/hook-scripts/S30samba-stop.sh Symlink Arbitrary File Overwrite
| [91889] Samba SMB2 Implementation CIFS Share Attribute Enforcement Weakness
| [91503] Samba Active Directory Domain Controller CIFS Shares World-writeable Files Creation Weakness
| [91255] ASUS RT-N66U Router root$ Samba Share Export Remote Information Disclosure
| [89627] Samba Web Administration Tool (SWAT) Manipulation CSRF
| [89626] Samba Web Administration Tool (SWAT) Clickjacking Weakness
| [89180] Samba AD DC LDAP Directory Objects Erroneous Write Access Permissions
| [83446] Samba smbmount Multiple Variable Username Handling Local Overflow
| [81648] Samba Multiple Remote Procedural Calls (RPC) Local Security Authority (LSA) Arbitrary File Manipulation
| [81490] Samba mount.cifs chdir() Call File Enumeration
| [81303] Samba RPC Code Generator Network Data Representation (NDR) Multiple Request Parsing Remote Overflow
| [79443] Samba process.c Any Batched (AndX) Request Packet Parsing Remote Overflow
| [79041] Webmin Samba Windows File Sharing Module /tmp/.webmin Local Password Disclosure
| [76058] Samba mtab Lock File Handling Local DoS
| [74872] Samba smbfs mount.cifs / umount.cifs RLIMIT_FSIZE Value Handling mtab Local Corruption DoS
| [74871] Samba mount.cifs Tool Share / Directory Name Newline Injection mtab Corruption Local DoS
| [74072] Samba Web Administration Tool (SWAT) Change Password Page user Field XSS
| [74071] Samba Web Administration Tool (SWAT) Multiple Function CSRF
| [71268] Samba FD_SET Macro Memory Corruption
| [69288] VLC Media Player Samba Network Share Module Incorrect Calling Convention Stack Corruption
| [67994] Samba sid_parse() Function SID Parsing Remote Overflow
| [62803] Samba CAP_DAC_OVERRIDE Capability Flag File Permission Restriction Bypass
| [62187] Samba sid_parse Stack Overflow
| [62186] Samba mount.cifs Symlink Arbitrary File Access
| [62155] Samba smbfs mount.cifs client/mount.cifs.c Crafted String mtab Corruption Local DoS
| [62145] Samba Guest Account Symlink Traversal Arbitrary File Access
| [60587] Windows File Sharing Samba Client Resource Exhaustion DoS
| [59810] Samba reply_nttrans Function Remote Overflow
| [59511] HP-UX CIFS/9000 Server (SAMBA) Unspecified Resource Modification Arbitrary File Overwrite
| [59350] Samba Web Administration Tool (SWAT) Malformed HTTP Request Saturation Remote DoS
| [58520] Samba SUID mount.cifs --verbose Argument Arbitrary File Portion Disclosure
| [57955] Samba Unconfigured Home Directory Windows File Share Directory Access Restriction Bypass
| [57653] Samba Unspecified Heap Overflow
| [57652] Samba --enable-developer Functionality Unspecified Heap Overflow
| [57172] Samba-TNG Unspecified Remote Privilege Escalation
| [55412] Samba smbclient client/client.c Filename Specifiers Multiple Format Strings
| [55370] Sambar Server Pbcgi.exe Remote Overflow
| [55369] Sambar Server testcgi.exe Remote Overflow
| [54378] Samba winbind Daemon Unresponsive Child Process Race Condition DoS
| [53074] Sambar Server /session/sendmail Arbitrary Mail Relay
| [51152] Samba Crafted Connection Request Remote Root File System Access
| [48699] CUPS cupsaddsmb Temporary File Cleartext Samba Credential Disclosure
| [47786] Samba group_mapping.tdb Permission Weakness Privilege Escalation
| [45657] Samba lib/util_sock.c receive_smb_raw() Function Crafted Packet Handling Overflow
| [42884] Sambar Server with IndigoPerl /cgi-bin/com1.pl Arbitrary Command Execution
| [42305] Samba Unspecified Remote Issue
| [42251] Sambar Server Unspecified Remote Command Execution
| [41385] SmbFTPD SMBDirList() Function Directory Name Remote Format String
| [40714] GoSamba main.php include_path Parameter Remote File Inclusion
| [40713] GoSamba inc_user.php include_path Parameter Remote File Inclusion
| [40712] GoSamba inc_smb_conf.php include_path Parameter Remote File Inclusion
| [40711] GoSamba inc_newgroup.php include_path Parameter Remote File Inclusion
| [40710] GoSamba inc_manager.php include_path Parameter Remote File Inclusion
| [40709] GoSamba inc_group.php include_path Parameter Remote File Inclusion
| [40708] GoSamba inc_freigabe3.php include_path Parameter Remote File Inclusion
| [40707] GoSamba inc_freigabe1.php include_path Parameter Remote File Inclusion
| [40706] GoSamba inc_freigabe.php include_path Parameter Remote File Inclusion
| [40705] GoSamba HTML_oben.php include_path Parameter Remote File Inclusion
| [39191] Samba nmdb send_mailslot() Function GETDC mailslot Request Remote Overflow
| [39180] Samba nmbd Crafted GETDC mailslot Request Remote Overflow
| [39179] Samba nmbd nmbd/nmbd_packets.c reply_netbios_packet Function Remote Overflow
| [39178] Samba idmap_ad.so Winbind nss_info Extension (nsswitch/idmap_ad.c) Local Privilege Escalation
| [37795] GSAMBAD /tmp/gsambadtmp Symlink Arbitrary File Overwrite
| [36971] Apple Mac OS X Samba Server Disk Quota Bypass
| [34852] Apple Mac OS X Apple-specific Samba Module (SMB File Server) ACL Handling Overflow
| [34733] Samba DFS RPC Interface DFSEnum Request Remote Overflow
| [34732] Samba SPOOLSS RPC Interface RFNPCNEX Request Remote Overflow
| [34731] Samba SRVSVC RPC Interface NetSetFileSecurity Request Remote Overflow
| [34700] Samba Unfiltered MS-RPC Calls Arbitrary Remote Command Execution
| [34699] Samba LSA RPC Interface Multiple Function Remote Overflow
| [34698] Samba SID/Name Translation Privileged SMB/CIFS Protocol Operation Execution
| [33101] Samba VFS Plugin afsacl.so Format String
| [33098] Samba nss_winbind.so.1 Multiple Function Overflow
| [32336] Sambar FTP Server Malformed SIZE Command DoS
| [27130] Samba smdb Share Connection Saturation DoS
| [24263] Samba winbindd Debug Log Server Credentials Local Disclosure
| [23282] Samba Unspecified Remote Memory Leak Information Disclosure
| [20434] Sambar Server proxy.asp Multiple Field XSS
| [16751] Sambar Server Referer XSS
| [16750] Sambar Server logout RCredirect XSS
| [16749] Sambar Server results.stm indexname XSS
| [14525] Samba Encrypted Password String Conversion Decryption Overflow DoS
| [14233] Sambar Telnet Proxy/Server Long Password Overflow
| [13872] Samba smbclient mput Symlink Arbitrary File Overwrite
| [13871] Samba smbclient more Symlink Arbitrary File Overwrite
| [13870] Samba Printer Queue Query Symlink Arbitrary File Overwrite
| [13397] Samba Multiple Unspecified Overflows
| [12642] Samba .reg File Race Condition Arbitrary File Overwrite
| [11794] Sambar Server whois Script Hostname Remote Overflow
| [11793] Sambar Server finger Script Hostname Remote Overflow
| [11782] Samba QFILEPATHINFO Unicode Filename Request Handler Overflow
| [11555] Samba ms_fnmatch() Function Wildcard Matching Remote DoS
| [11521] Samba Password Field Handling Remote Overflow
| [11479] Microsoft Windows NT Double Dot Samba Client DoS
| [10886] Sambar Web Server Long HTTP GET Request Overflow
| [10464] Samba MS-DOS Path Request Arbitrary File Retrieval
| [9917] Samba nmbd process_logon_packet Function Remote DoS
| [9916] Samba ASN.1 Parsing Function Malformed Request DoS
| [8860] Samba NETBIOS Name Service Daemon DoS
| [8859] Samba smbmnt Race Condition Arbitrary Mount Point
| [8191] Samba Mangling Method Hash Overflow
| [8190] Samba Web Administration Tool (SWAT) HTTP Basic Auth base64 Decoding Remote Overflow
| [7529] Samba wsmbconf Command Execution and Privilege Escalation
| [6585] Sambar Server showini.asp Arbitrary File Access
| [6584] Sambar Server showperf.asp title Parameter XSS
| [6583] Sambar Server show.asp show Parameter XSS
| [5820] Sambar Server vchist.stm Multiple Parameter XSS
| [5819] Sambar Server vccreate.stm Multiple Parameter XSS
| [5818] Sambar Server vccheckin.stm Multiple Parameter XSS
| [5817] Sambar Server update.stm Multiple Parameter XSS
| [5816] Sambar Server template.stm path Parameter XSS
| [5815] Sambar Server sendmail.stm Multiple Parameter XSS
| [5814] Sambar Server rename.stm Multiple Parameter XSS
| [5813] Sambar Server mkdir.stm path Parameter XSS
| [5812] Sambar Server htaccess.stm path Parameter XSS
| [5811] Sambar Server ftp.stm path Parameter XSS
| [5810] Sambar Server info.stm Multiple Parameter XSS
| [5809] Sambar Server create.stm path Parameter XSS
| [5808] Sambar Server iecreate.stm path Parameter XSS
| [5807] Sambar Server edit.stm Multiple Parameter XSS
| [5806] Sambar Server ieedit.stm Multiple Parameter XSS
| [5805] Sambar Server search.dll query Parameter XSS
| [5804] Sambar Server environ.pl param1 Parameter XSS
| [5803] Sambar Server testisa.dll check1 Parameter XSS
| [5802] Sambar Server echo.bat Code Execution
| [5786] Sambar Server results.stm Overflow
| [5785] Sambar Server book.pl E-mail Field XSS
| [5784] Sambar Server dumpenv.pl XSS
| [5783] Sambar Server ssienv.shtml XSS
| [5782] Sambar Server mortgage.pl price Parameter XSS
| [5781] Sambar Server DOS Device Name Code Execution
| [5780] Sambar Server Proxy IP Filter Bypass
| [5468] Sambar Server Password Encryption Scheme Weakness
| [5123] Sambar DOS Device Name DoS
| [5122] Sambar Server Null Terminated URL Arbitrary File Source Disclosure
| [5108] Sambar Server search.stm Multiple Parameter XSS
| [5107] Sambar Server findata.stm Multiple Parameter XSS
| [5106] Sambar Server whodata.stm sitename Parameter XSS
| [5105] Sambar Server showfnc.stm pkg Parameter XSS
| [5104] Sambar Server showfncs.stm pkg Parameter XSS
| [5103] Sambar Server showfunc.stm func Parameter XSS
| [5102] Sambar Server stmex.stm XSS
| [5101] Sambar Server ipdata.stm ipaddr Parameter XSS
| [5100] Sambar Server testcgi.exe XSS
| [5097] Sambar Server index.stm wwwsite Parameter XSS
| [5096] Sambar Server iecreate.stm Directory Listing
| [5095] Sambar Server ieedit.stm Directory Listing
| [5094] Sambar Server testcgi.exe Environment Variable Disclosure
| [5093] Sambar Server environ.pl Environment Variable Disclosure
| [4469] Samba trans2.c call_trans2open() Function Overflow
| [3919] Samba mksmbpasswd.sh Uninitialized Passwords
| [3916] Samba smbmnt Local Privilege Escalation
| [2204] Sambar Server search.pl results.stm Overflow DoS
| [1626] Samba Web Administration Tool (SWAT) cgi.log Permission Weakness Information Disclosure
| [1625] Samba Web Administration Tool (SWAT) Failed Login Logging Failure Weakness
| [1025] Samba smdb Malformed Message Handling Remote Overflow
| [861] Samba enum_csc_policy Data Structure Termination Remote Overflow
| [656] Samba NETBIOS Name Traversal Arbitrary Remote File Creation
| [589] Sambar Web Server pagecount CGI Traversal Arbitrary File Overwrite
| [487] Samba Web Administration Tool (SWAT) Error Message Username Enumeration
| [413] Sambar Server ISAPI Search Utility search.dll Query Parameter Parsing Folder Name Disclosure
| [319] Sambar Server mailit.pl Arbitrary Mail Relay
| [318] Sambar Server Sysadmin Web Interface Default Account
| [317] Sambar sendmail CGI Arbitrary Mail Relay
| [215] Samba Web Administration Tool (SWAT) cgi.log Symlink Arbitrary File Modification
| [194] Sambar Server hello.bat Code Execution
| [52] Sambar Server dumpenv.pl Information Disclosure
| [34] Sambar Server cgitest.exe Crafted GET Request Parsing Remote Overflow
|_
MAC Address: 00:15:5D:00:04:10 (Microsoft)
Service Info: Host: TARGET1; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon May 17 22:53:39 2021 -- 1 IP address (1 host up) scanned in 23.11 seconds