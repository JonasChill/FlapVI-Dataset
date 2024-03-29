# FlapVI: Visual-Inertial Datasets for Flapping-Wing Aerial Vehicles  Towards Fast Maneuvering with Benchmark Evaluation  

The detailed features of the **FlapVI dataset** can be found in our paper: **“FlapVI: Visual-Inertial Datasets for Flapping-Wing Aerial Vehicles  Towards Fast Maneuvering with Benchmark Evaluation  ”** by Jizhou Jiang, Erzhen Pan, Wenfu Xu, Wei Sun.

Created by Jizhou Jiang, you can contact me through E-mail：22B953004@stu.hit.edu.cn



## Video 

Bilibili：[FlapVI: Visual-Inertial Datasets for Flapping-Wing Aerial Vehicles Towards Fast_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1xK4y1i7yK/?vd_source=da4a4777b9d2f810c870bfee052cae71)

![dataset_features](image/dataset_features.png)



## The Platform ：HIT-Hawk

![platforms_and_avonics](image/platforms_and_avonics.png)

The platform and sensor configuration of the eagle-like large-scale flapping-wing aerial vehicle **HIT-Hawk**, with a wingspan of 1.80 meters and body weight of 770 grams, it can continuously autonomous flight for a maximum of 180 minutes while carrying payload equivalent to 100% of its weight, with a takeoff weight of 1550 grams.



## ROS Topic (Synchronized)

|      | Description                                                  | Topic                         | Type                            |
| :--: | :----------------------------------------------------------- | ----------------------------- | ------------------------------- |
|  1   | Realsense D435 depth image                                   | /camera/depth/image_rect_raw  | sensor_msgs/Image               |
|  2   | Realsense D435 left gray image                               | /camera/infra1/image_rect_raw | sensor_msgs/Image               |
|  3   | Realsense D435 right gray image                              | /camera/infra2/image_rect_raw | sensor_msgs/Image               |
|  4   | Realsense D435 color image                                   | /camera/color/image_raw       | sensor_msgs/Image               |
|  5   | The build-in IMU of D435i                                    | /camera/imu                   | sensor_msgs/Imu                 |
|  6   | The filltered fusion IMU data from CUAV V5+                  | /mavros/imu/data              | sensor_msgs/Imu                 |
|  7   | Ephemeris data for GLONASS (GLO) satellites                  | /ublox_driver/glo_ephem       | gnss_comm/GnssGloEphemMsg       |
|  8   | Range measurement data of RTK                                | /ublox_driver/range_meas      | gnss_comm/GnssMeasMsg           |
|  9   | The latitude, longitude, and altitude coordinates of the receiver (LLA stands for Longitude, Latitude, and Altitude) | /ublox_driver/receiver_lla    | sensor_msgs/NavSatFix           |
|  10  | The Position, Velocity, and Time (PVT) data of the RTK receiver | /ublox_driver/receiver_pvt    | gnss_comm/GnssPVTSolnMsg        |
|  11  | The data related to time pulse information in the u-blox driver | /ublox_driver/time_pulse_info | gnss_comm/GnssTimePulseInfoMsg  |
|  12  | Linktrack P UWB positioning tag data（trasn. and rota.）     | /nlink_linktrack_tagframe0    | nlink_parser/LinktrackTagframe0 |



## Dataset Sequences list

We provide the option to download the raw dataset files and the corresponding extracted motion trajectory files, both saved in rosbag format. The download links for each sequence and trajectory are attached in the table. If the links in the table cannot be directly opened, download readme file and copy the corresponding cloud storage link and paste it into your browser. If neither of these methods works, we also provide links to the cloud storage containing all the datasets:
**quark cloud link:**https://pan.quark.cn/s/6ed823d41de0

