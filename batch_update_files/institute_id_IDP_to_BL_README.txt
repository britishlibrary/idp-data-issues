README FILE CREATED BY SCRIPT:  http:/localhost/BRITISH_LIBRARY/IDP/4D/Test 4D application localhost/scripts/PHP/create_batch_update_files_based_on_SQL.php

THIS AND ASSOCIATED BATCH UPDATE FILES CREATED :  2023-04-26 03:08 PM
(WARNING: based on SQL access to Dev data - is possible that data was out of date compared to Live)


INSTRUCTIONS FOR USE
This README created in conjunction with two files suitable for use in 4D batch update (Admin > Import Update Data)
The reverse file can be used to revert to current values: D:/British Library/bl github group/bl_github_clones/idp-data-issues/batch_update_files/institute_id_IDP_to_BL_REVERSE.txt
The actual update file is initially identical to that: D:/British Library/bl github group/bl_github_clones/idp-data-issues/batch_update_files/institute_id_IDP_to_BL.txt
To use for batch updates this TSV should be edited (all but the first col which is the unique value of the record you want to edit).
Once data is ready to perform the batch update in 4D
- Run Admin > Import Updata Data.
- Select table (Items in this case).
- Select the columns (see top row of TSV file) in order using Available Fields: > Add (continue if hit debug).
- Select Record Delimiiter to be the 2nd selectable item (Line Feed... NOT the Carriage Return option even though that mentions tab delimited text files!).
- Click Update and select the (edited) file D:/British Library/bl github group/bl_github_clones/idp-data-issues/batch_update_files/institute_id_IDP_to_BL.txt
If you need to roll back then run a similar update but using the (unedited) file: D:/British Library/bl github group/bl_github_clones/idp-data-issues/batch_update_files/institute_id_IDP_to_BL_REVERSE.txt
Can check updated values using e.g. 4D's Records > Data Explorer


OPTIONS TABLE:

	<h4>Batch run info</h4>
	<table border='1'>
	<tr><td>Current hard-coded run number:</td><td><span style='color:red;'><b>1</b></span></td></tr>
	<tr><td>Description:</td><td><span style='color:red;'>[Items] records with `Institute id` value IDP to be flipped to value BL</span></td></tr>
	<tr><td>Table to modify:</td><td><b>Items</b></td></tr>
	<tr><td>SQL:</td><td><b>SELECT  A.`Pressmark`, A.`Institute id` FROM Items AS A WHERE A.`Institute id` = 'IDP' ORDER BY A.`Pressmark` ASC LIMIT 5000</b></td></tr>
	<tr><td>Batch update TSV file (for applying updates):</td><td><b>D:/British Library/bl github group/bl_github_clones/idp-data-issues/batch_update_files/institute_id_IDP_to_BL.txt</b></td></tr>
	<tr><td>Batch update TSV file (for reverting to current values):</td><td><b>D:/British Library/bl github group/bl_github_clones/idp-data-issues/batch_update_files/institute_id_IDP_to_BL_REVERSE.txt</b></td></tr>
	<tr><td>Batch update readme file (with info on use/source):</td><td><b>D:/British Library/bl github group/bl_github_clones/idp-data-issues/batch_update_files/institute_id_IDP_to_BL_README.txt</b></td></tr>
	</table>
	<hr/> 
