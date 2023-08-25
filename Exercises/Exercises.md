# Exercises 

The level of complexity is described by the number of stars next to the title - the more stars there are, the more complex is the exercise.

## 1. The RNA complementary (⭐️)
Transcription is the process in which DNA is converted to RNA. To do this, it is necessary to map each letter in a DNA sequence to its complemet `A -> U`, `T -> A`, `G -> C` and `C -> G`. Define a function that takes an input a DNA sequence and returns the RNA complementary.

## 2. The prime numbers (⭐️)
Define a function that takes as input a list of numbers and returns only those that are prime and that specifies how many they are. Call the function multiple times and check the output to be sure that it is working as expected.  

## 3. Find the GC-contnent, the individual nucleotides counts and the ATAT motif (⭐️)
In a DNA string you can have four different nucleotides: `A`, `C`, `T` and `G`. Knowing the number of each individual nucleotides and the percentage of GC-content (G **or** C nucleotides) is important. Define a function that takes as input a dictionary, with as key the name of a sequence and as value the DNA sequence and:
1. Calculates the number of individual nucleotides in each sequence 
2. Calculates the percentage of GC-content in each individual sequence 
3. Checks whether the sequence contains the motif `ATAT` and if it does it prints that the `sequence_name` has the motif.
3. Returns the percentage and the name of the sequence with the highest percentage of GC-content.
4. Prints the number of individual nucleotides in each sequence


## 4. Parse a corrupted file (⭐️⭐️)
There is a text file (*corrupted_mat.txt* in the Data folder) that is a matrix where each row in the matrix is a row in the file and the columns in the matrix are separated by  `\n `. The matrix should only have numbers, but, because of some internal errors, the matrix has been corrupted and some of the lines contain words. Write a *function* that:
1. Import the file 
2. Excludes the rows with words
3. Returns the fixed matrix as a numpy array

Use the function to check that it works properly

**HINT**: To solve the exercise, you have to acess the file, and use a *for* loop and *if* statement.

## 5. Implement an atbash cypher (⭐️⭐️)
A cypher is a way to encode messages by mapping each letter to a different one. One ancient way to do this is called `the atbash cypher`. This cypher uses as key an inverted alphabet, so that `A` becomes  `Z`,  `B` becomes `Y`. Write two functions that implements the encoding and decoding process of the cypher. 

**IMPORTANT** -> the cypher must:
1. Ignore elements in a message that are not letter (e.g. numbers or spaces)
2. Be able to take as input the message both in capital letter and lowercase.

**HINT**: To be able to solve this exercise you need to use a *dictionary* and string manipulation

## 6. Implement a Ceasar cypher (⭐️⭐️⭐️)
Another way to encode messages is through a Ceasar cypher. Here you are given a message and a key, which is a number, and the encoding is done by shifting the number in *key* places. So, if the key = 2, then `A` becomes `C`,  `B` becomes `D` and  `Z` becomes  `B` (and so on). Implement the encoding function (and as a bonus the decoding) that takes as input a message and a key (with key having as default value 3) and returns the encoded message. 

**HINT #1**: to solve it try to use a *dictionary*

**HINT #2**: to encode certain letter you will have to go back to the beginning of the alphabet. For this case, the *modulo* operator (%) is useful, which returns the remainder of the division of two numbers. 

**HINT #3**: if the *modulo* is too challenging, try with an *if* statement.

## 7. Fix the separated encoded message (⭐️⭐️⭐️)
An encoded message was written in 5 separate papers and needs to be put together into a unique sentence, in order to be able to decode the message. The only information you know is that the last letter of each sequence must correspond to the first letter of the following one. Implement a function that goes through the 5 separate strings and put them back together. There is one of these sequences that was accidentally written with a space between the letters - before adding that part to the unique sentence, remove the empty space.

**HINT #1**: to test you function you can use the following five sequences -  `AGCJDE`,  `TGRSGH`,  `EHSUTJ`,  `HFRSKA`,  `JSHGD W`. The output should be:  `TGRSGHHFRSKAAGCJDEEHSUTJJSHGDW`

**HINT #2**: to be able to solve the exercise you need to use a *while* loop.

## 8. Analysis of Taylor Swift's songs (⭐️⭐️⭐️)

Since Taylor Swift is one of the best artists of our time, we thought she deserved a spotlight in our exercises. The data presented in this exercise is collected via Spotify and it contains all of her songs/albums up until 2020, together with information about each song such as popularity and danceability. In this exercise we want you to analyse some of this data and find out more about Taylor. Who knows, you might even discover a song or two that you like? 

    IMPORTANT: To be able to complete this exercise you must have completed the statistical theory and coding tutorial

Below is a description of the dataset.

- name - Name of song
- album - Name of album
- artist - Name of artist/s involved
- release_date - Release date of album
- length - Song length in milliseconds
- popularity - Percent popularity of the song based on Spotify's algorithm (possibly the number of stream at a certain period of time)
- danceability - How suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity
- acousticness - How acoustic a song is
- energy - A perceptual measure of intensity and activity
- instrumentalness - Te amount of vocals in the song
- liveness - Probability that the song was recorded with a live audience
- loudness - Tdency o of music to be recorded at steadily higher volumes
- speechiness - Presence of spoken words in a track (if the speechiness of a song is above 0.66, it is probably made of spoken words, a score between 0.33 and 0.66 is a song that may contain both music and words, and a score below 0.33 means the song does not have any speech)
- valence - A measure of how happy or sad the song sounds
- tempo - Beats per minute

