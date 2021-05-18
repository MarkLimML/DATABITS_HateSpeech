# DATABITS Project
## Effectiveness of Twitch Chat Rules

## Dataset
  The dataset collected for this project was from the popular streaming platform Twitch, more specifically from the gaming genre. The data was from a total of 8 streamers, 4 of which implments chat rules and 4 who does not. These chat rules can be seen in the respective streamer's about page. The streamers with rules are Ninja, TimTheTatMan, MOONMOON, and GeekandSundry. The streamers who does not implement chat rules are Shroud, DrLupo, Summit1g, and Lirik.

  For streamers with and without chat rules. The primamry dataset contains 5 columns namely text, top_class, hate_speech, offensive_language, and neither. The text column contains a string value of the chat. The top_class contains a string value of the highest classification in the hate sonar. The hate_speech, offensive_language, and neither are float values based on the hate sonar which classifies the chat as either of the three. Hate sonar is a Python Library used mainly for the detection of hate speech. Created by Hiroki Nakayama, this library consists of a trained model aimed to recognize hate speech and offensive language.

  The datasets were loaded into a dataframe. After that the columns hate_speech, offensive_language, and neither were removed because these are unnecesary columns for this study. For the top_class column, the group decided to create another column called toxic, which is a binary representation of whether the text is not toxic (0) or toxic(1). Below is a sample table after doing these steps.

![Sample Table](/images/others/sample_table.PNG)

  The texts were then processed to lower case, remove stopwords, emotes, and streamer names. After doing this, the words are then placed inside a data frame with their respective number of occurence. Below is a sample data frame for it.

![Word Table](/images/others/words_table.png)

## For Streamers With No Rules
For streamers with no rules, the group was able to gather 1,873,772 chat lines.

#### No Pre-processing
![WordCloud No pre processing](images/norules/word_no_processing.png)

### After Pre-processing
![WordCloud after pre processing](images/norules/word_processed.png)

  For before and after pre-processing, we could see that stop words were removed and the streamer name 'shroud' was also removed from the wordcloud.

### Top 50 words
![Top 50 words](/images/norules/top_50.png)

  For the top 50 words that are frequent in the toxic chats, we can see that there are a lot of curse words such as f\*ck, sh\*t and wtf. We can also see a lot of derogatory and inaapropriate words such as fat, c\*ck, ass, gay, hell, and d\*ck.


## For Streamers With Rules
For streamers with no rules, the group was able to gather 1,311,976 chat lines.

#### No Pre-processing
![WordCloud No pre processing](/images/withrules/words_no_processing.png)

### After Pre-processing
![WordCloud after pre processing](/images/withrules/word_process.png)

  For before and after pre-processing, we could see that there exists more words inside the wordcloud for data with no pre-processing. After processing the data, we could see that the ammount of words significantly lowered. The word *bidet* stood out so the group searched why people are chatting this. It turns out that the word bidet, acoording to a reddit post[1] is a misspronounced "good day".

[1]. https://www.reddit.com/r/criticalrole/comments/dg8h58/no_spoilers_can_someone_explain_bidet_to_me/


### Top 50 words
![Top 50 words for with rules](/images/withrules/top_50.png)

  For the top 50 words that are frequent in the toxic chats, we can see that the front runners are the same with the chat with no rules these are f\*ck, sh\*t and wtf. We can also see a lot of derogatory and inaapropriate words such as damn, hell, ass, and d\*ck. 


## Merged Data

### Frequent in both rules and without rules chat
![Frequent Words](/images/merge/words_frequent)


### Top 50 words in both rules and without rules chat comparison
![Top 50 words for with rules](/images/merge/top_50.png)
  
  In the top 50 words for merged data, we can see that the top 5 words are the curse words, derogatory words and innapropriate words. Chat with rules and chat without rules seems to have similar toxic words they receive, however the quantity varies significantly.

### Conclusion
  
  In this data project, we planed to know wheter having chat rules in the popular streaming platform Twitch more specifically in the gaming section. Based on the gathered data, streamers who implements chat rules and those who does not, encounters the same toxic words such as f\*ck, sh\*t, wtf, c\*ck, hell, b\*tch and more. However the quantity of toic words the streamers receive varies a lot. When comparing chat with rules and without rules, the frequency of toxic words a streamer receives for chat without rules are signicantly higher. With that we can conclude that imposing chat rules can lower the frequency of the toxic word a streamer could receive.
