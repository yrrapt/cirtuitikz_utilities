# CirtuiTikZ Utilities

Collection of useful definitions and utilities for use with CircuiTikZ.

The repository current contains the following definitions:

### Small Signal Models
- Common source FET (cs_ss)
- Common gate FET (cg_ss)
- Diode connected FET (dc_ss)
- Current source FET, only capacitances (is_ss)

These can be instantiated using the following syntax

	\path (0,0)  pic[] {cs_ss=diff_p};
	
where in this case 'diff_p' is the name of the FET (M prefix ommited)


### Wiring Utilities
- Loop to denote no connect when crossing a net (kinky cross)

This can be used with the following type of definition:

	\node (c) at (0,0) {};
	\node (d) at (4,0) {};
	\draw (1,1)node[circ]{} to [kinky cross=(c)--(d), kinky crosses=left](1,-1)node[circ]{};
