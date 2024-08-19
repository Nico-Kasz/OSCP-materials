Source: https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide#documentation-requirements

#### [Screenshot Requirements](https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide#screenshot-requirements)

Each local.txt and proof.txt found must be shown in a screenshot that includes the contents of the file, as well as the **IP address** of the target by using `ipconfig`, `ifconfig` or `ip addr`. 
#### [Documentation Requirements](https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide#documentation-requirements)

You are required to write a professional report describing your exploitation process for each target. You must document all of your attacks including all steps, commands issued, and console output in the form of a penetration test report. Your documentation should be thorough enough that your attacks can be replicated step-by-step by a technically competent reader.
#### [Exploit Code](https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide#exploit-code)

If you have not made any modifications to an exploit, you should only provide the URL where the exploit can be found. Do not include the full unmodified code, especially if it is several pages long.

If you have modified an exploit, you should include:

- The modified exploit code
- The URL to the original exploit code
- The command used to generate any shellcode (if applicable)
- Highlighted changes you have made
- An explanation of why those changes were made
#### [Exam Proofs](https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide#exam-proofs)

==**Failure to provide the appropriate proof files in a screenshot for each machine will result in zero points being awarded for the target.**==

The valid way to provide the contents of the proof files is in an interactive shell on the target machine with the `type` or `cat` command from **their original location**.

**Obtaining the contents of the proof files in any other way will result in zero points for the target machine; this includes any type of web-based shell.**


On all Windows targets, you must have a shell running with the permissions of one of the following to receive full points:

- SYSTEM user
- Administrator user
- User with Administrator privileges

On all Linux targets, you must have a root shell in order to receive full points.
Each local.txt and proof.txt found must be shown in a screenshot that includes the contents of the file, as well as the **IP address** of the target by using `ipconfig`, `ifconfig` or `ip addr`. An example of this is shown below:

#### [Exam Restrictions](https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide#exam-restrictions)

You cannot use any of the following on the exam:

- Spoofing (IP, ARP, DNS, NBNS, etc)
- Commercial tools or services (Metasploit Pro, Burp Pro, etc.)
- Automatic exploitation tools (e.g. db_autopwn, browser_autopwn, ==SQLmap==, SQLninja etc.)
- Mass vulnerability scanners (e.g. Nessus, NeXpose, OpenVAS, Canvas, Core Impact, SAINT, etc.)
- ==AI Chatbots (e.g. ChatGPT, YouChat, etc.)==
- Features in other tools that utilize either forbidden or restricted exam limitations

==You may however, use tools such as Nmap (and its scripting engine), Nikto, Burp Free, DirBuster etc. against any of your target systems.==

#### [Metasploit Restrictions](https://help.offsec.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide#metasploit-restrictions)

The usage of Metasploit and the Meterpreter payload are restricted during the exam. You may only use Metasploit modules (==**Auxiliary, Exploit, and Post**==) or the Meterpreter payload against ==**one** single target machine of your choice.== Once you have selected your one target machine, you cannot use Metasploit modules ( Auxiliary, Exploit, or Post ) or the Meterpreter payload against any other machines.
 
Metasploit/Meterpreter **should not** be used to test vulnerabilities on multiple machines before selecting your one target machine ( this includes the use of **check** ) . You may use Metasploit/Meterpreter as many times as you would like against your one target machine.

If you decide to use Metasploit or Meterpreter on a specific target and the attack fails, then you **may not** attempt to use it on a second target. In other words, the use of Metasploit and Meterpreter becomes locked in as soon as you decide to use either one of them.

==Metasploit **cannot** be used for **pivoting**, because it would thereby be used on more than one target.==

You may use the following against all of the target machines with the exception that meterpreter payload could be used only against one target machine:

- multi handler (aka exploit/multi/handler)
- msfvenom

All the above limitations also apply to different interfaces that make use of Metasploit (such as Armitage, Cobalt Strike, Metasploit Community Edition, etc).