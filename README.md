# Weitinhsi

## Introduction

The Weitinhsi is a system to automatically generate events for the Windows sample such as PE file, MS Word, batch files and so on.
Instead of patching the Windows API, the core module "minidbg.exe" simulates the debugger to install break points and monitors certain APIs. The API list can be defined by the configuration.

The example for the configuration:
```

api:ntdll.dll!NtCreateFile,p$$$x$$$o$$$x$$$x$$$x$$$x$$$x$$$x$$$x$$$x$$$,3
api:ntdll.dll!NtOpenFile,p$$$x$$$o$$$x$$$x$$$x$$$,3

api:ntdll.dll!NtDeleteFile,o$$$,3
api:ntdll.dll!NtCreateSection,p$$$x$$$o$$$p$$$x$$$x$$$x$$$,3
api:ntdll.dll!NtOpenSection,p$$$x$$$o$$$,3
api:ntdll.dll!NtCreateEvent,p$$$x$$$o$$$x$$$x$$$,3
api:ntdll.dll!NtOpenEvent,p$$$x$$$o$$$,3
api:ntdll.dll!NtCreateSemaphore,p$$$x$$$o$$$x$$$x$$$,3
api:ntdll.dll!NtOpenSemaphore,p$$$x$$$o$$$,3
api:ntdll.dll!NtCreateMutant,p$$$x$$$o$$$x$$$,3
api:ntdll.dll!NtOpenMutant,p$$$x$$$o$$$,3
api:ntdll.dll!NtCreateKey,p$$$x$$$o$$$x$$$u$$$x$$$p$$$,3
api:ntdll.dll!NtOpenKey,p$$$x$$$o$$$,3
api:ntdll.dll!NtOpenKeyEx,p$$$x$$$o$$$x$$$,3
api:ntdll.dll!NtSetValueKey,x$$$u$$$x$$$x$$$x$$$x$$$,3
api:ntdll.dll!NtProtectVirtualMemory,x$$$p$$$p$$$x$$$p2u$,3
api:ntdll.dll!NtWriteVirtualMemory,x$$$x$$$x$$$x$$$p$$$,3
api:ntdll.dll!NtCreateUserProcess,p$$$p$$$x$$$x$$$o$$$o$$$x$$$x$$$p$$$p$$$p$$$,3
api:ntdll.dll!NtOpenProcess,p$$$x$$$p$$$c$$$,3

api:ntdll.dll!NtAlpcSendWaitReceivePort,x$$$x$$$p$$$p$$$p$$$p$$$p$$$p$$$,3
api:ntdll.dll!NtAlpcSetInformation,x$$$x$$$x$$$x$$$,3
api:ntdll.dll!NtAlpcConnectPort,p$$$u$$$o$$$p$$$x$$$p$$$p$$$p$$$p$$$p$$$p$$$,3
api:ntdll.dll!LdrLoadDll,x$$$x$$$u$$$p$$$,3

```

## Requirements

The Weitinhsi needs run under x64 Windows OS. Either create an Windows instance in GCP or create a Debian 12 instance and run a nested [QEMU Windows VM](./qemu/README.md) in GCP.
