# Convert 8 and 10 digit OS grid refs to 6 digits in excel with a formula
an excel formula to convert 8 and 10 digit grid references to 6 digit. 

Works for formulas in a single string with no spaces, eg
NS7486320333

becomes

NS 748 203

=LEFT(A1,2)&" "&MID(A1,3,(((LEN(A1)-2)/2)+2)/2)&" "&MID(A1,(((LEN(A1)-2)/2)+2)+1,(((LEN(A1)-2)/2)+2)/2)
