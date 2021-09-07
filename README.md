# ymir
ymir is a sniffing tool ("sniffer") which captures traffic sent between wow servers and clients and writes it to a file. 

## Disclaimer

Use at your own risk, TrinityCore is not responsible for any actions caused (by Activision Blizzard, jurists or anyone else) due to usage of this tool.  
The generated sniff files contain private data (e.g. your real name), so its highly advised to only share it with TrinityCore developers and official contributors.

Since initial development during patch 8.1.5/Retail no known bans were caused so far. Nevertheless this is no proof for total security.

## Operating system requirements
The sniffer is developed for usage on Windows 10.  
It might be possible to use it on OS X via. wine (untested)

## Installation
1. Download and install Npcap using Npcap installer from https://nmap.org/npcap/ (and install it in **WinPcap compatibility mode**)
2. Download sniffer binary for your version, patch from [Releases](http://github.com/TrinityCore/ymir/releases) and save it anywhere (preferably not in wow directory)

## How to sniff
1. Delete Cache directory within your relevant wow installation (for retail e.g. inside *\_retail\_* directory)
2. Start *ymir_retail.exe* (name might be different depending on wow branch, e.g. *ymir_ptr.exe* for PTR)
3. Start wow client (via Battle.net or explorer)
4. Sniffs will be saved in the dump/ subdirectory next to the sniffer while playing
5. When done playing just close wow regularly and wait for the sniffer to close automatically (usually happens 1-5s after client is closed)
6. Compress sniff in 7z, rar or zip, upload them to any file hoster (e.g. mega, zippyshare) and share the links [in the TC Forum](https://community.trinitycore.org/forum/13-wdbadbsniffs/), we're working on an easier solution for this already.

## Tips
You can combine step 1 & 2 with a batch file (adjust paths to your needs, especially partitions *E:* and *F:*):
```batch
E:
cd E:\Games\World of Warcraft\_retail_\
rmdir /S /Q Cache

F:
cd F:\ymir\Retail
start ymir_retail.exe
```

## Sniff processing
The saved sniffs may be further processed using [WowPacketParser](http://github.com/TrinityCore/WowPacketParser)

## Authors
- [shelby](http://github.com/Izidor)
- [ModoX](http://github.com/mdX7)
- [Shauren](http://github.com/Shauren)
