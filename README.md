Quick and dirty port of 4.3BSD timed to linux.
Required in order to sync the clocks of several ancient System V UNIX installations (backporting NTP was deemed unfeasible / next to impossible).
This port is 32bit only and it will never make it to the 64bit world. TSP is bound to 32bit time_t and this is not going to change, ever.
