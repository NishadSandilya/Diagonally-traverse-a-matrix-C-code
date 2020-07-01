# Diagonally-traverse-a-matrix-C-code
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

THE EXPLAINATION FOR THE SECOND PART, THE SECOND CODE -

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

This is written without comments, sourced from geeks for geeks, also, this version is a bit easier to understand.
Let me explain - 
This method finds the total number of lines required to print all the elements diagonally until the end is reached. There is a certain pattern to this that, you have to figure out. You must have found out by now that row+colunms - 1 lines are required the required diagonals. so if its a 3X3 matrix, 5 diagonals are required to reach to the end element. 

Also, each line starts from 1 and ends at r+c-1 as shown in the code above. After that's done, we need to find the indices of the first element in each line. see the code:
the row index goes along with line-1 at each iteration, and once the max row is reached, the row is constant then, so min(r,line-1). the same goes for the column index.
this one's interesting as the column remains the same till the last row and increases after wards, so, we make this pattern, 0 till the rth row and 1, 2, 3, ....afterwards till the last column. so max(0, line-row). 

finding the count is a bit tricky though. for a square matrix, the number of elements in a line is equal to the line number till the last row, after that the elements become max_col - the_current_col. this is true for a square and a vertically extending matrix(r x c where r>c), however for a horizontally extending matrix, the rows matter while calculating the number of elements in a line. so min(line, max_column-current_col, max_row).  
