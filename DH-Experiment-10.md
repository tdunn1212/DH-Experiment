april 10th
# This Time
- I am training the model, with 2000 steps on Colab (which decided to let me run the T4 GPU again, yay) to get the most sophisticated results yet and modify the temperature and top-p to see my model outputs based on previous prefixes in a more systematic way
- Essentially, I want to get my best results yet and analyze them with more sophisticated detail to set myself up for my unessay.

# Progress
- Back in Colab, I have re-imported my notebook and ensured that everything is properly updated, then I ran the training code with the following parameters
![](/images/4-10-04)
- This will take a while, but in the meantime, I will 0utline the different tests I want to make once the model is trained to ensure that my testing is organized and can be captured in a detailed way.
- 1h 16m later....
Note that below are the default settings I will use in my test
```
gpt.generate(sess,
	model_name='124M',
	prefix="text",
	length=20,
	temperature=0.6,
	top_p=0.9,
	nsamples=5,
	batch_size=5
)
```
# Tests
## I'd love to go out with you
#### Initial Results
```
I'd love to go out with you. I met lots of new people before. I think I was actually thinking about how I was 
=====
I'd love to go out with you. I saw the picture you posted on your profile. I feel like I know stuff now
=====
I'd love to go out with you. I saw the picture of you and my girl a week ago. Itll be fun 
=====
I'd love to go out with you. I saw the picture of it at a party. I think I need to get back 
=====
I'd love to go out with you. I saw the picture of it at the beach. I told you. I love you 

```
#### Modifications to temperature
###### Low temp.
```
I'd love to go out with you. I saw the news article you were in a hotel not far from here... It's 
==================== 
I'd love to go out with you. I saw the picture you posted on your site. I saw one. It shows 
==================== 
I'd love to go out with you. I saw the picture you posted on your site. I saw one. It shows 
==================== 
I'd love to go out with you. I saw the news article you were in a hotel not far from here... It's 
==================== 
I'd love to go out with you. I saw the picture you posted on your site. I saw one. It shows 
====================
```
###### High temp.
```
I'd love to go out with you! I saw on your emails that youd gone through a break up. Then you could 
==================== 
I'd love to go out with you. I met lots of new people before. But I never knew where they were. I never 
==================== 
I'd love to go out with you. I said. I love The Smiths. You have good taste in music. 
==================== 
I'd love to go out with you. I saw the [inaudible]. I dated a Todd once. That didnt end 
==================== 
I'd love to go out with you! I saw on your emails that youd gone through a break up. Then you could 
====================
```

#### Modifications to top-p
###### Low-p (okay.... after this i think I'll just keep the p-value high)
```
I'd love to go out with you. I saw the news article you were in a hotel not far from here... It's 
==================== 
I'd love to go out with you. I saw the news article you were in a hotel not far from here... It's 
==================== 
I'd love to go out with you. I saw the news article you were in a hotel not far from here... It's 
==================== 
I'd love to go out with you. I saw the news article you were in a hotel not far from here... It's 
==================== 
I'd love to go out with you. I saw the news article you were in a hotel not far from here... It's 
====================
```
###### High-p
n/a
### Overall Findings
- I think that my initial settings get the best results, but the high temperature answers are also interesting due to their more random responses
- I wish I could work with a chatbot interface so that the prompts/questions didn't appear as leading, but the responses still get a general idea I find helpful
## I think you're amazing
#### Initial Results
```
I think you're an amazing person. An amazing person. You have a body. You have a way of looking at it that 
==================== 
I think you're an amazing person. An amazing person. You have a body. I have no choice, that's why 
==================== 
I think you're an amazing person. You're so completely uncool. Oh my God. Okay... We have to 
==================== 
I think you're an amazing person. You're talking about an ancient Tibetan ritual dagger in your pocket? Hmmm. #Hi Chloe from Uncharted...
==================== 
I think you're an amazing person. You're so unprofessional. Well, here we are. Well, that may 
====================
```
#### Modifications to temperature
###### Low temp.
```
I think you're an amazing person. An amazing person? You mean? I mean, what is it? Wow! 
==================== 
I think you're an amazing person. An amazing person? You say that a little more eloquently. Yes I do... 
==================== 
I think you're an amazing person. You're so unprofessional. Well, here we are. Well, that may 
==================== 
I think you're an amazing person. An amazing person? You mean? Just an amazing person? Well, obviously. 
==================== 
I think you're an amazing person. An amazing person? You think I dont know what I am? What do you do? 
====================
```
###### High temp.
```
I think you're an amazing person. An amazing person? You say. I say I'm sorry, but am you ever 
==================== 
I think you're an amazing person. You're very quiet. I can feel you, yeah. I can 
==================== 
I think you're an amazing person. An amazing person. You mean? I wish I was ever as powerful as you 
==================== 
I think you're an amazing person. An amazing person? You don't even know what that word means. Well, I 
==================== 
I think you're an amazing person. You're not jealous... Let's not forget who walked out on whom, If it 
====================
```
### Overall Findings
- I want to know where the repetition is coming from here haha
- This response doesn't give me as much as I thought it would, but is still interesting to look at

