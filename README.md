# Election_Analysis

## Project Overview
A Colorado Board of Elections employee has given the following tasks to complete the election audit of a recent local election.

1. Calculate the total numbre of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Challenge Overview
A Colorado Board of Elections employee has given the following tasks to complete the election audit of a recent local election.

1. The voter turnout for each county
2. The percentage of votes from each county out of the total count
3. The county with the highest turnout
4. All the previous information saved in a text file named "election_results.txt"

## Resources
- Data Source: election_results.csv
- Software: Python 3.9.12, Visual Studio Code 1.72.0

## Election-Audit Results

The analysis of the election show that:
- There were "369,711" votes cast overall in the election. It was counted with by counting how many rows of information there were in the csv file. While the file was being read the counter for the total votes was added 1 for each row until there were no rows left to be read.

![total_votes](https://user-images.githubusercontent.com/110573146/196782360-a9c9af89-cd83-4b83-a354-76c4a90d8732.png)

- By using an if funciton and comparing the name of the candidate given in each row with an empty list (that at the start was empty) that if the name was not in the list it would add it if it was already in the list it would not add it. The candidates were:
    -  Charles Casper Stockham
    -  Diana DeGette
    -  Raymon Anthony Doane
- ***The same exact method was used to identify all the counties that voted for the election.*** The countes were:
    - Jefferson
    - Denver
    - Arapahoe 

![candidates_counties](https://user-images.githubusercontent.com/110573146/196784267-2b31ece9-6805-40e7-b6a8-138ebca9e0bb.png)

- For both the candidate results and the counties turnout count results the method was the same as seen in the previous figure and in the next, first for each row the name was obtained after with the help of two dictionaries (one for the candidate and another for the counties) and with the name as a key (candiddate or county) the vote count was added by 1 for each vote either for that candidate or that came from that county. Once the votes are counted a simple percentage formula is applied to get each of the percentages of the total votes taht came from each county and that each candidate got. The formula is a division of the count of votes of each county/candidate divided by the total amount of votes and multiplied by 100. Finally, after gathering all the data it was presented in a nice and easy to read format that is printed to the terminal and saved in the txt file. The candidates results were:
    - Charles Casper received 23.0% of the vote with 85,213 number of votes.
    - Diana DeGette received 73.8% of the vote with 272,892 number of votes.
    - Raymon Anthony Doane received 3.1% of the vote with 11,606 number of votes.
- The counties results were:
    - Jefferson gave a 10.5% of the participation with 38,855 number of voters.
    - Denver gave a 82.8% of the participation with 306,055 number of voters.
    - Arapahoe gave a 6.7% of the participation with 24,801 number of voters.

 ![counties_votes_results](https://user-images.githubusercontent.com/110573146/196790911-4a156196-8807-4c34-bb09-ec9e7821fba4.png)

![candidate_votes_results](https://user-images.githubusercontent.com/110573146/196790997-4da37cc3-116d-4d71-b780-d01096e0194d.png)

- The winner of the election and the county with the largest turnout of votes were elected comparing the total final count saved in the dictionary for each option, it was done with an if statement that used a logical operation of comparisson between the quantities, with help of the "><" symbols. The candidate that won the election was:
    - Diana DeGette, who received 73.8% of the vote with 272,892 number of votes.
- The county with the largest turnout of votes of the election was:
    -  Denver, that had 306,055 voters and represents the 82.8% of the total participation of the election.

![candidate_winner](https://user-images.githubusercontent.com/110573146/196797008-882acb3c-0bed-40ec-84a6-07f67513a7f6.png)

![county_winner](https://user-images.githubusercontent.com/110573146/196797084-79f691c8-23b9-4759-87bd-0848a31eb375.png)

## Election-Audit Summary

1. The first reccomendation to using this code again for another election would be to proportionate another csv file with much more election information, maybe even a presidantial election, the required changes are: 
    - change the path of the file to read to where the csv file will be saved in the computer.
    - change the path of where the txt file with the results will be saved.
    - if possible make the new csv file format coincide with the format of the file used for this analysis, if not make the adjustments necessary to the code to load to save the correct data, for example the candidate name or the county.

2. The second option to reusing or modifyng the code is to use it to identify the preference of candidates of each county, so we can see more tendencies and get more information about the election. For this it would be necessary to:
    - create another dicitonary that will hold as key all the combinations of candidate and county.
    - to create the list and the keys we will use the information already gathtered from the challenge and use the same method of adding it if it is not already in there.
    - just a normal counter it will add 1 to the count each time it appears and save it as value in the dictionary.
    - once all the csv file has been read the dictionary and its values is printed and read, here we will see the tendencies of each county for each candidate and how they affect the election.
