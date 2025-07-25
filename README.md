# 35.-Star-Wars-Reinforcement-Learning

its less on the RL algorithms, but more on learning how to design a good RL Environment (such as the reward functions, etc.)


FOr phase 3, NPC ships are regenerated cuz by the time the explorers decide to send a new drone, the state of the war could be different and new ships will occupy the area so yea.

For Phase 3, also another issue is that the RL agent found a policy to 'camp' at the last planet to farm the rewards off its positive rewards halo rather than just visiting it. It likely didnt want to visit it because once it visits it the planet will emit a negative rewards halo, which penalises it. 

Solution:
- I maybe could fix this by not making visited planets penalise the RL agent.
- or i could give a big reward for the RL agent if it finds all planets. However, I didnt want to do it because it dosent make sense as the RL agent isnt supposed to know how many planets there are in the map, and the objective is supposedly to try its best to find as many planets as possible.
- one more rationale is that we could still give the RL agent a big reward for finding all planets, if it has already seen all parts of the map (since if it has already seen all parts of the map, then it make sense that we should already know how many planets there are in the area and thus we should know if all planets has already been found)

But, I will open this phenomenon to your interpretation and future experiments.


talk about the future phase 4 and 5, and possibly using LLMs. Might do it when free 

Call if anyone wanna contribute (e.g. a new environment/better reward function for the existing ones, feel free to do a pull request)

Put extra render of the seperatist and republic logo, maybe planet logo also in the simulation

I spend many weeks watching pixels move around - not good for my sanity