Note to Swifties: Unfortuntely the dataset does not contain the re-recorded albums (e.g. Taylor's Versions), though that might be a blessing in disguise as the 10-minute version of All Too Well would have likely skewed your statistical results. 

Using the dataset, address the following exercises: 

### Exploratory Analsysis
1. Read the csv file using a dataframe
2. What are Taylor's most popular and least popular songs?
3. Which album had the highest popularity and when was it published?
4. Which songs are the most danceable?
5. Are danceable songs more popular than accoustic ones?
6. Notice that the length of the songs is stored in milliseconds. Although accurate, those measures are not very interpretable. Figure out a way to convert the song length to minutes, then find her longest song. Furthermore, correlate the song length with a measure of popularity. Are long songs more popular?
7. Which songs are more popular, her sad songs or her happy songs?

HINT: The quickest way to understand your data is to visualize it

### Data Analysis

Now that we had a good look at the data, we might wonder, what makes a song popular? Is it its tempo, its danceability or it its length? Or perhaps is it mainly the lyrics and the songrwriting that make her songs popular?

1. Correlate different song features and find out which ones are the most closely related and how.
2. Predict the popularity of a song using its tempo, danceability and length via a linear regression. Also control for the album, as some albums are more popular than others. Feel free to include other features that you may have found useful in the previous analysis
3. Use an ANOVA to determine whether there is a statistically significant difference in popularity and speechiness across albums.

HINT: Before you run any of your analyses, make sure you follow all the appropiate data visualisation and pre-processing steps, such as checking for missing values, removing outliers and determining whether or not your data is normally distributed.

## 9. Cognitive data analysis (⭐️⭐️⭐️⭐️)
We have collected behavioural and cognitive data from 100 people as part of a study called GBIT (Great Britain Intelligence Test). The data consists in their performance in three cognitive tasks, as well as their demographics and measures of their mental health. This data are provided in two separate dataframes: `cognitive.csv` contains the results in the cognitive tasks, and `demographics.csv` contains the answers from questionnaires. The data were anonymised and a basic processing was already completed. The aim of this exercise is to properly clean the data and run some statistical tests to analyse them. 

    IMPORTANT: To be able to complete this exercise you must have completed the statistical theory and coding tutorial
 
### Data cleaning and processing

1. Import the data in the format of a `pandas` dataframes.
2. Check the column headers, shape of the dataframe and types of columns. There is a column that should be an integer and is, instead a string. Detect that column and change the variable type.
3. Currently, the index of the dataframe is not easy to interpret. Change it and replace it with the values in the `user_id`
3. Find out which columns have missing values and how many there are for each column.  If a column is more than 50% NA then drop it. Most of the analysis cannot be completed if the participants don't have demographics. So, after filtering the columns, filter the questionnaire dataframe for the remaining rows without missing values. 
4. Find out if there are duplicates in both dataframes. If there are two rows that are fully duplicated, then keep the second entry. In case of the questionnaire dataframe, if a columrown is duplicated in the  `user_id`,  `sex` and  `Residence` columns, but not the others, then drop both rows. 
5. The variable residence includes many different countries. Check how many people are from the United Kingdom and how many are from other countries. As you can see, there aren't many people from each one of the other individual countries. Replace the values in that column with `UK` for all people from United Kingdom, and `Other` for all the other countries.
5. Until now, you have worked with two separate dartaframes. But to be able to run the next steps of the analysis, you need to `merge` the two dataframes together. Merge together the dataframes based on the values in the `user_id`.

### Data analysis

1. Let's complete some descriptive statistics on the data. Check:
    - The distribution of the scores in the different cognitive tests using an histogram and boxplot. Since you have 3 different cognitive tests, try to create a unique figure with 3 subplots. 
    - If you see any outliers in the boxplot, use the `rank_inverse_transform` function explained in the lectures to remove those outliers.
    - Compare the `mean` and `median` of the cognitive scores values before and after the `rank_inverse_transform`. What do you notice?
    - Obtain the overall counts of the demographics: how many people do you have for each `sex`, `ethnicity`, `occupation`? Try to represent it using a pie chart and/or a bar chart. 
6. The `words definition` task is a language based task, so we would expect partcipants from the UK to perform better, or at least different, compared to participants from other non-english speaking countries. To verify this, we can run a **t-test**. Which t-test is the most appropriate? Check the *decision tree*.

    **IMPORTANT #1**: in order to be able to run a t-test, you need to check if the data are normally distributed. To do this, you can use of the **normality** tests explained in the stats material.

    **IMPORTANT #2**: Since you are completing multiple comparisons at once, you need to correct the p-values for multiple comparisons. How would you do it?

    Once you have completed the analysis, try to interpret the results.

7. *Age* is well-known to be associated to cognitive performance. Can you check whether there is any correlation between the age of participants and their performance in the cognitive tests? What type of correlation test should you use?

7. Another interesting thing to investigate is whether there is a difference in cognitive performance among the participants with different educations. To be able to do this, since the educational backgrounds are more than two, you need to run an **ANOVA**. Which *ANOVA* should you run?

7. Do you think we can predict the score in different cognitive tasks based on the demographics? To find out, let's build one (or more) **multiple linear regression models** that try to predict the cognitive score in one (or more) tasks. 

    **IMPORTANT**: It would be better to hot-encode the categorical variable for education and to input the age data in decades rather than as a conitnous variables. 

    Interpret the meaning of the output results.

