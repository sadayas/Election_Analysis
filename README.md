# Election Analysis

## Project Overview
With the use of our resources, we will use the election audit results to determine the voter turnouts, percentage of votes, and highest voter turnout for all the counties.

## Challenge Overview

1. How many votes were cast in this congressional election?
    - Total of 369,711 Votes
2. Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
    - Jefferson: 10.5% with (38,855 votes)
    - Denver: 82.8% with (306,055 votes)
    - Arapahoe: 6.7% with (24,801 votes)
3. Which county had the largest number of votes?
    - Denver 
4. Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
    - Charles Casper Stockham: 23.0% with (85,213 votes)
    - Diana DeGette: 73.8% with (272, 892 votes)
    - Raymon Anthony Doane: 3.1% with (11,606 votes)
5. Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
    - Diana Gette: with 272,892 and 73.8% of the votes.
 
![This is an image](https://github.com/sadayas/Election_Analysis/blob/main/Resources/election_challenge_results.png)

## Challenge Summary

During the process of reading and developing the code, we were able to determine the winner of the election. 

` if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage`

The use of this code, allowed us to determine the candidate with the most votes, and the win percentage.  But the ease of the use, and being able to plug in information, created a versatile script. In which we were able to also determine the data of the voter turnover for the counties in the election. As seen below:

`if (county_votecount > topcounty_count) and (county_percentage > topcounty_percentage):
            topcounty_count = county_votecount
            topcounty_percentage = county_percentage
            top_county = county_name`

With this script, we can easily loop through all the data, and find important details.  We can even extract the data to help determine specific results.  For example, in this code: we were able to search for the counties names and see if any counties were missing from our list.

        county_name = row[1]
        
        if county_name not in county_votes:

            county_list.append(county_name)
            
We used the script to loop through the rows, while finding out which counties voted, and if there was missing values - our script was able to find and add the data for us.

 With the use of this script, we will be able to audit any election.