|  #   |                 sequences (link)                  |    camera perspective     | illumination |                       trajectory(link)                       | length(m) | duration(s) | max ground speed(m/s) | air speed(m/s) | groundtruth |   level   |
| :--: | :-----------------------------------------------: | :-----------------------: | :----------: | :----------------------------------------------------------: | :-------: | :---------: | :-------------------: | :------------: | :---------: | :-------: |
|  1   | [Outdoor_01](https://pan.quark.cn/s/a176ecdb9dcd) | 45 degree downward facing | bright scene |         [oval](https://pan.quark.cn/s/2c497376fac8)          |  910.18   |     156     |         12.02         |      0.36      |      ✔      |  medium   |
|  2   | [Outdoor_02](https://pan.quark.cn/s/88513081e6f9) | 45 degree downward facing | bright scene |         [oval](https://pan.quark.cn/s/e654374c453d)          |  839.24   |     150     |         13.40         |      0.39      |      ✔      |  medium   |
|  3   | [Outdoor_03](https://pan.quark.cn/s/2e671803ab9e) |      Forward  facing      | bright scene |         [oval](https://pan.quark.cn/s/a2f07f9a35ea)          |  1150.60  |     197     |         13.47         |      1.59      |      ✔      | difficult |
|  4   | [Outdoor_04](https://pan.quark.cn/s/4badfa1e3cc8) | 45 degree downward facing | bright scene |      [8-character](https://pan.quark.cn/s/6415f87b77a9)      |  808.28   |     159     |         10.04         |      1.68      |      ✔      |  medium   |
|  5   | [Outdoor_05](https://pan.quark.cn/s/4b0f4afa33f8) | 45 degree downward facing | bright scene |      [8-character](https://pan.quark.cn/s/03ed33708d70)      |  963.88   |     155     |         11.74         |      1.53      |      ✔      |  medium   |
|  6   | [Outdoor_06](https://pan.quark.cn/s/cf41e2edac14) |      Forward  facing      | bright scene |      [8-character](https://pan.quark.cn/s/b0bc2f87f21f)      |  575.89   |     125     |         11.09         |      1.75      |      ✔      | difficult |
|  7   | [Outdoor_07](https://pan.quark.cn/s/fd8b2cdf1822) | 45 degree downward facing | bright scene | [Fast Flapping and Gliding Switch](https://pan.quark.cn/s/d033837a3f6c) |  377.71   |     67      |         12.29         |      1.62      |      ✔      |  medium   |
|  8   | [Outdoor_08](https://pan.quark.cn/s/a2c003ba35b5) |      Forward  facing      | bright scene | [Fast Flapping and Gliding Switch](https://pan.quark.cn/s/b5b16b3f5ea0) |  104.10   |     41      |         9.87          |      1.64      |      ✔      |  medium   |
|  9   | [Outdoor_09](https://pan.quark.cn/s/d90d8e54409b) | 45 degree downward facing | dark  scene  |                            random                            |   78.15   |     26      |         8.34          |      1.34      |      ✔      | difficult |
|  10  | [Outdoor_10](https://pan.quark.cn/s/86f89110fb4d) | 45 degree downward facing | dark  scene  |                            random                            |  105.86   |    31.5     |         7.87          |      1.47      |      ✔      | difficult |
|  11  | [Outdoor_11](https://pan.quark.cn/s/d94616bb429b) |      Forward  facing      | dark  scene  |                            random                            |   94.31   |    34.4     |         8.92          |      1.44      |      ✔      | difficult |
|  12  | [Outdoor_12](https://pan.quark.cn/s/6ae1433a1104) |      Forward  facing      | dark  scene  |                            random                            |   98.82   |     69      |         9.27          |      1.51      |      ✔      | difficult |
|  13  | [Indoor_13](https://pan.quark.cn/s/a176ecdb9dcd)  | 45 degree downward facing | bright scene |         [oval](https://pan.quark.cn/s/08baf75cba0a)          |   43.25   |    17.6     |         8.94          |      NaN       |      ✔      |  medium   |
|  14  | [Indoor 14](https://pan.quark.cn/s/13da836478cf)  | 45 degree downward facing | bright scene |         [oval](https://pan.quark.cn/s/1f5645dbc845)          |  163.44   |    36.3     |         12.17         |      NaN       |      ✔      | difficult |
|  15  | [Indoor 15](https://pan.quark.cn/s/8ff207e19441)  |      Forward  facing      | bright scene |         [oval](https://pan.quark.cn/s/b82f1bfc5536)          |   83.34   |    29.3     |         8.81          |      NaN       |      ✔      | difficult |
|  16  | [Indoor 16](https://pan.quark.cn/s/45fcd10333fe)  | 45 degree downward facing | dark  scene  |        [random](https://pan.quark.cn/s/7a72ac536e98)         |   55.28   |    13.4     |         11.85         |      NaN       |      ✔      | difficult |
|  17  | [Indoor 17](https://pan.quark.cn/s/bafbca7367c8)  |      Forward  facing      | dark  scene  |        [random](https://pan.quark.cn/s/cb078b250cb6)         |   51.14   |    14.6     |         11.99         |      NaN       |      ✔      | difficult |



## Benchmark comprasion

In our letter, we compared a total of four SOTA stereo VIO frameworks, the corresponding GitHub links are as follows. If you need to compare other algorithms, you can config the algorithm based on the calibr file.

1.ORB-SLAM3 [UZ-SLAMLab/ORB_SLAM3: ORB-SLAM3: An Accurate Open-Source Library for Visual, Visual-Inertial and Multi-Map SLAM (github.com)](https://github.com/UZ-SLAMLab/ORB_SLAM3)

2.VINS-FUISON [HKUST-Aerial-Robotics/VINS-Fusion: An optimization-based multi-sensor state estimator (github.com)](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion)

3.MSCKF-VIO [KumarRobotics/msckf_vio: Robust Stereo Visual Inertial Odometry for Fast Autonomous Flight (github.com)](https://github.com/KumarRobotics/msckf_vio)

4.GVINS [HKUST-Aerial-Robotics/GVINS: Tightly coupled GNSS-Visual-Inertial system for locally smooth and globally consistent state estimation in complex environment. (github.com)](https://github.com/HKUST-Aerial-Robotics/GVINS)



## Requirement(recommend)

To ensure the proper functioning of the dataset, we recommend the following environmental configuration.If you need to run a VIO (Visual-Inertial Odometry) algorithm, please refer to its corresponding requirements.

1.ROS 20.04 Noetic full-desktop

2.Onboard-sensors SDK(sensor configuration file)

3.Python 3.8 & 2.7





