# VLookup

There are four pieces of information that you will need in order to build the VLOOKUP syntax:

1. The value you want to look up, also called the lookup value.

2. The range where the lookup value is located. Remember that the lookup value should always be in the first column in the range for VLOOKUP to work correctly. For example, if your lookup value is in cell C2 then your range should start with C.

3. The column number in the range that contains the return value. For example, if you specify B2: D11 as the range, you should count B as the first column, C as the second, and so on.

4. Optionally, you can specify TRUE if you want an approximate match or FALSE if you want an exact match of the return value. If you don't specify anything, the default value will always be TRUE or approximate match.


Now put all of the above together as follows:

=VLOOKUP(lookup value, range containing the lookup value, the column number in the range containing the return value, optionally specify TRUE for approximate match or FALSE for an exact match)