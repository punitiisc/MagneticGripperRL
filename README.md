# MagneticGripperRL
RL environment with magnetic gripper and IK-based control (code private until publication)
# IKGripperEnv: Reinforcement Learning with Magnetic Gripper Control

> 🔒 *Note: The full environment and training code will be released after the acceptance of the associated publication.*

## 🧠 Project Summary

This project introduces a custom Gymnasium-compatible environment simulating a 7-DOF robotic arm equipped with a magnetic gripper. The agent is trained using Soft Actor-Critic (SAC) to attach to a slowly rotating object using inverse kinematics control in a continuous action space.

- 🎯 Task: Track and magnetically attach to a rotating cube using IK-based control
- 🧲 Gripper: Reward is given for successful proximity-based magnetic attachment
- 🎥 Rendering: RGB rendering supported for evaluation and video export

## 📽️ Demo Video

Click to watch:
[sac_gripper_result.mp4](./rollout/sac_gripper_result.mp4)

## 📈 Evaluation Plot

![eval_reward_plot](./training/eval_reward_plot.png)

- Reward reached **+90** after ~20,000 timesteps with SAC.
- Consistent success in attaching and tracking the rotating object.

## 📊 TensorBoard Logs

Logs for reward, loss, entropy, and evaluation can be viewed in TensorBoard.

```bash
tensorboard --logdir sac_gripper_tensorboard/