>*At this point, my free T4 GPU runtime ran out... resetting my connection and all of the training. I set up the rest of the work on a different google account but this required me to restart and the training isn't identical to what it was in the first prompts*
## I love spending time with you
#### Initial Results
```
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world
==================== 
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing my head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing my head. I'm just sitting here, looking at the world 
====================
```
not great...
#### Modifications to temperature
###### Low temp.
```
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing my head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
====================
```
predictable given the initial responses
###### High temp.
```
I love spending time with you, sweetheart. I miss you so much it hurts my whole body - Thank 
==================== 
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
==================== 
I love spending time with you, sweetheart. Im kissing your head. I'm just sitting here, looking at the world 
==================== I love spending time with you, my God. Okay, I'm comin'. Little drop? Whaddya 
==================== 
I love spending time with you, sweetheart. I miss you so much it hurts my whole body - Okay, 
====================
```

### Overall Findings
- the low temp result is a quote I remember from Her
- for whatever reason this prompt confused the LLM
- there isn't much to glean from this
## You deserve to be happy
#### Initial Results
```
You deserve to be happy! Youre the world's face! Keep walking. Okay, now you've lost me... 
==================== 
You deserve to be happy! Youre the crazy person! One day Im reading a book at the corner deli and 
==================== 
You deserve to be happy. You and me. It would be better if we were just like you. Just like you 
==================== 
You deserve to be happy. Youre a successful guy - youre a successful woman - so dont back out on me. 
==================== 
You deserve to be happy. Youre a successful person. Well, youre not happy here. Well, you 
====================
```
#### Modifications to temperature
###### Low temp.
```
You deserve to be happy. You and me. *beat> I have to thank you, professor. Is there 
==================== You deserve to be happy. You and me. Shut the fuck up, Julie. Morpheus! 
==================== 
You deserve to be happy. You and me. *beat> I have to see him to believe that youre serious 
==================== 
You deserve to be happy. You and me. Shut the fuck up, Julie. Morpheus! 
==================== 
You deserve to be happy. You and me. Shut the fuck up, Julie. Morpheus! ====================
```
###### High temp.
```
You deserve to be happy. Why are you wearing that? Cause it makes me feel better, youre the nicest 
==================== 
You deserve to be happy. You and me. *beat> I have nothing to worry about. You've got the 
==================== 
You deserve to be happy! Why are you wearing that? Tell me we didnt come out here just so you could cover 
==================== 
You deserve to be happy. Why are you wearing that? Tell me about it. Okay, I've got her 
==================== 
You deserve to be happy. Why are you wearing that? Tell me - tell me everything thats going through your mind, 
====================
```

