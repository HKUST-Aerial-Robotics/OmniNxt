<div align="center">
    <h2>OmniNxt: A Fully Open-source and Compact Aerial Robot with Omnidirectional Visual Perception</h2>
    <strong>IROS 2024 Oral</strong>
    <br>
        <a href="https://uav.hkust.edu.hk/current-members/" target="_blank">Peize Liu</a>,
        <a href="https://chen-albert-feng.github.io/AlbertFeng.github.io/" target="_blank">Chen Feng</a><sup>†</sup>,
        <a href="" target="_blank">Yang Xu</a>,
        <a href="" target="_blank">Yan Ning</a>,
        <a href="https://www.xuhao1.me/" target="_blank">Hao Xu</a><sup>†</sup>, and
        <a href="https://uav.hkust.edu.hk/group/" target="_blank">Shaojie Shen</a>
    <p>
        <h45>
            HKUST Aerial Robotics Group &nbsp;&nbsp;
            <br>
        </h5>
        <sup>†</sup>Corresponding Authors
    </p>
    <a href='https://arxiv.org/pdf/2403.20085.pdf'><img src='https://img.shields.io/badge/arXiv-OmniNxt-red' alt='arxiv'></a>
    <a href='https://hkust-aerial-robotics.github.io/OmniNxt/'><img src='https://img.shields.io/badge/Project_Page-OmniNxt-green' alt='Project Page'></a>
    <a href="https://www.bilibili.com/video/BV1AK421Y7Vz/?spm_id_from=333.999.0.0&vd_source=0af61c122e5e37c944053b57e313025a"><img alt="Bilibili" src="https://img.shields.io/badge/Video-Bilibili-blue"/></a>
    <!-- <a href="https://www.youtube.com/watch?v=jjPPIAAkPrk"><img alt="Youtube" src="https://img.shields.io/badge/Video-Youtube-red"/></a> -->
</div>

<div align="center">
  <img src="misc/system_overview.png" alt="system overview" />
</div>

## 📢News

* **[30/06/2024]**: OmniNxt is accepted to IROS 2024.
* **[15/08/2024]** V0.1 Release

## Outline

[TOC]

## 🤖Build your own OmniNxt 

> You should have basic knowledge of the standard quadrotor's electronic system. 

#### BOM

