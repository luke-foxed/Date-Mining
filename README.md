# Date-Mining

This notebook combines Pandas, RegEx and the FuzzyWuzzy library to import, clean and extract dates from a CSV file. 

A variety of date formats and seperators exist within the date that must be account for with RegEx, such as:
- 04/20/2009; 04-20/09; 4/20/09; 4/3/09
- Mar-20-2009; Mar 20, 2009; March 20, 2009; Mar. 20, 2009; Mar 20 2009;
- 20 Mar 2009; 20 March 2009; 20 Mar. 2009; 20 March, 2009

FuzzyWuzzy on the other hand, is used to correct mispelled months by using Levenshtein Distance to compare spelling differences.

The final output of this notebook contains columns for `Day`, `Month` and `Year` - as well as a `Date` column which combines these three.

_(Lines that are missing months/days are defaulted to 'January' and '01' respectively)_
