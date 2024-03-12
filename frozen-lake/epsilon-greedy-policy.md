# Epsilon-Greedy Algorithm

In terms of how the agent navigates the map, both Q-Learning and Deep Q-Learning uses the Epsilon-Greedy Algorithm

```python
# Epsilon starts with the maximum value (1)
epsilon = 1

# Decay rate is the amount of epsilon decrease of each episode
decay_rate = 0.0005

# We generate a random number between zero and 1 (lower and maximum values of Epsilon)
random_number = random.random()

if random_number < epsilon:
  # If the random number generated is lower than epsilon, we take a random action
  > select random action
else:
  # If it's higher then epsilon, we take the best action (based on Q-table ou DQN)
  > select the best action

# At the end of each episode we decrease the epsilon value by a decay rate
epsilon = epsilon - decay_rate
```

Based on this, we can observe that, how much as we train our DQN (or Q-Table), minor is our epsilon. This means that, on each episode, minor is the chance of getting a random action. 

So, as how trained is our DQN, we have higher chances to execute the best action, based on our weights and biases. And less chances to get a random action.