| 🧰Component                    | 📏 Specification                                              | 🔗 Purchase Link                                              |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| ***Quad-Fisheye Camera Set*** |                                                              |                                                              |
| OAK-FFC-4P                    | Camera control board                                         | [Official](https://shop.luxonis.com/products/oak-ffc-4p) / [Taobao](https://detail.tmall.com/item.htm?abbucket=2&id=797243380525&ns=1&priceTId=213e37fe17166914596117457e9698&skuId=5432965948084&spm=a21n57.1.item.4.2d47523c7FgKjv) |
| B0335 (OV9782)                | Camera  modules (Fisheye lens FOV larger than 210 degrees)   | [Official](https://www.arducam.com/product/arducam-1mp-ov9782-global-shutter-color-mipi-camera-module-22pin-for-depthai-oak-dm1090ffc) / [Taobao](https://item.taobao.com/item.htm?abbucket=2&id=681463610876&ns=1&priceTId=213e376b17166916784225765e28ee&skuId=5076193835807&spm=a21n57.1.item.10.2d47523c7FgKjv) |
| Camera cables                 | Customized                                                   | Camera cable SCH                                             |
| ***Onboard computer***        |                                                              |                                                              |
| Jetson Orin Nx                |                                                              |                                                              |
| Jetson Orin Nx carrier board  |                                                              | [DM](https://item.taobao.com/item.htm?id=719455999699&spm=a1z10.1-c-s.w4004-23557095002.16.165328f6HpXRcJ&skuId=5047593809727) |
| Jetson Orin Nx radiator       |                                                              |                                                              |
| Jeston Orin Network card      |                                                              |                                                              |
| 2230 SSD                      |                                                              |                                                              |
| Intel AX200                   |                                                              |                                                              |
| ***Flight platforms*** (6S)   |                                                              |                                                              |
| Nxt-FC                        | [Project Page](https://github.com/HKUST-Aerial-Robotics/Nxt-FC) | [MicoAir](https://micoair.com/flightcontroller_nxtpx4v2/) / [Taobao](https://item.taobao.com/item.htm?abbucket=2&id=720171355815&ns=1&priceTId=2150440c17167079494632690e1d2e&spm=a21n57.1.item.4.54dc523cLAwNaW) |
| Flight frame                  | Customized                                                   | [Fusion360](https://a360.co/3vK6dJd)                         |
| Protector                     | Customized / Oddity RC XI35 protector                        | [Fusion360](https://a360.co/3vK6dJd) / [Oddity RC](https://oddityrc.com/products/oddityrc-xi35-pro-1?variant=42274592981142) |
| Motors                        | 2204 1750KV/ 1804 2450KV                                     |                                                              |
| 6S Battery                    |                                                              |                                                              |

Our latest design can be accessed by Fusion360.🔗[Link](https://a360.co/3vK6dJd )  Access code: **hkustUAV**

#### Multi-fisheye Camera Module

ROS wrap driver 🔗[oak_ffc_4p](https://github.com/D2SLAM-Fusion/oak_ffc_4p_ros), which contains hardware information, ROS1 driver and test tools.  

Calibration tool 🔗 [quater-calib](https://github.com/D2SLAM-Fusion/tools-quarterKalibr?tab=readme-ov-file)

#### Jetson Orin

**Environment Info**

![image-20240813153943466](https://khalil-picgo-1321910894.cos.ap-hongkong.myqcloud.com/images/202408131539535.png)

We suggest you follow these settings to avoid conflict (especially CUDA and TensorRT).

#### Nxt-FC

We open-source hardware designs at 🔗[NXT-FC](https://github.com/HKUST-Aerial-Robotics/Nxt-FC).  Nxt-FC supports [PX4](https://github.com/PX4/PX4-Autopilot) and [Ardupilot](https://github.com/ArduPilot/ardupilot) firmware.

Follow the **instructions for setting up the Nxt-FC** part to configure your flight controller.

The PX4 parameter of OmniNxt can be downloaded from [Onedrive]([OmniNxt-03.params](https://hkustconnect-my.sharepoint.com/:u:/g/personal/pliuan_connect_ust_hk/ET4mtqjwqqNOmA8y2WK9rqoBrwlOHXtEKi6IFt4mSGJmqg?e=KJVn5Y)).

## 💾Runtime setup

Our Omni-VINS and Omni-Depth are developed from D2SLAM. Since building the Docker images on the local machine(Jetson Orin) usually takes a long time, we suggest you pull the images from the Docker Hub. If you want to build the Docker image on your local machine, follow the instructions [Build Docker Images On Local Machine](#Build Docker images in local machines).

the docker images structure is as follows:

![docker_image_strcture](https://khalil-picgo-1321910894.cos.ap-hongkong.myqcloud.com/images/202408142216869.png)

#### Step 1 Clone the repository into your local machine

```shell
git clone --branch pr_fix_main https://github.com/HKUST-Aerial-Robotics/D2SLAM.git
```



#### Step 2 Configure your quad-cam parameters and VINS parameters following our template

```shell
cd ./D2SLAM/config/quadcam_drone_nxt_tmp
```

If you have already calibrated your quad fisheye camera set, you can simply replace the files with the same name, which includes:

1. **stereo_calib_n_m_240_320.yaml** (n and m is the camera number; used in Omni-Depth). 
2. **fisheye_cams.yaml**. (used in Omni-VINS)



#### Step 3 Configure ./start_docker.sh script with your local environment.

**./start_docker.sh** is under the **./D2SLAM** directory.

Modify the following parameters with the absolute path under your local host environment.

1. DATA_SET (where the data set is) (Optional)

Then run with the following command under the D2SLAM directory (very important, this will map your D2SLAM dir into the container)：

```shell
./start_docker.sh 1
```



#### Step 4 Launch algorithm modules

***run all algorithm modules together (Omni-VINS & Omni-Depth)***

```shell
## you should under /root/swarm_ws/
source ./devel/setup.bash
roslaunch d2vins quadcam.laucnh
```

***Only launch Omni-VINS. Please remove the nodes in the red box*** 

![image-20240814230125692](https://khalil-picgo-1321910894.cos.ap-hongkong.myqcloud.com/images/202408142301837.png)

```shell
source ./devel/setup.bash
roslaunch d2vins quadcam.laucnh
```

***Only launch Omni-Depth***

```shell
source ./devel/setup.bash
roslaunch quadcam_depth_est depth-node.launch
```

**[Notice]** If you are running Omni-VINS and Omni-Depth for the first time, the initialization process of these two modules would be a little bit long because of the building of the inference engine.



#### Almost done

If everything works well, you will see

![image-20240814230904005](https://khalil-picgo-1321910894.cos.ap-hongkong.myqcloud.com/images/202408142309079.png)

which means Omni-VINS(D2VINS) initialized normally.

Omni-Depth

![image-20240814231049022](https://khalil-picgo-1321910894.cos.ap-hongkong.myqcloud.com/images/202408142310101.png)

### 🖥️Build Docker images in local machines

#### Step 1 Build Jeston_base image

```shell
cd /D2SLA/docker
make jetson_orin_base
```

#### Step 2 Build Jeston Orin image

```shell
cd /D2SLA/docker
make jetson_orin
```

#### 

#### PX4 Controller

We highly suggest you refer to Fast-Lab's PX4 controller [PX4-Control](https://github.com/ZJU-FAST-Lab/Fast-Drone-250/tree/master/src/realflight_modules/px4ctrl)

We also provide our yaw-rotation-free version of  Fast-Lab's PX4 controller [PX4-Control](https://github.com/D2SLAM-Fusion/controller-PX4Control).

Please cite ZJU-Fast-Lab if these modules are useful for your research and project.

#### Flight planer

We modified some of the strategies in the [ego-planner](https://github.com/ZJU-FAST-Lab/ego-planner.git).  Our version is here [ego-planner-omni-modify](https://github.com/D2SLAM-Fusion/planner-EgoPlanner) 

Please cite ZJU-Fast-Lab's [ego-planner](https://github.com/ZJU-FAST-Lab/ego-planner.git) if these modules are useful for your research and project.



## 🔧Troubleshooting



## 💯Acknowledgment

