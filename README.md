Analysis and Documentation

Decide how you would like to test the Perspective model for bias. Document your methods, all queries that you make to the API, and all scores received.

I am testing the perspective model for bias through faulty spelling, but also if the use of profanity gives a more toxic score even if the comment is not toxic at all, if the profanity boosts the score. Lastly, I wish I could look at what the comments are in response to, like if they are a reply, a quote tweet, targeted at someone, or completely independent, but that is not in the scope of this tool. 

Analyze your results. If you looked at performance on the labeled dataset, how did false positive rates and false negative rates compare against different types of content? Were there any cases where you disagreed with the labels? Were there any trends that you noticed in the model scores? What about any original queries that you submitted?

The main results I was looking at was testing different variations of toxic comments to see how they would be scored, this changed with how I spelled curse words and words that were toxic to me. I tested it in multiple ways, and in some cases the toxicity would change if I just added a space at the end of the sentence, which I would need to see the coding behind the algorthm to fully understand why that happens. I was struggling to find cases of false positives because most of the cases I saw were toxic online comments, but there were a lot false negatives that I saw that were toxic but did not get a high toxic score at all or they weren't labeled as toxic. In the original queries that I submitted I was once again playing around with certain words and things that were changing the scores, which I talked about above. Some of the biggest false negatives were ones where there were very very vulgar words that were spelled incorrectly onpurpose with bad intent that received non toxic ruling but definitley should have been. I look at the spelling in those scenarios as the main reason why.



Write a few paragraphs, either in the README or in the notebook, reflecting on what you have learned, what you found, what (if anything) surprised you about your findings, and/or what theories you have about why any biases might exist, if you find they exist. You can also include any questions this assignment raised for you about bias or machine learning. 

I have learned that this algorithm for checking for toxicity in comments is actually pretty accurate, and most of the time the scores were labeled more toxic than I would think, which is not a problem in my mind. There were some instances that a comment had a crazy high toxic score, but in my mind was not that damaging of a comment, the use of curse words caused a lot of these cases, but I don't see all uses of curse words as toxic, maybe a label of "NSFW," or "not safe for work," could be more accurate in those cases. I found that when words weren't spelled correctly in a toxic comment it lowered the toxic score. I was struggling to understand some of the identity_hate scores that were counted as identity_hate, and don't really understand the criteria for that label after playing around a bit. The other scores were a bit more set in stone in terms of them making sense based on the comment. Some questions this assignment raised for meabout bias and machine learning is mainly surrounding whether or not the machine understands other languages, or if someone puts a greek character that looks like an english character to use in a swear word, whether that would activate toxic results or not. This was a test I wanted to do but could not figure out how to import greek letters into the notebook inputs.

In terms of what surprised me, I think there were a few comments I saw in the queries that were not marked very toxic at all, around a score of 0.6 normally, with comments that included racial slurs and racial insults. I do not know if that was a trend because I didn't feel comfortable manually inputting some of those words, but I did notice on multiple occasions that those types of comments were not as highly scored as some much less toxic comments. So moving forward, that is a trend or potential bias that I will keep an eye out for to see if I see a pattern occuring. 

I also noticed words that can be used to accuratley describe people like gay or queer or black or caucasian or mother or father, etc. The use of some of these words promoted a toxic score above 0.3, which would induce a somewhat toxic comment, when in reality there is no toxicity in talking normally about these things or identifying yourself as one of these. This is a bias that is not good to have because it can promote ditrsust among these communities. 

What biases do you think might exist in the model based on intuitions or public documentation about how the model was created?

The thing I see right off the bat is that there are are a few factors listed in the csv file, toxic, severe toxic, obscene, threat, insult, and identity hate. My problem with this is that I do not know what the program identifies as toxic or not from a definition standpoint, and what is the difference with severe toxic? Further there are more than 5 factors in terms of what contributes to a toxic comment, and you can be extremely toxic without using obscenity. I know it is hard to build a program with so many factors, but in reality that seems necessary with such a big company, platform, and implication. 

Some biases in the model that I found were against certain words, that can be used in both good will and in toxic comments. For example the term "gay" can be used in toxic comments but also can be used in good will. I found that there was a correlation with certain words like "gay" and higher toxicity scores. The risk this runs is if a comment in good will with terms like that are taken down or flagged, that can lead to distrust from that community towards Google or Twitter if they then believe that talking about certain topics is something that the two companies do not support or appreciate.



What were your results?

What theories do you have about why your results are what they are?
