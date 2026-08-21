*Centralized resource for listing and organizing known injection techniques and POCs*

* [Introduction](#introduction)
* [Linux Injection](#linux-injection)
  * [Process Spawning](#process-spawning)
    * [LD\_PRELOAD](#ld_preload)
    * [Seccomp Notifier](#seccomp-notifier)
  * [Process Injection](#process-injection)
    * [PTRACE](#ptrace)
    * [Proc Memory](#proc-memory)
* [Windows Injection](#windows-injection)
  * [Process Spawning](#process-spawning-1)
    * [Process Hollowing](#process-hollowing)
    * [Transacted Hollowing](#transacted-hollowing)
    * [Process Doppelganging](#process-doppelganging)
    * [Process Herpaderping](#process-herpaderping)
    * [Process Ghosting](#process-ghosting)
    * [Early Bird](#early-bird)
    * [EntryPoint Patching](#entrypoint-patching)
    * [Ruy-Lopez](#ruy-lopez)
    * [Early Cascade Injection](#early-cascade-injection)
    * [Kernel Callback Table Injection](#kernel-callback-table-injection)
    * [PichichiH0ll0wer - Split Hollowing](#pichichih0ll0wer---split-hollowing)
  * [Process Injection](#process-injection-1)
    * [Classic Dll Injection](#classic-dll-injection)
    * [Classic Shellcode Injection](#classic-shellcode-injection)
    * [Dll Injection via SetWindowsHookEx](#dll-injection-via-setwindowshookex)
    * [Reflective Dll Injection](#reflective-dll-injection)
    * [PE Injection](#pe-injection)
    * [Section Mapping Injection](#section-mapping-injection)
    * [APC Queue Injection](#apc-queue-injection)
    * [Thread Execution Hijacking](#thread-execution-hijacking)
    * [Atom Bombing Injection](#atom-bombing-injection)
    * [Mocking jay Injection](#mocking-jay-injection)
    * [ListPlanting Injection](#listplanting-injection)
    * [Extra Window Memory Injection](#extra-window-memory-injection)
    * [ThreadlessInject](#threadlessinject)
    * [EPI](#epi)
    * [DllNotification Injection](#dllnotification-injection)
    * [D1rkInject](#d1rkinject)
    * [NtQueueAPCThreadEx Gadget Injection](#ntqueueapcthreadex-gadget-injection)
    * [Dirty-Vanity](#dirty-vanity)
    * [Function Stomping](#function-stomping)
    * [Caro-Kann](#caro-kann)
    * [Stack Bombing](#stack-bombing)
    * [Ghost Injector](#ghost-injector)
    * [Ghost Writing](#ghost-writing)
    * [Ghost Writing 2](#ghost-writing-2)
    * [Mapping Injection with Instrumentation Callback](#mapping-injection-with-instrumentation-callback)
    * [SetProcessInjection](#setprocessinjection)
    * [Pool Party Injection](#pool-party-injection)
    * [Thread Name Calling](#thread-name-calling)
    * [Waiting Thread Hijacking](#waiting-thread-hijacking)
    * [RedirectThread Context Injection](#redirectthread-context-injection)
    * [Overwriting Loaded DLL EntryPoint](#overwriting-loaded-dll-entrypoint)
    * [Living Of The Process by g3tsyst3m](#living-of-the-process-by-g3tsyst3m)

# Awesome Introduction with stars

I've been thinking about putting together a list of process injection techniques and ingenious POCs because I haven't found a decent one. This list focuses on process-spawning injection methods and actual process injection, excluding pre-execution techniques (e.g. AppCert and AppInit Dlls), and self-injection techniques.

**PRs are welcome to help me maintain and extend this list!**

# Linux Injection

## Process Spawning

#### LD\_PRELOAD

* <https://attack.mitre.org/techniques/T1574/006/>

#### Seccomp Notifier

* <https://www.outflank.nl/blog/2025/12/09/seccomp-notify-injection/>
* <https://github.com/outflanknl/seccomp-notify-injection> ⭐ 95 | 🐛 0 | 🌐 C | 📅 2025-12-09

## Process Injection

#### PTRACE

* <https://attack.mitre.org/techniques/T1055/008/>
* <https://github.com/kubo/injector> ⚠️ Archived

#### Proc Memory

* <https://github.com/DavidBuchanan314/dlinject> ⭐ 826 | 🐛 11 | 🌐 Python | 📅 2025-02-09
* <https://github.com/AonCyberLabs/Cexigua> ⭐ 260 | 🐛 0 | 🌐 Shell | 📅 2017-08-24
* <https://attack.mitre.org/techniques/T1055/009/>

# Windows Injection

## Process Spawning

#### Process Hollowing

* <https://attack.mitre.org/techniques/T1055/012/>
* <https://github.com/m0n0ph1/Process-Hollowing>

#### Transacted Hollowing

* <https://github.com/hasherezade/transacted_hollowing> ⭐ 586 | 🐛 2 | 🌐 C | 📅 2024-03-08

#### Process Doppelganging

* <https://attack.mitre.org/techniques/T1055/013/>
* <https://github.com/hasherezade/process_doppelganging> ⭐ 652 | 🐛 2 | 🌐 C | 📅 2022-08-30

#### Process Herpaderping

* <https://github.com/jxy-s/herpaderping> ⭐ 1,208 | 🐛 1 | 🌐 C++ | 📅 2023-07-05

#### Process Ghosting

* <https://github.com/hasherezade/process_ghosting> ⭐ 700 | 🐛 7 | 🌐 C | 📅 2024-03-11

#### Early Bird

* <https://www.cyberbit.com/endpoint-security/new-early-bird-code-injection-technique-discovered/>
* <https://www.ired.team/offensive-security/code-injection-process-injection/early-bird-apc-queue-code-injection>

#### EntryPoint Patching

* <https://www.ired.team/offensive-security/code-injection-process-injection/addressofentrypoint-code-injection-without-virtualallocex-rwx>

#### Ruy-Lopez

* <https://github.com/S3cur3Th1sSh1t/Ruy-Lopez> ⭐ 323 | 🐛 0 | 🌐 C | 📅 2023-06-28

#### Early Cascade Injection

* <https://www.outflank.nl/blog/2024/10/15/introducing-early-cascade-injection-from-windows-process-creation-to-stealthy-injection/>
* <https://github.com/Cracked5pider/earlycascade-injection> ⚠️ Archived

#### Kernel Callback Table Injection

* <https://github.com/0xHossam/KernelCallbackTable-Injection-PoC> ⭐ 276 | 🐛 0 | 🌐 C | 📅 2024-10-31

#### PichichiH0ll0wer - Split Hollowing

* <https://github.com/itaymigdal/PichichiH0ll0wer> ⭐ 65 | 🐛 0 | 🌐 Nim | 📅 2025-07-22

## Process Injection

#### Classic Dll Injection

* <https://attack.mitre.org/techniques/T1055/001/>
* <https://www.ired.team/offensive-security/code-injection-process-injection/dll-injection>

#### Classic Shellcode Injection

* <https://www.ired.team/offensive-security/code-injection-process-injection/process-injection>

#### Dll Injection via SetWindowsHookEx

* <https://github.com/DrNseven/SetWindowsHookEx-Injector> ⭐ 186 | 🐛 0 | 🌐 C | 📅 2023-04-18

#### Reflective Dll Injection

* <https://attack.mitre.org/techniques/T1055/001/>
* <https://github.com/stephenfewer/ReflectiveDLLInjection> ⭐ 3,338 | 🐛 15 | 🌐 C | 📅 2022-09-03
* <https://www.ired.team/offensive-security/code-injection-process-injection/reflective-dll-injection>

#### PE Injection

* <https://attack.mitre.org/techniques/T1055/002/>
* <https://www.ired.team/offensive-security/code-injection-process-injection/pe-injection-executing-pes-inside-remote-processes>

#### Section Mapping Injection

* <https://www.ired.team/offensive-security/code-injection-process-injection/ntcreatesection-+-ntmapviewofsection-code-injection>

#### APC Queue Injection

* <https://attack.mitre.org/techniques/T1055/004/>
* <https://www.ired.team/offensive-security/code-injection-process-injection/apc-queue-code-injection>

#### Thread Execution Hijacking

* <https://attack.mitre.org/techniques/T1055/003/>
* <https://www.ired.team/offensive-security/code-injection-process-injection/injecting-to-remote-process-via-thread-hijacking>

#### Atom Bombing Injection

* <https://github.com/BreakingMalwareResearch/atom-bombing> ⭐ 741 | 🐛 9 | 🌐 C++ | 📅 2020-10-07

#### Mocking jay Injection

* <https://www.securityjoes.com/post/process-mockingjay-echoing-rwx-in-userland-to-achieve-code-execution>

#### ListPlanting Injection

* <https://attack.mitre.org/techniques/T1055/015/>
* <https://cocomelonc.github.io/malware/2022/11/27/malware-tricks-24.html>

#### Extra Window Memory Injection

* <https://attack.mitre.org/techniques/T1055/011/>
* <https://github.com/BreakingMalware/PowerLoaderEx> ⭐ 385 | 🐛 3 | 🌐 C++ | 📅 2017-04-17

#### ThreadlessInject

* <https://github.com/CCob/ThreadlessInject> ⭐ 825 | 🐛 0 | 🌐 C# | 📅 2024-09-04

#### EPI

* <https://github.com/Kudaes/EPI> ⭐ 356 | 🐛 0 | 🌐 Rust | 📅 2024-09-10

#### DllNotification Injection

* <https://github.com/Dec0ne/DllNotificationInjection> ⭐ 470 | 🐛 3 | 🌐 C++ | 📅 2023-08-23

#### D1rkInject

* <https://github.com/TheD1rkMtr/D1rkInject> ⭐ 187 | 🐛 0 | 🌐 C++ | 📅 2023-08-02

#### NtQueueAPCThreadEx Gadget Injection

* <https://github.com/LloydLabs/ntqueueapcthreadex-ntdll-gadget-injection> ⭐ 267 | 🐛 1 | 🌐 C | 📅 2023-04-29

#### Dirty-Vanity

* <https://github.com/deepinstinct/Dirty-Vanity> ⭐ 678 | 🐛 1 | 🌐 C | 📅 2022-12-23

#### Function Stomping

* <https://github.com/Idov31/FunctionStomping> ⚠️ Archived

#### Caro-Kann

* <https://github.com/S3cur3Th1sSh1t/Caro-Kann> ⭐ 430 | 🐛 0 | 🌐 C | 📅 2023-09-12

#### Stack Bombing

* <https://github.com/maziland/StackBombing> ⭐ 55 | 🐛 0 | 🌐 C++ | 📅 2020-07-09

#### Ghost Injector

* <https://github.com/woldann/GhostInjector> ⭐ 29 | 🐛 1 | 🌐 C | 📅 2025-12-01

#### Ghost Writing

* <https://github.com/c0de90e7/GhostWriting> ⭐ 199 | 🐛 0 | 🌐 C | 📅 2018-03-26
* <https://blog.sevagas.com/IMG/pdf/code_injection_series_part5.pdf>

#### Ghost Writing 2

* <https://github.com/fern89/ghostwriting-2> ⭐ 42 | 🐛 0 | 🌐 C | 📅 2023-12-18

#### Mapping Injection with Instrumentation Callback

* <https://github.com/antonioCoco/Mapping-Injection> ⭐ 408 | 🐛 0 | 🌐 Assembly | 📅 2020-08-07

#### SetProcessInjection

* <https://github.com/OtterHacker/SetProcessInjection> ⭐ 155 | 🐛 1 | 🌐 C | 📅 2023-10-02

#### Pool Party Injection

* <https://www.safebreach.com/blog/process-injection-using-windows-thread-pools>
* <https://github.com/SafeBreach-Labs/PoolParty> ⭐ 1,285 | 🐛 2 | 🌐 C++ | 📅 2023-12-11

#### Thread Name Calling

* <https://github.com/hasherezade/thread_namecalling> ⭐ 312 | 🐛 1 | 🌐 C | 📅 2025-04-18
* <https://research.checkpoint.com/2024/thread-name-calling-using-thread-name-for-offense/>

#### Waiting Thread Hijacking

* <https://github.com/hasherezade/waiting_thread_hijacking> ⭐ 266 | 🐛 0 | 🌐 C | 📅 2025-08-31
* <https://research.checkpoint.com/2025/waiting-thread-hijacking/>

#### RedirectThread Context Injection

* <https://blog.fndsec.net/2025/05/16/the-context-only-attack-surface/>
* <https://github.com/Friends-Security/RedirectThread> ⭐ 207 | 🐛 2 | 🌐 C++ | 📅 2025-06-17

#### Overwriting Loaded DLL EntryPoint

* <https://github.com/RWXstoned/LdrShuffle> ⭐ 288 | 🐛 0 | 🌐 C++ | 📅 2025-06-04

#### Living Of The Process by g3tsyst3m

* <https://g3tsyst3m.com/lotp/Living-off-the-Process/>
* <https://github.com/g3tsyst3m/CodefromBlog/tree/main/2026-1-29-Living%20off%20the%20Process/LOTP_blog> ⭐ 118 | 🐛 0 | 🌐 C++ | 📅 2026-06-27

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-21._
