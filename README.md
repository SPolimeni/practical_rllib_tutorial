RLlib documentation: https://docs.ray.io/en/latest/index.html

We are working with Ray 1.10.0

# Tutorial Steps
## 1. Installation
```
conda create -n rllib python=3.8
conda activate rllib
pip install "ray[rllib]" tensorflow torch

pip install pygame  # so we can visualize what is going on, 2.1.2
```
## 2. Setup
Set `YOUR_ROOT` in `your_constants.py`

## 3. Test the Environment
Run `demo/demo_your_rllib_env.py`
You should see your robots running around until they bump into a chicken.

## 4. Train Your Agent
Run `your_rllib_train.py` 
(set `NUM_ITERATIONS` to 500 for about an hour of training to match the results in the slides)

Results at `your_home_dir/ray_results/YourTrainer`

Go into directory
```
cd your_home_dir/ray_results/YourTrainer
cd YourTrainer_YourEnvironment_?????_00000_0_2022-MM-DD_SS-NN-NN  # fill in with what is there
```

Run TensorBoard to see the results
```
tensorboard --logdir ./  
```

## 5. Load and Use the Learned Policy
Put in your run and checkpoint number in `demo/demo_after_training.py` and run it.

## 6. Look at Your Learned Policy
Put in your run and checkpoint number in `demo/demo_look_at_policies.py` and run it.

# Credits
Icons from publicdomainvectors.org https://publicdomainvectors.org/  

robot https://publicdomainvectors.org/en/free-clipart/Yellow-robot/81372.html

chicken https://publicdomainvectors.org/en/free-clipart/Vector-illustration-of-cartoon-chicken-confused/24675.htm