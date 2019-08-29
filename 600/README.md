# SECTION 600 Reverse Engineering 
 
## Note:

​The following tasks requires the REMWorkstationVM to be installed on your 
machine. It is available on the N5 google drive share

(​https://drive.google.com/open?id=0B9BxiubYy0ibOEc2STR5S1J4aUE​). 

See Appendix C for a reverse engineering example. 

Estimated Time to Complete:  1 week. 

### 600.1

1. From C:\Users\REM\Desktop\Malware\day1 extract brbbot.zip. a. password : 
malware

2. Place brbbot.exe in your %AppData% directory.

3. Create a shortcut to this executable on your desktop. 

4. Modify the shortcut so that it runs with full admin privileges.

5. Run the ​strings2 ​ command on the executable to see the embedded strings. 
It is recommended that you pipe the output to a file. a. strings2  brbbot.exe>
brbbot.txt I. From the strings alone can you characterize the executable?


### 600.2

Open the executable in PeStudio. I. By examining the indicators, import table,
and strings can you gain further insight into the malicious  functionality of
brbbot.exe? 

### 600.3

Recall that brbbot.exe created a file brbconfig.tmp. The contents of the file 
are unreadable because they are encrypted. One approach to discovering the 
content of the file is to set a breakpoint on the instruction that reads the 
file from disk and follow the buffer that hold the contents of the file in 
hopes of finding where it is decrypted. 

I. Discover the decrypted contents within  brbconfig.tmp. 

To do this open brbbot.exe in x64dbg and run the command; SetBPX [name of API 
call] 

Once this is done let the debugger run. It will stop once it encounters the 
API call specified above. Continue stepping until you have discovered the 
decoded contents of the file. 

#### HINTS:

1. Recall the windows calling convention on x64.
2. The registers and their values are shown in the right hand panel.
3. One can see all handles being used by the process via the handle tab on the
top right. Make sure to right click and refresh when in that tab.
4. You can run to user code when debugging with Alt+F9 or by going to the 
Debug Tab.
5. You can also run to selection by highlighting the line you would like to
run to and pressing F4(or under Debug click ​run until selection ​ ).


## strings2 getdown.exe output

```s
!This program cannot be run in DOS mode.
$
PRich
.text
`.rdata
@.data
.pdata
@.reloc
L$xD
D$XH
D$`H
D$PH
D$HH
D$pE3
D$@H
t$8H
t$0E3
t$(H
D$ph
t$H+
T$pA
D$XE3
T$`H
D$PH
D$HH
D$0H
D$@H
D$(H
D$
L
L$PL
D$XH
T$`3
D$hH
8csm
@
=
\$0H
\$0H
\$0H
WATAUAVAWH
D$0H
D$
L
t$(L
D$8H
|$
H;
\$(H
\$0L
D$8H
\$pH
t$xH
@A_A^A]A\_
t$
WATAUH
<vGI
f93t
L$@@
L$0H
T$@H
A]A\_
WATAUAVAWH
y8M+
IcqHI
L$0I
D$(I
D$(I
t;3
IcqHH
;7sUH
D;+t1
D$HD
\$@I
A_A^A]A\_
\$0H
l$8H
t$@H
;
w
;"u
3
<
w
H
\$0H
t.Hc
\$@H
l$HH
t$PH
x
ATAUAVH
l$`M
;"u6
<
tG<
tC
\$@H
l$HH
t$PH
|$XH
A^A]A\
t$
WH
D$HL
L$@E3
Hct$@H
s\HcL$HH
D$HL
L$@H
\$@H
\$PH
t$XH
x
ATH
fD9
t
fD9#u
fD9#u
d$8H+
d$0H
d$(L
d$8L
d$0D
l$(H
\$PH
l$XH
t$`H
|$hH
ATAUAVH
B1
D
fD9t$b
D$hH
B0
D
tEHc
A^A]A\
\$0H
\$0H
\$0H
\$0H
L$0H
L$0H;
H;=J
\$8H
D$0A
L$8D
\$8L3
\$@H
u&Hc
\$0H
t$8H
|$@H
\$0H
l$8H
t$@H
\$0H
t$8H
|$@H
\$0H
WATAUAVAWH
|$`3
|$(H
}*Hc
\$hH
t$pH
0A_A^A]A\_
UWATH
L$t3
\$pH
\$HH
T$@I
T$@H
L$`H
L$0H
L$XL
L$(H
L$
3
|$tH
A\_]
T$`L
\$@H
l$HH
t$PH
D$`H
;
t+
ATAUAVH
V
H;
\$@H
t$HH
|$PH
A^A]A\
\$0H
HcH<H
LcA<E3
t"M+
@SUVWATAUAVH
D$HA
tbL;
L$0A
D$8H
L$
A
L$HH3
PA^A]A\_^][
d$
L
L$
A
D$(D
D$
H
\$PH
t$XH
\$0H
l$8H
t$@H
x
UH
D$p
H
D$(H
D$8H
\$0H
D$(L
L$pD
D$8H
\$0H
D$(L
L$pA
\$0H;
L$0H;
\$8H
L$
3
UVWATAUH
D$8H
D9d$
D$&8\$&t-8X
t18Y
L$8H3
@A]A\_^]
`
AUH
\$@H
t$HH
|$PL
d$XH
t7SH
x
ATH
l$8H
t$@H
|$HH
\$0H
x
ATH
l$8H
t$@H
|$HH
\$0H
x
ATH
l$8H
t$@H
|$HH
\$0H
\$0H
t$8H
fffffff
D
@H
L
L
T
(H
ffff
fffffff
ffff
@UATAUAVAWH
l$@H
@88t
|$@H
l$(H
!t$(H!t$
A
L$(E
\$@H
t$(H
L$8D
L$(H
D$(H
D$
A
A_A^A]A\]
L$PI
L$PD
D$0H
\$pI
@UATAUAVAWH
l$0H
\$0H
d$(H
A_A^A]A\]
L$@A
L$@D
D$(H
\$pH
t$xH
\$0H
t$8H
\$0H
\$0H
t$8H
tfSH
H;)N
KXH;KN
K`H;AN
K
H;
(H;
K0H;
K8H;
K@H;
KHH;
KhH;
KpH;
KxH;
H;tM
H;gM
CorExitProcess
mscoree.dll
runtime
error
TLOSS
error
SING
error
DOMAIN
error
R6033
-
Attempt
to
use
MSIL
code
from
this
assembly
during
native
code
initialization
This
indicates
a
bug
in
your
application.
It
is
most
likely
the
result
of
calling
an
MSIL-compiled
(/clr)
function
from
a
native
constructor
or
from
DllMain.
R6032
-
not
enough
space
for
locale
information
R6031
-
Attempt
to
initialize
the
CRT
more
than
once.
This
indicates
a
bug
in
your
application.
R6030
-
CRT
not
initialized
R6028
-
unable
to
initialize
heap
R6027
-
not
enough
space
for
lowio
initialization
R6026
-
not
enough
space
for
stdio
initialization
R6025
-
pure
virtual
function
call
R6024
-
not
enough
space
for
_onexit/atexit
table
R6019
-
unable
to
open
console
device

R6018
-
unexpected
heap
error
R6017
-
unexpected
multithread
lock
error
R6016
-
not
enough
space
for
thread
data
R6010
-
abort()
has
been
called
R6009
-
not
enough
space
for
environment
R6008
-
not
enough
space
for
arguments
R6002
-
floating
point
support
not
loaded
Microsoft
Visual
C++
Runtime
Library
<program
name
unknown>
Runtime
Error!
Program:
GetProcessWindowStation
GetUserObjectInformationW
GetLastActivePopup
GetActiveWindow
MessageBoxW
USER32.DLL
HH:mm:ss
dddd,
MMMM
dd,
yyyy
MM/dd/yy
December
November
October
September
August
July
June
April
March
February
January
Saturday

Friday
Thursday
Wednesday
Tuesday
Monday
Sunday
HH:mm:ss
dddd,
MMMM
dd,
yyyy
MM/dd/yy
December
November
October
September
August
July
June
April
March
February
January
Saturday
Friday
Thursday
Wednesday
Tuesday
Monday
Sunday

(((((
H

h((((
H

H

!"#$%&'()*+,-./0123456789:;<=>?@abcdefghijklmnopqrstuvwxyz[\]^_`abcdefghijklmnopqrstuvwxyz{
|}~

!"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`ABCDEFGHIJK
LMNOPQRSTUVWXYZ{|}~
CreateProcessA
GetTempFileNameA
IsDebuggerPresent

GetTempPathA
KERNEL32.dll
URLDownloadToFileA
urlmon.dll
GetCommandLineA
GetStartupInfoW
TerminateProcess
GetCurrentProcess
UnhandledExceptionFilter
SetUnhandledExceptionFilter
RtlVirtualUnwind
RtlLookupFunctionEntry
RtlCaptureContext
GetProcAddress
GetModuleHandleW
ExitProcess
DecodePointer
WriteFile
GetStdHandle
GetModuleFileNameW
RtlUnwindEx
GetModuleFileNameA
FreeEnvironmentStringsW
WideCharToMultiByte
GetEnvironmentStringsW
SetHandleCount
InitializeCriticalSectionAndSpinCount
GetFileType
DeleteCriticalSection
EncodePointer
FlsGetValue
FlsSetValue
FlsFree
SetLastError
GetCurrentThreadId
GetLastError
FlsAlloc
HeapSetInformation
GetVersion

HeapCreate
QueryPerformanceCounter
GetTickCount
GetCurrentProcessId
GetSystemTimeAsFileTime
LeaveCriticalSection
EnterCriticalSection
LoadLibraryW
GetCPInfo
GetACP
GetOEMCP
IsValidCodePage
HeapFree
Sleep
HeapSize
LCMapStringW
MultiByteToWideChar
GetStringTypeW
HeapAlloc
HeapReAlloc


abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ


abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ

```


## PREAMBLE

​To be used as an example to illustrate concepts.  The output below is from
running strings2 on the executable.  This is a common technique used as the 
first step in reverse engineering to build an output of all strings within the 
binary of an executable.  

The strings included here can be function calls, which can give you an idea of
functionality the program has.  One example would be seeing functions related 
to network programming, which would lead to the conclusion that the program is 
talking to something else over the network.  Another example would be seeing 
functions related to writing to the memory of another process. 

The strings can also be strings that were hard coded into the program by the 
developer.  This can include an ip address and a port that can give you an 
idea of where communications are going to.  It can also include text that the 
program is looking for as input to user fields. 

Look at the output below, and after that you will see examples of information
that was deduced based off of the output. 


## PREAMBLE RELEVANT STRINGS:

Above is the output from strings2 on an executable. The Following are some 
conclusions you can draw from these strings: 
 
● CreateProcess: Spawn a new process. 
● GetProcessWindowStation​ : ​Retrieves a handle to the current window station 
for the calling process. 
● GetUserObjectinformation: Retrieves information about the specified window
station or desktop object 
● GetLastActivePopup: Determines which pop-up window owned by the specified 
window was most recently active.
● GetTempFileName: Creates a name for a temporary file. If a unique file name 
is generated, an empty file is created and the handle to it is released; 
otherwise, only a file name is generated. 
● GetTempPath: Retrieves the path of the directory designated for temporary 
files. 
● URLDownloadToFIle: Downloads bits from the Internet and saves them to a 
file. 
● GetCommandLine: Retrieves the command-line string for the current process.
● WriteFile
● IsDebuggerPresent 
● List of all months and date format strings: HH:mm:ss dddd, MMMM dd, 
yyyy MM/dd/y


## PREAMBLE  DEDUCTIONS:

From the strings highlighted above one could argue the following: 

1. The executable is malicious due to the fat that it checks if a debugger is 
present (IsDebuggerPresent). Malware authors know that those trying to figure
out how their software works often do so with the aid of a debugger to follow
execution and analyze dynamically in greater depth. Thus, malware authors
often use this API call in an attempt to thwart reverse engineering efforts by
causing their software to behave differently in the presence of a debugger.

2. The executable likely drops a file on disk with metadata about the windows 
opened in the context of its own process (CreateProcess,
GetProcessWindowStation​, GetUserObjectinformation, GetLastActivePopup,
GetTempFileName, GetCommandLine, WriteFile). This file and its information can 
be used by the malicious software in a future instance or possibly be sent 
back to the author. 

3. The executable reaches over the internet to retrieve information from a 
malicious server and drops it on disk (URLDownloadToFIle). This can be used in
many ways, one of them being C2 (Command and Control).