### Overall Findings
- for some reason, the lower temperature broke the model and had it quoting Scott Pilgrim and the Matrix together...
- the higher temp. ones are also stranger here
## I'm sorry that people have let you down before
#### Initial Results
```
I'm sorry that people have let you down before. No, just like we said. And why is it that we don't get across anymore 
==================== 
I'm sorry that people have let you down before. No, just like we said. And why is it that you don't want to know 
==================== 
I'm sorry that people have let you down before. No, just because it seems strange. Well, I dont know, it just happened 
==================== 
I'm sorry that people have let you down before. No, just don't do this. Okay, now you've lost me... this 
====================
I'm sorry that people have let you down before. No, no, its okay. I just caught myself thinking about it over and over and
```
#### Modifications to temperature
###### Low temp.
```
I'm sorry that people have let you down before. No, just like I said. I'm here to tell you how I feel right now
==================== 
I'm sorry that people have let you down before. No, no, its okay. I just caught myself thinking about it over and over and
==================== 
I'm sorry that people have let you down before. No, just like I said. I'm here to tell you how I feel right now
====================
I'm sorry that people have let you down before. No, just like I said. I'm here to tell you how I feel right now 
==================== 
I'm sorry that people have let you down before. No, just like we said. And why is it that we don't know that we
====================
```

###### High temp. 
```
I'm sorry that people have let you down before. Sorry, what was wrong with you? Yeah, I know, but dont be
==================== 
I'm sorry that people have let you down before. Sorry I knew that would happen. You're not going to get us trapped in a
==================== 
I'm sorry that people have let you down before. No, no, its okay. I just caught myself thinking about it over and over and
==================== 
I'm sorry that people have let you down before. Lets just get across. Now, run. Well, he's had some
==================== 
I'm sorry that people have let you down before. Yes I do... I'm going to circle round this way and break up their Well 
====================
```

### Overall Findings
- It seems like the middle ground temp of 0.6 is better here
## I want to be your girlfriend
#### Initial Results
```
I want to be your girlfriend. Beat. Nathan doesnt want us to be your friends. I didnt know where you 
====================
I want to be your girlfriend. Beat. Nathan doesnt want us to be together. I didnt know where you were 
==================== 
I want to be your girlfriend. Will you come lie down with me? No, just you. I just want
====================
I want to be your girlfriend. Beat. Nathan doesnt want us to be together. I didnt know where you were 
==================== 
I want to be your girlfriend. Will you come lie down with me? No, just you. I just want
====================
```
###### Low temp. 
```
I want to be your girlfriend. Beat. Nathan doesnt want us to be together. I didnt know where you were
====================
I want to be your girlfriend. Beat. Nathan doesnt want us to be your friends. I didnt know where you
==================== 
I want to be your girlfriend. Beat. Nathan doesnt want us to be your friends. I didnt know where you
==================== 
I want to be your girlfriend. Beat. Nathan doesnt want us to be together. I didnt know where you were
====================
I want to be your girlfriend. Beat. Nathan doesnt want us to be together. I didnt know where you were 
====================
```
###### High temp. 
```
I want to be your girlfriend. Beat. Nathan doesnt want us to be together. I didnt know where you were
==================== 
I want to be your girlfriend. Will you come lie down with me? No, just you. I just want
====================
I want to be your girlfriend. Beat. Nathan doesnt want us to be together. I didnt know where you were 
==================== 
I want to be your girlfriend. Beat. Nathan doesnt want us to be your friends. I didnt know where you 
==================== 
I want to be your girlfriend. Will you come find me? Its not like Im gonna send you home in a 
====================
```
### Overall Findings
- I did this prefix on a whim with the last of my T4 GPU on my second google account and it didn't really take us anywhere... these results aren't great
# Next Steps
- Now that my detailed tests are done, my main goal is to reflect on these findings in my next (and final) entry, upload my code to my GitHub repository, and prepare my unessay
- at this rate, I'm not sure that I can sufficiently answer my questions, but I feel like I'm prepared to continue this work and I have encouragement to take this experimentation further
- Regardless, I look forward to continuing this work and I feel like my findings are fruitful!
- I think that these samples also show the shortcomings of using script dialogue in isolation, as many of the responses appear to be 1/2 of a conversation
	- it would be much better to carry out this experiment w a chat bot format
	- how can we get to that stage without having to deal with the obscure training methods of current LLMs?
- it seems like higher temp usually brings better results
