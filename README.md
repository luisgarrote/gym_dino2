# Gymnasium Environment of the Chrome T-Rex Game

A pygame based port of the Chrome T-Rex Game as an Gymnasium Environment.

## Important info

You can change the FPS of the game by adjusting the env.FPS value. By default, it is at 60.

`Action Space = [0, 1, 2]
`

`
0 : No action
`

`
1 : Duck
`

`
2 : Jump
`


<img width="598" height="148" alt="image" src="https://github.com/user-attachments/assets/29f4dcec-ca72-496c-8cfc-dd01fb9f538f" />

You can import it as:

```
import gym_dino2
```

Demo code:
```
import gymnasium as gym
import gym_dino2

# Create the environment
env = gym.make('dino-v0')

obs,info = env.reset()
done = False

while not done:
    env.render()
    action = env.action_space.sample()
    obs, reward, done, truncated, info = env.step(action)
env.close()
```
---

Adapted from  [Rochan-A's gym-dino](https://github.com/Rochan-A/gym-dino).
