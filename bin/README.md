# minidbg

The minidbg is a monitoring tool for Windows OS to record the application's events.
The caller needs to specify the Windows sample file into the batch file named "sample.bat".
By default the minidbg will generate logs under the temp folder. For example, logs are as below.

With base64 encoding:
```
0x0004d09b,2088,11196,process,7692,b64::QzpcV2luZG93c1xTeXN0ZW0zMlxjbWQuZXhl,b64::Y21kLmV4ZSAvQyBjOlxteWFwcFxzYW1wbGUuYmF0,0000002259171000,0000000000000000
0x0004d09c,2088,11196,module,b64::QzpcV2luZG93c1xTeXN0ZW0zMlxjbWQuZXhl,base:0x00007FF76B490000
0x0004d09d,2088,11196,module,b64::QzpcV2luZG93c1xTeXN0ZW0zMlxudGRsbC5kbGw=,base:0x00007FFD381D0000
0x0004d09e,2088,11196,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7ffd3836e530,0x8,0x4,0x00000000)=0x00007FFD3826FD60 from 0x00007FFD381FB1F9 (ntdll.dll+0x2b1f9)
0x0004d0a0,2088,11196,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7ffd3836e000,0x1000,0x8,0x00000008)=0x00007FFD3826FD60 from 0x00007FFD381FB21D (ntdll.dll+0x2b21d)
0x0004d0a2,2088,11196,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFD3826FC60 from 0x00007FFD3827D43C (ntdll.dll+0xad43c)
0x0004d0a3,2088,11196,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFD3826FC60 from 0x00007FFD3829A0B9 (ntdll.dll+0xca0b9)
```

```
0x023b952d,15192,14952,process,14328,C:\Windows\System32\cmd.exe,cmd.exe /C c:\myapp\sample.bat,0000006DD8E7C000,0000000000000000
0x023b952d,15192,14952,module,C:\Windows\System32\cmd.exe,base:0x00007FF6C7F80000
0x023b952e,15192,14952,module,C:\Windows\System32\ntdll.dll,base:0x00007FFF6C950000
0x023b952f,15192,14952,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7fff6caee530,0x8,0x4,0x00000000)=0x00007FFF6C9EFD60 from 0x00007FFF6C97B1F9 (ntdll.dll+0x2b1f9)
0x023b9532,15192,14952,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7fff6caee000,0x1000,0x8,0x00000008)=0x00007FFF6C9EFD60 from 0x00007FFF6C97B21D (ntdll.dll+0x2b21d)
0x023b9533,15192,14952,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFF6C9EFC60 from 0x00007FFF6C9FD43C (ntdll.dll+0xad43c)
0x023b9535,15192,14952,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFF6C9EFC60 from 0x00007FFF6CA1A0B9 (ntdll.dll+0xca0b9)
```

The checksum for the minidbg.
```
cd83b51129703d1ce67471d395297ea47089f8b6e867d73bf7379972d4567d25  minidbg.exe
```
