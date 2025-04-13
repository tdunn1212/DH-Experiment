april 8th
# This Time
- I will be adding to the dataset with more scripts, I am for sure using Ava from *Ex Machina,* and if I think of any others on the fly, I can add that too
- My goal is to just add some variety to my dataset to increase the options for GPT2 to respond with.

# Progress
- Easily enough, I redefined my function and variables to extract Ava's dialogue from the Ex Machina script![](/images/4-09-01)
- The convenience of this makes me want to do it ten more times, but I feel like for the sake of not going buck wild, it's best to just concatenate samantha and ava to train my model, then try adding a whole bunch and seeing what happens next
- Having this function already written will make it easy for me to go wild and add a whole bunch of characters to work out a completed GF
  ![](/images/4-09-02)
- I was able to successfully combine the sam and ava files, bringing my training data to 270~ lines of dialogue. I think for my final test, I want to have at least 1000 lines to have a larger variety of data I am drawing from 
- Things are going so deceptively well. I am used to my code blowing up in my face... this could be a good confidence booster or a sign of things to come!
- Lastly, I will try to see what happens when I train GPT2 on my GFdata.txt file to see how things go, then I know I can move onto the next stage of finding more sources
  ![](/images/4-09-03)
- Here's the final output with both dialogue sets, unfortunately, it seems like GPT2 prefers Samantha a whole lot more, which makes sense since she has more dialogue and a warmer tone. I definitely want to find more sources to pull from, but this step has made me feel much more confident, and I feel like I can streamline my process much more from here.

# Next Steps
- First, I am going to find more sources to expand my dataset
- Then, once I train the model on data I deem to be big enough, I will do a big training session to assess the results in a more detailed manner (probably back in Colab, for the faster GPU speeds)
