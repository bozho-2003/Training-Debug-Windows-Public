## About Scenarios
- 第3天
	- About Crash
		- How to debug Access Violations?
		- How to debug Heap Corruption?
		- How to debug Stack Corruption?
	- About Hang
		- Common hang scenarios
			- Wait for Lock
			- Wait for Web Services
			- Wait for DB
		- How to debug a Spinning Thread?
	- About Leak
		- GFlags
		- How to debug a Native Memory Leak?
		- Finding COM Leaks Using Extensions
		- VMMap
		- RAMMap
		- LeakTrack extension
	- About HighCPU
		- Live Debug with HighCPU
		- Dump Analysis with HighCPU
		- Common HighCPU scenarios
			- Regex
			- Parallel race
			- Blank loop
			- GC
	- [CrashMe Project](http://windbg.info/apps/46-crashme.html)
		- 01-breakpoint
			- Tools: [WER Dump](https://docs.microsoft.com/zh-cn/windows/desktop/wer/wer-settings)
			- Tools: [Procdump](https://docs.microsoft.com/en-us/sysinternals/downloads/procdump)
			- EventLog
			- Dump first check
			- `!analyze -v`
		- 02-asm-int-3
			- Faulting IP
			- Error Code
		- 03-raise-exception
			- kernelbase!RaiseException
		- 04-throw
			- `.dump /ma C:\test.dmp`
			- `kP`
			- `dd` <Exception Object>
		- 05-stackoverflow
			- [`windbg -I`](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/windbg-command-line-options)
			- [enabling-postmortem-debugging](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
			- [How to disable or enable Dr. Watson for Windows](https://support.microsoft.com/en-us/help/188296/how-to-disable-or-enable-dr-watson-for-windows)
			- [`kd`](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/k--kb--kc--kd--kp--kp--kv--display-stack-backtrace-)
			- `uf <Address>`
		- 06-Division-By-NULL
		- 07-StackOverflow-with-recursion
		- 08-Nested-Exceptions
		- 09-Access-Test-Variable
			- Locals Window 
		- 10-check-for-debugger
		- 11-Enter-Critical-Section
		- 12-test-Calling-Conventions
		- 13-Invalid-Handles
		- 14-set-last-error
		- 15-HeapAlloc
		- 16-HeapDealloc
	- Demo
		- [Crash](https://msdn.microsoft.com/library/windows/desktop/ee416349)
		- [Hang](https://blogs.msdn.microsoft.com/benjaminperkins/2013/01/08/debugging-a-hung-application-with-windbg/)
		- [Hang2](https://blogs.msdn.microsoft.com/msdnts/2006/11/24/how-to-debug-application-crashhang-in-production-environment/)
		- [Native Memory Leak](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/using-umdh-to-find-a-user-mode-memory-leak)
		- [Managed Memory Leak](https://blogs.msdn.microsoft.com/paullou/2011/06/28/debugging-managed-code-memory-leak-with-memory-dump-using-windbg/)
		- [CPU High](https://blogs.msdn.microsoft.com/ntdebugging/2008/05/15/how-to-track-down-high-cpu-in-user-mode-applications-a-live-debug/) 
			- `!runaway`
	- Scripts: [pykd](https://github.com/wu-wenxiang/Tool-Windbg-Pykd-Scripts)
	- Tools: [DebugDiag](https://www.microsoft.com/en-us/download/details.aspx?id=49924)
		- Demo: [How to use the Debug Diagnostics tool to troubleshoot a process that has stopped responding in IIS](https://support.microsoft.com/en-us/help/919792/how-to-use-the-debug-diagnostics-tool-to-troubleshoot-a-process-that-h)
		- Demo: [How to use the Debug Diagnostics Tool to troubleshoot high CPU usage by a process in IIS](https://support.microsoft.com/en-us/help/919791/how-to-use-the-debug-diagnostics-tool-to-troubleshoot-high-cpu-usage-b)
