# 35.-Star-Wars-Reinforcement-Learning

its less on the RL algorithms, but more on learning how to design a good RL Environment (such as the reward functions, etc.)

Relatively simple environment


FOr phase 3, NPC ships are regenerated cuz by the time the explorers decide to send a new drone, the state of the war could be different and new ships will occupy the area so yea.

For Phase 3, also another issue is that the RL agent found a policy to 'camp' at the last planet to farm the rewards off its positive rewards halo rather than just visiting it. It likely didnt want to visit it because once it visits it the planet will emit a negative rewards halo, which penalises it. 

Solution:
- I maybe could fix this by not making visited planets penalise the RL agent.
- or i could give a big reward for the RL agent if it finds all planets. However, I didnt want to do it because it dosent make sense as the RL agent isnt supposed to know how many planets there are in the map, and the objective is supposedly to try its best to find as many planets as possible.
- one more rationale is that we could still give the RL agent a big reward for finding all planets, if it has already seen all parts of the map (since if it has already seen all parts of the map, then it make sense that we should already know how many planets there are in the area and thus we should know if all planets has already been found)

As you could see, I believe there is alot of possible improvements and expansion on this project (could be applied to space travel or similar fields of work) to simulate different scenarios. So I open to anyone who willing to contribute new scenarios and the learned policies.

Currently the NPC ships, particularly the SeparatistShips are moving at half the speed of the RL agent, making it very easy for the RL agent to outmaneouvre them. I believe if we make them move at the same speed as the RL agent, it will force the RL agent to learn very different policies (and definitely will take longer/more iterations to train) (which I do not have the luxury of since Im running all this on my local laptop and each training process takes me 30 minutes)

But, I will open this phenomenon to your interpretation and future experiments.

Sorry the logs and saved RL models are really messy... I didnt manage to spend the time to organise them. But I did highlight the key RL models through which their policy/behaviour helped me to formulate the reward function to finding the best policy in that environment.

I didnt have the luxury to test the environments with other RL algorithms, but let me know if anyone did (though I assume they should more or less work similarly in finding the planets (since thats the ultimate goal in the various scenarios with slight differences in cumulative rewards)). Since in all my experiments i just used SB3's PPO only. 

talk about the future phase 4 and 5, and possibly using LLMs. Might do it when free 

Call if anyone wanna contribute (e.g. a new environment/better reward function for the existing ones, feel free to do a pull request)

Put extra render of the seperatist and republic logo, maybe planet logo also in the simulation


Tried to get RepublicShips visible to potentially encourage emergent behaviour (not reward-driven, since I dont reward the RL agent from being near a RepublicShip, I merely allowed it to 'see' them in its vision)... but not sure if it works (to encourage high level policies arising from emergent behaviour such as kiting, camping near RepublicShips so they will take agro from SeperatistShips to maximise its rewards if the RL agent 'sees' a RepublicShip). 

I spend many weeks watching pixels move around - not good for my sanity

