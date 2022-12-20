# election_Analysis

## Election Audit Project Overview

A Colorado Board of Elections employee, named Tom, had given me the following task.

1. Calculate the Total number of votes cast
2. Get a  complete list of candidates who received votes
3. Need Total number of votes each candidate received
4. Get Percentage of votes each candidate won
5. Determine the winner of the election based on popular vote
6. Determine which country had the most votes
7. Show how many votes per county
8. Show percentage of votes per country

## Resources
-Data Source: election_results.csv
-Software: Python 3.9.13 and Visual Studio Code 1.74.1

## Election-Audit Results

### There were 369,711 votes cast in the election!

1. I used the following

* I set the code starting at 0 and then added to the total vote counts as it read through the whole of the date using 
* total_votes += 1

### Breakdown of County Votes and Vote Percentage 

1. I used Python math with the following formula and also to format the data in a view that was more pleasant to the eyes.

*  Vote count formula after retrieving the county names
*  votes = county_votes[county_name]
*  Vote percentage formula
        vote_percentage = float(votes) / float(total_votes) * 100
        county_results = (
            f"{county_name}: {vote_percentage:.1f}% ({votes:,})\n")
2. Denver county received 306,055 which was 82.8% of the total votes.
3. Jefferson county received 38,855 votes for 10.5% of the total votes
4. Arapaho county received 24,801 votes for 6.7% of the total votes.

### County with the largest Votes

1. I used the following formula to get largest votes.  using if statement and greater then statements to bring out the largest county.
    * if (votes > largest_count) and (vote_percentage > largest_percentage):
            largest_count = votes
            largest_county = county_name
            largest_percentage = vote_percentage
2. Denver was the county with the largest vote count
 
### Breakdown of Candidate Votes and Vote Percentage 

1. Same process was used here as with counties.  Find all the candidate names, formula to calculate count and percentage.
2. Charles Casper Stockholm received 23.0% of the votes for 85,213 total votes
3. Diana DeGette received 73.8% of the votes for 272,892 total votes
4. Taymon Anthony Doane received 3.1% of the votes for 11,606 total votes


### Which Candidate Won?

1. The following formulate used to determine election winner, votes, and vote percentage
* votes = candidate_votes[candidate_name]
* vote_percentage = float(votes) / float(total_votes) * 100
* candidate_results = (
    * f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")
2. Diana DeGette was declared the winner winning 73.8% of the total votes which was 272,892 votes.

## Election-Audit Summary

As you can see we took a very large amount of data and simplified it to show the end results.  It would be very easy to take the entire state using the script to calculate total state results.  Of course, we would have to include text for a complete state vs counties.  We could also take this script and use for county elections by using cities instead of counties.  We could do a national election results using states vs counties and get a national breakdown.

I believe we could also use this script for a national elections.  We would just have to adjust the coding to accommodate the type of election.  For example you might want to know Senators or Congress winners/losers by country and by state. Also could use this to look at presidential elections show show wins and losses by State or county.   

We can add lots of things like demographics into the script if data can be provided.  Gives a quick summary of election results or even more details if needed.  More data helps us understand why we get the winning candidates.
