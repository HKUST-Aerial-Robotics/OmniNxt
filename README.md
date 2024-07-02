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

## News

* **[30/06/2024]**: OmniNxt is accepted to IROS 2024.
* The whole project (Hardware and Software) will be released before 15.Aug. ( I am currently cooperating with the hardware producer to make the reproduction easier, and fixing some bug in Omni-VINS to make it easy to be implemented on Jetson Orin NX). If you want early access please contact ()

## Hardware

You can access our latest design by using Fusion360.

Projest link: https://a360.co/3vK6dJd

Access code: hkustUAV

### BOM

All our components can be purchased at Taobao

| Component                     | Specification                                                | Link                                                         |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| ***Quad-Fisheye Camera Set*** |                                                              |                                                              |
| OAK-FFC-4P                    | Camera control board                                         | [Official](https://shop.luxonis.com/products/oak-ffc-4p) / [Taobao](https://detail.tmall.com/item.htm?abbucket=2&id=797243380525&ns=1&priceTId=213e37fe17166914596117457e9698&skuId=5432965948084&spm=a21n57.1.item.4.2d47523c7FgKjv) |
| B0335 (OV9782)                | Camera  modules (210-degree fisheye lens)                    | [Official](https://www.arducam.com/product/arducam-1mp-ov9782-global-shutter-color-mipi-camera-module-22pin-for-depthai-oak-dm1090ffc) / [Taobao](https://item.taobao.com/item.htm?abbucket=2&id=681463610876&ns=1&priceTId=213e376b17166916784225765e28ee&skuId=5076193835807&spm=a21n57.1.item.10.2d47523c7FgKjv) |
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



#### Camera cable SCH

![image-20240526120914708](https://khalil-picgo-1321910894.cos.ap-hongkong.myqcloud.com/images/202405261209056.png)

-----

-----

### Hardware system Overview







### Multi-fisheye camera set

![image-20240703002552632](https://khalil-picgo-1321910894.cos.ap-hongkong.myqcloud.com/images/202407030025811.png)







### Jetson Orin





### Nxt-FC






### Runtime setup

