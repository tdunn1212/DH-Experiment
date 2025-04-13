april 7th
## Starting Thoughts
I am looking at the code for making your own GPT-2 bot for the first time and I am... confused. and overwhelmed. In my aims for this assignment, I want to take the preliminary steps in creating GPT-2 bots that can converse in a rudimentary way similar to AI girlfriends.

### First experiment 04/07
- in this first try, I am going to try and create a super insanely simple bot based on dialogue from Haley in Stardew Valley, one of the more hyperfeminine and (at first glance) vapid characters
- Thanks to the game's online community, I have a JSON file (attach) of all of Haley's dialogue, which I will input into the Practical Necromancy code Shawn Graham provided me with and I'll see what happens
- the code will very likely break...
- the file upload did work! I'm definitely going to have to revise my JSON files to parse them for specific text, since right now it just gathers each line. right now there's a big long training session happening
	- i will also need to figure this out for movie scripts, where I only want certain characters' dialogue![](/images/4-07-01)
	- the photo of my code running.... i did not account how long it would take to train a LLM. no instant gratification to be found here
- in the future... i will not add as many steps to my preliminary efforts (it's been 22 minutes... now 36..)

While I wait, I think I will write a revised idea of my final goals for this process
- I don't expect I will reach the final experimental AI model I want to be included in my thesis. I think I will need to spend much more time learning Python and ML processes to get to the final product
- *What I do want, is a rudimentary LLM that mimics the kinds of dialogue found in appealing/attractive fictional characters and video game dialogue*
- Not only will this first try (not to be confused with my ongoing first-first try) give me an idea of how to refine my code and process for the final thesis project (getting my toes wet), it'll also give a good insight into _how sophisticated_ LLM/AI GFs are
So...
>*This experiment is then my first steps in developing my programming experience to successfully create my replication of an AI girlfriend large language model (LLM), to distill the sophistication, obscurification, and potential harms in AI GFs

#### Final Results
![](/images/4-07-02)
![](/images/4-07-03)
So it didn't work... I need to go through the JSON file and add code that parses and isolates the dialogue and not the entire file
- Right Now, it's incoherent and doesn't really work how I want it to, but! I uploaded my own file and the code still ran, so there's a small victory
- Next time, I will add code that parses the file and maybe tries multiple files of dialogue for a larger sample size
	- since the data that I did get outputted was the same lines of dialogue each time
