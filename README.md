# Dexterous Grasping Training Preparation

Training resources used to prepare for a final-year project on dexterous robotic grasping. The main example is the DRO-Grasp workflow for learning cross-embodiment robot–object geometry from point clouds. It includes correspondence pretraining, supervised grasp training, Hydra configurations, data loaders, and validation utilities. The notebooks cover related PyTorch exercises, including VAE and conditional VAE training on MNIST.

## Training

Set up the Python and PyTorch environment using the [upstream setup instructions](dro-grasp/README.md). Download the required grasp datasets from the upstream release, then select the robot hands and training settings in `dro-grasp/configs/`.

```bash
cd dro-grasp
pip install -r requirements.txt
python pretrain.py
python train.py
```

The training scripts use Weights & Biases. Follow the upstream setup to configure it, or adapt the logger for a local run. Isaac Gym is used by the simulator evaluation entry points. The dataset and checkpoints are available from the upstream release. The MNIST notebooks use optional `torchvision`, `matplotlib`, and `tqdm` installations.

The training reference code comes from [DRO-Grasp by Zhenyu Wei et al.](https://github.com/zhenyuwei2003/DRO-Grasp). Its original README and [MIT license notice](dro-grasp/LICENSE.txt) are included. This repository is a preparation snapshot of the training workflow. BODex, PyTorch3D, MANO, NIMBLE, local datasets, generated weights, and personal notes are outside its scope.
