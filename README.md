# deep-RL-course-labs

## Unit 1 repository: [k0T0z/ppo-LunarLander-v2](https://huggingface.co/k0T0z/ppo-LunarLander-v2)
## Bonus unit 1 repository: [k0T0z/ppo-Huggy](https://huggingface.co/k0T0z/ppo-Huggy)
## Unit 2 repositories: [k0T0z/q-FrozenLake-v1-4x4-noSlippery](https://huggingface.co/k0T0z/q-FrozenLake-v1-4x4-noSlippery), [k0T0z/q-Taxi-v3-500](https://huggingface.co/k0T0z/q-Taxi-v3-500)
## Unit 3 repository: [k0T0z/dqn-SpaceInvadersNoFrameskip-v4](https://huggingface.co/k0T0z/dqn-SpaceInvadersNoFrameskip-v4)

## Unit 3 building:

1. Clone the repository.
```bash
git clone https://github.com/k0T0z/deep-RL-course-labs.git
```

2. Change directory.
```bash
cd deep-RL-course-labs
```

3. Download the requirements.
```bash
pip install -r unit3-requirements.txt
```

4. Run the training.
```bash
python -m rl_zoo3.train --algo dqn --env SpaceInvadersNoFrameskip-v4  -f logs/  -c dqn.yml
```

5. Run the evaluation for 5000 steps.
```bash
python -m rl_zoo3.enjoy  --algo dqn  --env SpaceInvadersNoFrameskip-v4  --no-render  --n-timesteps 5000  --folder logs/
```

6. Upload the model to the Hugging Face Hub. Replace `_____` with your username.
```bash
python -m rl_zoo3.push_to_hub  --algo dqn  --env SpaceInvadersNoFrameskip-v4  --repo-name dqn-SpaceInvadersNoFrameskip-v4 -orga _____ -f logs/
```

