# minidbg

The minidbg is a monitoring tool for Windows OS to record the application's events.
By default minidbg will generate logs under temp folder such logs below.
The caller need specify the Windows sample file into batch file "sample.bat".
'''
0x023b952d,15192,14952,process,14328,C:\Windows\System32\cmd.exe,cmd.exe /C c:\myapp\sample.bat,0000006DD8E7C000,0000000000000000
0x023b952d,15192,14952,module,C:\Windows\System32\cmd.exe,base:0x00007FF6C7F80000
0x023b952e,15192,14952,module,C:\Windows\System32\ntdll.dll,base:0x00007FFF6C950000
0x023b952f,15192,14952,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7fff6caee530,0x8,0x4,0x00000000)=0x00007FFF6C9EFD60 from 0x00007FFF6C97B1F9 (ntdll.dll+0x2b1f9)
0x023b9532,15192,14952,api,ntdll.dll!NtProtectVirtualMemory(0xffffffffffffffff,0x7fff6caee000,0x1000,0x8,0x00000008)=0x00007FFF6C9EFD60 from 0x00007FFF6C97B21D (ntdll.dll+0x2b21d)
0x023b9533,15192,14952,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFF6C9EFC60 from 0x00007FFF6C9FD43C (ntdll.dll+0xad43c)
0x023b9535,15192,14952,api,ntdll.dll!NtCreateEvent(0x0,0x1f0003,,0x0,0x0)=0x00007FFF6C9EFC60 from 0x00007FFF6CA1A0B9 (ntdll.dll+0xca0b9)
'''
