april 9th
# This Time
#### Characters to Add
- Ramona Flowers (Scott Pilgrim)
	- could also do Knives Chau!
- ~~Aerith (Final Fantasy 7), might be much harder to get video game files~~
	- ended up being way too complicated
- Trinity (the Matrix)
- Chloe (Uncharted 2) (will need to modify code to use : instead of line breaks)

This is a good start!
- I will be adding each of these characters to my file to give the model more data to pull from

# Progress
- I've found all required scripts online, so now I will be adding them to work to make sure that I can accommodate merging multiple scripts together
- the only roadblock seems to be that I will have to modify my function for Chloe from Uncharted, since the script uses colons instead of line breaks to indicate dialogue
- I will make txt files for every other script first and execute the function, then rewrite it to get Chloe's dialogue
- Everything is (hopefully) done. I'm a bit nervous about the Chloe code, since I modified the function, but fingers crossed
- worst case, I'm not worried about just commenting it out/not running it for now
- on a whim, I also decided to add Envy from Scott Pilgrim... because Scott Pilgrim seems like the type to have an AI GF
- another interesting element of this is seeing how much/little different female characters speak
	- many of these female love interests are integral to their medias' plots, but when i get into it, they seem to only have minimal lines of dialogue, making their media *about* them rather than what they have to say
![](/images/4-09-04)
- With all of our characters done, it's time to concatenate their dialogue
- Chloe definitely has the most dialogue, which makes sense since she's a video game character in a 10+ hour narrative, but I'm h0ping she won't dominate the training data, else I may have to cut her out (after I made her own function and everything, sorry Chloe!)
- However, this should definitely get me to my goal of 1000+ lines
- I lied! 848 :(
- but this is okay, since it still gives me more opportunities to add.
	- it does make me more worried about chloe taking over, since she has 348 of these lines
- Lastly, we train again! let's see what GPT has to say
- Findings: the output still! is swayed towards her, but not as bad as before.
- i wonder if this will change if her is in the middle VS first or if i need more data or if the responses are catered to her, i think I will have to search around and experiment a ltittle more
![](/images/4-09-05)
# Next Steps
- I am going to import my code into Colab again to do a big big training session and see what I get. If the results are promising, I will continue to further sophisticate my training before getting to the final results
- i feel like i need much much more data to be able to get adequate and variable results, but i'm drawing a blank on training data
- i also wonder if there is any way to contain responses to contained sentences, instead of it trailing onto the next lines of dialogue, but im unsure if this is within my current scope
