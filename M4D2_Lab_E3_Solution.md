# Exercise 3: Quantifying differences in spiking - Method 1

One way that we will observe differences in neural activation in both areas is by looking at <i> total number of spikes in visual areas vs non-visual 
  areas </i> during the visual behavior task. This is known as the <b> total spike count.</b>

> <b>Create a hypothesis: do you think that mice will have more neural spiking in visual areas or in non-visual areas during the task? 
> What about before the stimulus onset for the task?</b> Write your hypotheses below.

## Solution: 

```
Hypotheses: 
```

Now that you've made an informed guess about what the total spike count will look like for each dataset, let's go ahead and analyze the data! <i>Which data matrix will have a greater total spike count?</i>

> <b>Write some code below to determine which brain regions</b> (`vis_data` or `non_vis_data`) <b> have a greater total spike count.</b>

## Solution:

```ruby
# To do this, you want to count the total number of spikes for ALL neurons.
# Remember that there are 111 neurons in each subset of data.

# Hints: 
  # Check out NumPy's nonzero function
  # Check out what 'for' loops can do when coding in Python.

#Checking the shape again as a reminder
vis_data.shape

# np.nonzero gives you a matrix with 2 arrays. Each index in both arrays gives 
# the X and Y coordinates in the matrix where there is a nonzero element.
ans = np.nonzero(vis_data)

#Checking that a random coordinate will give a non-zero element
vis_data[2,181]

# Finding how many nonzero elements we have
len(ans[0])

# Answer:
# This vis_data matrix is 111x250, which means that there are 27,750 entries. Out of 
# these number of entries, 411 of them are 1's. There were 411 spikes in the 
# total visual neurons over time. 

ans2 = np.nonzero(non_vis_data)
len(ans2[0])

# Answer:
# This non_vis_data matrix is 111x250, which means that there are 27,750 entries. 
# Out of these number of entries, 590 of them are 1's. There were 590 spikes 
# in the total visual neurons over time. 

```
