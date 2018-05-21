# getRSS
This code is the backup of [getRSS.c](http://nadeausoftware.com/sites/NadeauSoftware.com/files/getRSS.c) whose link is broken now. This file provides `2` APIs:  
	
	/* get the current resident set size, in bytes, of the current process */
	size_t currentSize = getCurrentRSS( );

	/* get the peak resident set size, in bytes, of the current process */
	size_t peakSize = getPeakRSS( );

If you use it on `Winodows`, you should link it with `psapi.lib`.  

The other thing you should pay attention is for `GetProcessMemoryInfo` and `getrusage`, the code doesn't check return value. So if you use it, I think it is a good habit to check the return value.