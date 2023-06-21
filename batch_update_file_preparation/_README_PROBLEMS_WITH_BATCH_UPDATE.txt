When export from Excel lines end with CR LF
When use this in batch import set the Record Delimiter to Line Feed NOT Carriage Return (even though that option mentions it is used for TSV!)

Export from Excel to TSV tends to wrap text in " and replace " by "" so we manually modify:
 global replace "" by _QUOT_
 global replace " by nothing
 global replace _QUOT_ by "

Always be sure to check the total records changed equals number of rows in TSV (minus 1) in case the update aborted halway through

Seems some characters cause batch update to fail e.g. 
ü - we replace by u
ø - we replace by o

This means we are NOT truly reverting to the original data.

