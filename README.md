# winDED

Custom exploit for CVE-2023-38831 using python.

# Introduction:
WinRAR is an archiving software that allows users to create file archives and zipped versions of files and folders so that users can easily transport files/ folders or store them at a compressed size. I mean, you’ve heard of it, most definitely. It embeds checksums to ensure file integrity, allowing for ease of use of the compressed files or folders. It also employs optional encryption. But as we know, nothing is truly safe.

The WinRAR vulnerability, also known as CVE-2023-38831, was discovered in April 2023 by a security researcher, who goes by the name "Goodbyeselene", while analyzing the code of WinRAR. The vulnerability is a logic issue in the WinRAR archive extractor that could allow an attacker to execute arbitrary code on a victim's computer and exists because WinRAR incorrectly handles certain file extensions when extracting files from ZIP archives.

Refer to [this](https://nvd.nist.gov/vuln/detail/CVE-2023-38831) document to get a more in-depth understanding about WinRAR’s vulnerability.

> For explanation of exploit, please check [exploit_with_comments.py](https://github.com/r1yaz/winDED/blob/main/exploit_with_comments.py).

## How to exploit
1. Preferably in a virtualized Windows OS, install WinRAR version 6.21.0. Link to grab this is [here](https://filehippo.com/download_winrar-64/6.21/).
>NOTE: DO NOT, I repeat, DO NOT, use this version for your personal machine's WinRAR. It is vulnerable. Please fetch the latest WinRAR version from [here](https://www.win-rar.com/start.html?&L=0) for your personal machine.

>NOTE 2: I am not the author/hoster and am not responsible for the file you download from https://filehippo.com/download_winrar-64/6.21/ for the Winrar version 6.21. Feel free to grab your own version. Use a VM!

2. Download [BILLION_DOLLAR_SECRET.pdf](https://github.com/r1yaz/winDED/blob/main/BILLION_DOLLAR_SECRET.pdf) (Or create your own pdf and name it the same).

3. Download [super_sneaky_evil_script.bat](https://github.com/r1yaz/winDED/blob/main/super_sneaky_evil_script.bat) (Or create your own bat file and name it the same).

4. Run either [exploit_with_comments.py](https://github.com/r1yaz/winDED/blob/main/exploit_with_comments.py) OR [just_the_exploit.py](https://github.com/r1yaz/winDED/blob/main/just_the_exploit.py).

5. Open the newly created zip file (name would be BILLION_DOLLAR_SECRET.rar). Double click the second pdf file, not folder, you see. It should execute the contents of the super_sneaky_evil_script.bat and spawn a calc instance and open up the pdf as well. Refer to screenshot below.

![Image showing which pdf file to click](https://raw.githubusercontent.com/r1yaz/winDED/main/step5.png)

### References and Citations
1. https://www.bleepingcomputer.com/news/security/winrar-zero-day-exploited-since-april-to-hack-trading-accounts/
2. https://www.rapid7.com/db/modules/exploit/windows/fileformat/winrar_cve_2023_38831/
3. https://github.com/rapid7/metasploit-framework/blob/master//modules/exploits/windows/fileformat/winrar_cve_2023_38831.rb
5. https://winrar.en.uptodown.com/windows/versions
6. https://b1tg.github.io/post/cve-2023-38831-winrar-analysis/
7. https://isc.sans.edu/diary/Analysis+of+RAR+Exploit+Files+CVE202338831/30164/
