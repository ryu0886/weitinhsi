# minidbg

The minidbg is a monitoring tool for Windows OS to record the application's events.
The startup point is the minidbg's path but suffixed with ".bat" instead of ".exe".
For example, the caller needs to specify the Windows sample path into the batch file named "minidbg.bat".
The minidbg will generate logs under the same folder. For example, the log file name is "minidbg.log".

With base64 encoding:
```
0x006b25cd,9116,10744,process,11184,b64::QzpcV2luZG93c1xTeXN0ZW0zMlxjbWQuZXhl,b64::QzpcV2luZG93c1xzeXN0ZW0zMlxjbWQuZXhlIC9jICJDOlx2bVxtaW5pZGJnLmJhdCI=,00000037D11FC000,0000000000000000
0x006b25cf,9116,10744,module,b64::QzpcV2luZG93c1xTeXN0ZW0zMlxjbWQuZXhl,base:0x00007FF68B5D0000
0x006b25d0,9116,10744,module,b64::QzpcV2luZG93c1xTeXN0ZW0zMlxudGRsbC5kbGw=,base:0x00007FFE49870000
0x006b25d1,9116,10744,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7ffe49a0e530,0x8,0x4,0x00000000)=0x00007FFE4990FD60 from 0x00007FFE4989B1F9 (ntdll.dll+0x2b1f9)
0x006b25d2,9116,10744,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7ffe49a0e000,0x1000,0x8,0x00000008)=0x00007FFE4990FD60 from 0x00007FFE4989B21D (ntdll.dll+0x2b21d)
0x006b25d3,9116,10744,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFE4990FC60 from 0x00007FFE4991D43C (ntdll.dll+0xad43c)
0x006b25d5,9116,10744,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFE4990FC60 from 0x00007FFE4993A0B9 (ntdll.dll+0xca0b9)
```

After decoding to the original string:
```
0x006b25cd,9116,10744,process,11184,C:\Windows\System32\cmd.exe,C:\Windows\system32\cmd.exe /c "C:\vm\minidbg.bat",00000037D11FC000,0000000000000000
0x006b25cf,9116,10744,module,C:\Windows\System32\cmd.exe,base:0x00007FF68B5D0000
0x006b25d0,9116,10744,module,C:\Windows\System32\ntdll.dll,base:0x00007FFE49870000
0x006b25d1,9116,10744,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7ffe49a0e530,0x8,0x4,0x00000000)=0x00007FFE4990FD60 from 0x00007FFE4989B1F9 (ntdll.dll+0x2b1f9)
0x006b25d2,9116,10744,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7ffe49a0e000,0x1000,0x8,0x00000008)=0x00007FFE4990FD60 from 0x00007FFE4989B21D (ntdll.dll+0x2b21d)
0x006b25d3,9116,10744,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFE4990FC60 from 0x00007FFE4991D43C (ntdll.dll+0xad43c)
0x006b25d5,9116,10744,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFE4990FC60 from 0x00007FFE4993A0B9 (ntdll.dll+0xca0b9)
```

The checksum for the minidbg.
```
cd83b51129703d1ce67471d395297ea47089f8b6e867d73bf7379972d4567d25  minidbg.exe
```