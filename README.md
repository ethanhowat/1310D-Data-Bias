# 1310D-Data-Bias
## Project Goal
The goal of this project is to test whether the Perspective API's toxicity ratings of comments are biased based on the length of the comments.
## Hypothesis
Longer comments (comments with at least 200 characters) will be rated by toxicity more accurately.
## Results
My hypothesis was definitely not correct according to the results of my testing. Perspective API showed very high accuracy for long, non-toxic comments and short, toxic comments. On the contrary, it had moderate accuracy for short, non-toxic comments and zero percent accuracy for long, toxic comments.

I think a large reason these results is actually do to how small the sample size that I tested was. I actually choose to include only 15 comments in my testing sample because I was having a lot of techinical difficulties when using a larger sample size, but in hind sight I think hurt the accuracy of my study.

Assuming my results are accurate regardless of my small sample size, I have a few guesses as to why the accuracy in relation to comment length might be like this.

For the high accuracy for long, non-toxic comments, I think that having a lot of words to provide context for words or phrases that might be flagged as toxic helped the API avoid flagging entire comments as toxic for including one toxic word.

I think the reason for the high accuracy in identifying short, toxic comments is because the API identifies single toxic words or phrases that make up a majority of the comment, without other clutter or conext.

I think the moderate accuracy for short, non-toxic comments is due to a lack of other words for context, or simply as filler, to mitigate the impact of one toxic word or phrase on the toxicity rating.

Finally, I am pretty confident that the 0% accuracy for long, toxic comments is due to the small sample size. I curious as to how the accuracy of the API would change for these types of comments with a larger sample size.
## Documentation
matplotlib: https://matplotlib.org/stable/index.html

NumPy: https://numpy.org/

pandas: https://pandas.pydata.org/docs/

Perspective API: https://developers.perspectiveapi.com/s/?language=en_US
