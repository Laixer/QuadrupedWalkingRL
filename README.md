# Training a robot to walk using Unity ML-Agents

# Environment

* Agent: a 4-legged crawler with each leg having 2 joints. 
* Goal : walk towards a dynamic target without falling.
* Methods : policy-based learning, off-policy learning
* Results : the off-policy learning method(SAC) is more sample-efficient and yields a higher maximum reward of 539 



#Setup for Inference using the trained models

* Launch Unity
* In the Project window, go to the Assets/ML-Agents/Simulation/Crawler/Scenes folder and open the CrawlerDynamic scene file.
* In the Hierarchy window, click on DynamicPlatform/Crawler.
* In the Inspector, there should be a model present under Behavior Parameters. This model was trained using Soft Actor Critic. You can also select the model trained with PPO (in Assets/ML-Agents/Simulation/Crawler/TFModels).
* Press the Play button to see the agent in action.

All training information and model statistics can be found in the summaries directory.

# Setup for Training

* Download and install Anaconda with Python v3.6.1 or higher
* It is recommended to create a conda environment and install the python dependencies there 
* Install tensorflow: pip install tensorflow==1.7.1
* Install mlagents: pip install mlagents

Once this is done, you can use the mlagents-learn API to train, or train via ml-agents-envs on Jupyter notebook.