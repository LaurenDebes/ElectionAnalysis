# ElectionAnalysis
Module 3 using Python
## Overview of Election Audit
A Colorado Board of Elections employee has given us the following tasks to complete the election audit of a recent local congressional election. The first set of tasks is regarding total candidate votes and the overall winner of the election: 
    * Calculate the total number of votes cast
    * Get a complete list of candidates who received votes
    * Calculate the total number of votes each candidate received
    * Calculate the percentage of votes each candidate won
    * Determine the winner of the election based on popular vote. 
Then we were tasked with analyzing county turnouts:
    * Get a list of counties who votes
    * Calculate the percentage of votes count in each county
    * Calculate the number of votes in each county
    * Determine the county with the largest voter turnout

## Election Audit Results
Total votes cast in congressional election:
    * 369,711 total votes were cast in the election. 
        * Steps to determine total vote count:
            * Create a variable to hold total votes, initialize it to zero
            ```
            total_votes = 0
            ```
            * Loop through each row to add votes to the total vote count
            ```
            for row in reader:
            total_votes = total_votes + 1
            ```
            * Print the count to the text file
            
Number and percentage of total votes for each county:
     * Jefferson County: 38,855 votes (10.5% of total vote)
     * Denver County: 306,055 votes (82.8% of total vote)
     * Arapahoe County: 24,801 votes (6.7% of total vote)
     
     The list of counties was determined by first creating a county list variable
     ```
     county_list = []
     ```
     Then identifying counties through the following code:
     ```
     county_name = row [1]
     if county_name not in county_list:
     county_list.append(county_name)
     ```
    The number of votes per county was calculated by first creating a county_votes dictionary, then tracking the number of votes per county (first initializing the     counter to zero) through the following code:
    ```
    county_votes[county_name] = 0
    county_votes[county_name] += 1
    ```
    The percent of votes and which county had the largest number of votes (Denver County) were determined through the following code:
    ![Screenshot 2022-04-23 134623.png](https://raw.githubusercontent.com/LaurenDebes/ElectionAnalysis/main/Screenshot%202022-04-23%20134623.png)

    

## Summary
The analysis of the election show that:
- There were "x" votes cast in the election.
- The candidates were:
    - Candidate 1
    - Candidate 2
    - Candidate 3
- The candidate results were:
    - Candidate 1 received "x%" of the vote and "y" number of votes.
    - Candidate 2 received "x%" of the vote and "y" number of votes
    - Candidate 3 received "x%" of the vote and "y" number of votes.
- The winner of the election was:
    - Candidate (1, 2, or 3), who recieved "x%" of the vote and "y" number of votes.

## Challenge Overview

## Challenge Summary
