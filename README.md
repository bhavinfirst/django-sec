This is the in-progress code to parse key accounting concepts from XBRL documents, coupled with a tool that downloads the index of filings from the SEC's EDGAR, puts them into SQL, and downloads specified filings. 


The XBRL parsing is translated from VB script written by Charles Hoffman, an accountant and XBRL expert, and reliably extracts more than 50 commonly used accounting terms.

just:

import xbrl
x = xbrl.XBRL(PATH TO LOCAL XML 10-K FILING)
print x.fields #a dict of the most important values

To get any XBRL term:

x.GetFactValue(XMBL TAG, "Duration" or "Instant" (depending on if it's a year-long or snapshot value)):

By Luke Rosiak
Released under the GNU