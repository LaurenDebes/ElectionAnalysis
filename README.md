# ElectionAnalysis
Module 3 using Python
## Overview of Election Audit
A Colorado Board of Elections employee has given us the following tasks to complete the election audit of a recent local congressional election. The first set of tasks is regarding total candidate votes and the overall winner of the election:
   - Calculate the total number of votes cast
   - Get a complete list of candidates who received votes
   - Calculate the total number of votes each candidate received
   - Calculate the percentage of votes each candidate won
   - Determine the winner of the election based on popular vote. 
Then we were tasked with analyzing county turnouts:
   - Get a list of counties who votes
   - Calculate the percentage of votes count in each county
   - Calculate the number of votes in each county
   - Determine the county with the largest voter turnout

## Election Audit Results
**Total votes cast in congressional election:**
369,711 total votes were cast in the election. 
  
   - Steps to determine total vote count:
      - Create a variable to hold total votes, initialize it to zero
            ```
            total_votes = 0
            ```
       - Loop through each row to add votes to the total vote count
     
            ```
            for row in reader:
            total_votes = total_votes + 1
            ```
            
      - Print the count to the text file
            
**Number and percentage of total votes for each county:**
   - Jefferson County: 38,855 votes (10.5% of total vote)
   - Denver County: 306,055 votes (82.8% of total vote)
   - Arapahoe County: 24,801 votes (6.7% of total vote)
   
   The list of counties was determined by first creating a county list variable:
   ```
   county_list = []
   ```
   Then identifying counties through the following code:
   ```
   county_name = row[1]
   if county_name not in county_list:
   county_list.append(county_name)
   ```
   The number of votes per county was calculated by first creating a county_votes dictionary, then tracking the number of votes per county (first initializing the      counter to zero) through the following code:
   ```
   county_votes[county_name] = 0
   county_votes[county_name] += 1
   ```
**The percent of votes per county and which county had the largest number of votes** (Denver County) were determined through the following code:
![Screenshot 2022-04-23 134623.png](https://raw.githubusercontent.com/LaurenDebes/ElectionAnalysis/main/Screenshot%202022-04-23%20134623.png)

**Number and percentage of total votes for each candidate:**
   - Charles Casper Stockham: 85,213 votes (23.0% of total vote)
   - Diana DeGette: 272,892 votes (73.8% of total vote)
   - Raymon Anthony Doane: 11,606 votes (3.1% of total vote)
   
   The list of candidates was determined by first creating a candidate list variable:
   ```
   candidate_options = []
   ```
   Then identifying candidates through the following code:
   ```
   candidate_name = row[2]
   if candidate_name not in candidate_options:
   candidate_options.append(candidate_name)
   ```
   The number of votes per candidate was calculated by first creating a candidate_votes dictionary, then tracking the number of votes per candidate (first  initializing the counter to zero) through the following code:
   ```
   candidate_votes[candidate_name] = 0
   candidate_votes[candidate_name] += 1
   ```
**The percent of votes per candidate and which candidate had the largest number of votes** (Diana DeGette) were determined through the following code:
![candidate_code.png](https://raw.githubusercontent.com/LaurenDebes/ElectionAnalysis/main/candidate_code.png)

**Winner Information**
Diana DeGette won the election with 272,892 votes, which is 73.8% of the total vote count.

## Election-Audit Summary
This script can be simply rewritten to provide results for any election. There only needs to be a CSV (Excel) file of results and I can provide the exact same analysis. I would just need to change the code to reflect any changes in the file such as if there were a different method of organizing data into columns, I would alter the code to correspond to the correct column (e.g. our candidate list was in column 2, if it moved to column 5 the code would need to change to candidate_name = row[5] instead). The same script could be used for other election questions as well, such as yes/no votes on bond questions. We would just alter the code so it were more readable, replacing candidate name variables with something like bondvote or yes_or_no_answer. 
