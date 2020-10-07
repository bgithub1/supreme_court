# Supreme Court Politics
### The power of the Senate in determining Supreme Court social attitudes
___
This Jupyter Notebook shows the history the *political leanings* of the 31 distinct Supreme Courts since 1970. Since the U.S. Civil War, Republicans and Democrats have controlled both the presidency and the Senate.  At any time, when a Supreme Court justice leaves the court, the party of both the President and of the Senate leadership **determine the extremity of the next nominiee's politics**.  

In this workbook, I create a simple coding system in which both the presidency and the Senate receive either:
  * `+1` if they are Republican, 
  * `-1` if they are Democrat.
___

### Creating `political extremity rating` values per justice:  
1. I then apply these values to each justice, so that the judge gets:  
  * `+1` or `-1` value related to the president that nominated she/he, and 
  * `+1` or `-1` value related to the Senate leadership that confirmed the justice.


2. I add the president and Senate ratings together to create a justice's `political extremity rating`:  
  * `+2` if they are conservative,   
  * `0` if they are neutral, and   
  * `-2` if they are liberal.  


3. The values above are divided by `+2`, so each justice gets assigned a value of:  
  * `+1` if they are conservative, 
  * `0` if they are neutral, and 
  * `-1` if they are liberal.  
 
___
### Create `political extremity rating` values for each distinct court since 1970:
1. I create a `daily court composition table` in which, for each day since 1970, I list the judges that made up the Supreme Court on that day, along with the party of the president that nominated them.


2. I aggregate the `daily court composition table` into a **`distinct court composition table`** which contains **`31` rows**. Each row contains information about each distinct court.


3. For each of the **`31` rows** in the **`distinct court composition table`**, I sum the values of `political extremity rating` of each judge to get an total `political extremity rating` for each court.

4. I perform the same analysis in `3.` above, but I create a row for each of the 50 years from 1970 to 2020.
___

### Data Sources:
Court composition by president: https://en.wikipedia.org/wiki/Party_divisions_of_United_States_Congresses


List of Supreme Court Justices: https://www.supremecourt.gov/about/members_text.aspx

Senate composition by Senate: 
* https://www.senate.gov/history/partydiv.htm  
* https://www.infoplease.com/us/government/legislative-branch/composition-of-congress-by-political-party-1855-2017