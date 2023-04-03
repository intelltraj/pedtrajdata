**数据格式**

数据文件名格式：地图编号+用户 id+年月日时分秒



采集数据以 JSON 对象形式保存。大致结构如下：

- **beaconScanList**：表示 beacon 扫描列表，列表中每个元素代表一次 beacon 扫描数据：

  -  **beaconList**: 此次扫描到的 beacon 列表，列表中每个元素代表一个

    beacon: 

    - **major**: major 号
    - **minor**: minor 号
    - **rssi**: 信号强度值
    - **mac**: MAC(可选) 
    - **uuid**: UUID(可选) 
    - **locPoint**: 此次扫描对应的定位点

  -  **timestamp**: 此次扫描的时间戳

- 

-  **startPoint**： 记录用户手动在地图上标记的数据采集起始位置点(可选) 

- **accelerationList**: 三轴加速度计数据列表, 记录 x, y, z 三个轴上的加速度计读数(m/s²) 

- **rotationRateList**: 陀螺仪数据列表, 记录三个轴上的角速度

- **orientationList**: 方位角数据列表，其中 alpha 为朝向(设备当前指南针方向与磁北向之间的角度。如果设备的上边缘面朝磁北向，则方位角为 0 度；如果上边缘朝南，则方位角为 180 度。与之类似，如果上边缘朝东，则方位角为 90 度；如果上边缘朝西，则方位角为 270 度。)  

- 更多其他数据...



**另外，可以按需要在 JSON 对象的最外层可以添加其他数据字段。 具体格式如下所示：**

采集数据以 JSON 对象形式保存。大致结构如下：

- beaconScanList：表示 beacon 扫描列表，列表中每个元素代表一次 beacon 扫描数据：
- beaconList: 此次扫描到的 beacon 列表，列表中每个元素代表一个 beacon: 
- major: major 号
- minor: minor 号
- rssi: 信号强度值
- mac: MAC(可选)
- uuid: UUID(可选)
- locPoint: 此次扫描对应的定位点
- timestamp: 此次扫描的时间戳
- startPoint：: 记录用户手动在地图上标记的数据采集起始位置点(可选)accelerationList: 三轴加速度计数据列表, 记录 x, y, z 三个轴上的加速度计读数(m/s²)
- rotationRateList: 陀螺仪数据列表, 记录三个轴上的角速度
- orientationList: 方位角数据列表，其中 alpha 为朝向(设备当前指南针方向与磁北向之间的角度。如果设备的上边缘面朝磁北向，则方位角为 0 度；如果上边缘朝南，则方位角为 180 度。与之类似，如果上边缘朝东，则方位角为 90 度；如果上边缘朝西，则方位角为 270 度。)
- 更多其他数据... 



另外，可以按需要在 JSON 对象的最外层可以添加其他数据字段。

具体格式如下所示：

```
{

    "beaconScanList": [

        {

            "beaconList": [

                {

                    "major": 10085,

                    "minor": 59810,

                    "rssi": -57,

                    "txPower": -59,

                    "mac": "AC:23:3F:24:E7:3F",

                    "uuid": "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                },

                {

                    "major": 50211,

                    "minor": 1018,

                    "rssi": -60,

                    "txPower": -59,

                    "mac": "C2:02:BE:00:07:63",

                    "uuid": "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                }

            ], "locPoint": {
                "x": 12686092.6611092, "y": 2559453.87022379, "fnum":

                    2
            },

            "timestamp": 1615261767824

        },

        {

            "beacons": [

                {

                    "major": 10085,

                    "minor": 59810,

                    "rssi": -60

                },

                {

                    "major": 50211,

                    "minor": 1018,

                    "rssi": -61

                }

            ],

            "locPoint": {
                "x": 12686092.6611092, "y": 2559453.87022379, "fnum":

                    2
            },

            "timestamp": 1615261768824

        }

    ],

        "startPoint": { "x": 12629799.73, "y": 2580119.303, "fnum": 2, "bid": "10007" },

    "accelerationList": ["x, y, z, timestamp", "x, y, z, timestamp"],

        "rotationRateList": ["alpha, beta, gama, timestamp", "alpha, beta, gama, 
    
    timestamp"], 
    
    "orientationList": ["alpha, beta, gama, timestamp", "alpha, beta, gama, 
    
    timestamp"], 
    
    "...": "..."
    
    } {

    "beaconScanList": [

        {

            "beaconList":

                [

                    {

                        "major": 10085,

                        "minor": 59810,

                        "rssi": -57,

                        "txPower": -59,

                        "mac": "AC:23:3F:24:E7:3F",

                        "uuid": "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                    },

                    {

                        "major": 50211,

                        "minor": 1018,

                        "rssi": -60,

                        "txPower": -59,

                        "mac": "C2:02:BE:00:07:63",

                        "uuid":

                            "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                    }

                ],

            "locPoint": {
                "x": 12686092.6611092, "y": 2559453.87022379, "fnum":

                    2
            },

            "timestamp": 1615261767824

        },

        {

            "beacons": [

                {

                    "major":

                        10085,

                    "minor": 59810,

                    "rssi":

                        -60

                },

                {

                    "major": 50211,

                    "minor": 1018,

                    "rssi":

                        -61

                }

            ],

            "locPoint": {
                "x":

                    12686092.6611092, "y": 2559453.87022379, "fnum": 2
            },

            "timestamp":

                1615261768824

        }

    ],

        "startPoint":

    { "x": 12629799.73, "y": 2580119.303, "fnum": 2, "bid": "10007" },

    "accelerationList":

    ["x, y, z, timestamp", "x, y, z, timestamp"],

        "rotationRateList": ["alpha, beta, gama, 
    
    timestamp", "alpha, beta, gama, timestamp"], 
    
    "orientationList": ["alpha, beta, gama, 
    
    timestamp", "alpha, beta, gama, timestamp"], 
    
    "...": "..."}
```



**Data Format**

Data file name format: map number + user id + year, month, day, hour, minute, second



The collected data is saved in the form of JSON object. The general structure is as follows:

- **beaconScanList**: Indicates the beacon scan list, each element in the list represents a beacon scan data:

   - **beaconList**: The list of beacons scanned this time, each element in the list represents a

     beacon:

     - **major**: major number
     - **minor**: minor number
     - **rssi**: signal strength value
     - **mac**: MAC (optional)
     - **uuid**: UUID (optional)
     - **locPoint**: The location point corresponding to this scan

   - **timestamp**: The timestamp of this scan

-

- **startPoint**: Record the starting point of data collection manually marked on the map by the user (optional)

- **accelerationList**: Three-axis accelerometer data list, record the accelerometer readings on the three axes of x, y, z (m/s²)

- **rotationRateList**: Gyroscope data list, record angular velocity on three axes

- **orientationList**: A list of azimuth angle data, where alpha is the orientation (the angle between the current compass direction of the device and the magnetic north direction. If the upper edge of the device faces magnetic north, the azimuth is 0 degrees; if the upper edge faces South, the azimuth is 180 degrees. Similarly, if the upper edge faces east, the azimuth is 90 degrees; if the upper edge faces west, the azimuth is 270 degrees.)

- more other data...



**In addition, other data fields can be added to the outermost layer of the JSON object as needed. The specific format is as follows:**

The collected data is saved in the form of JSON object. The general structure is as follows:

- beaconScanList: Indicates the beacon scan list, each element in the list represents a beacon scan data:
- beaconList: The list of beacons scanned this time, each element in the list represents a beacon:
- major: major number
- minor: minor number
- rssi: signal strength value
- mac: MAC (optional)
- uuid: UUID (optional)
- locPoint: The locating point corresponding to this scan
- timestamp: The timestamp of this scan
- startPoint:: record the start point of data collection manually marked on the map by the user (optional) accelerationList: a list of three-axis accelerometer data, record the accelerometer readings on the three axes of x, y, and z (m/s²)
- rotationRateList: gyroscope data list, record angular velocity on three axes
- orientationList: Azimuth data list, where alpha is the orientation (the angle between the current compass direction of the device and the magnetic north. If the upper edge of the device faces magnetic north, the azimuth is 0 degrees; if the upper edge faces south, the azimuth The angle is 180 degrees. Similarly, if the upper edge faces east, the azimuth is 90 degrees; if the upper edge faces west, the azimuth is 270 degrees.)
- more other data...



In addition, other data fields can be added to the outermost layer of the JSON object as needed.

The specific format is as follows:

```
{

    "beaconScanList": [

        {

            "beaconList": [

                {

                    "major": 10085,

                    "minor": 59810,

                    "rssi": -57,

                    "txPower": -59,

                    "mac": "AC:23:3F:24:E7:3F",

                    "uuid": "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                },

                {

                    "major": 50211,

                    "minor": 1018,

                    "rssi": -60,

                    "txPower": -59,

                    "mac": "C2:02:BE:00:07:63",

                    "uuid": "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                }

            ], "locPoint": {
                "x": 12686092.6611092, "y": 2559453.87022379, "fnum":

                    2
            },

            "timestamp": 1615261767824

        },

        {

            "beacons": [

                {

                    "major": 10085,

                    "minor": 59810,

                    "rssi": -60

                },

                {

                    "major": 50211,

                    "minor": 1018,

                    "rssi": -61

                }

            ],

            "locPoint": {
                "x": 12686092.6611092, "y": 2559453.87022379, "fnum":

                    2
            },

            "timestamp": 1615261768824

        }

    ],

        "startPoint": { "x": 12629799.73, "y": 2580119.303, "fnum": 2, "bid": "10007" },

    "accelerationList": ["x, y, z, timestamp", "x, y, z, timestamp"],

        "rotationRateList": ["alpha, beta, gama, timestamp", "alpha, beta, gama, 
    
    timestamp"], 
    
    "orientationList": ["alpha, beta, gama, timestamp", "alpha, beta, gama, 
    
    timestamp"], 
    
    "...": "..."
    
    } {

    "beaconScanList": [

        {

            "beaconList":

                [

                    {

                        "major": 10085,

                        "minor": 59810,

                        "rssi": -57,

                        "txPower": -59,

                        "mac": "AC:23:3F:24:E7:3F",

                        "uuid": "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                    },

                    {

                        "major": 50211,

                        "minor": 1018,

                        "rssi": -60,

                        "txPower": -59,

                        "mac": "C2:02:BE:00:07:63",

                        "uuid":

                            "FDA50693-A4E2-4FB1-AFCF-C6EB07647825"

                    }

                ],

            "locPoint": {
                "x": 12686092.6611092, "y": 2559453.87022379, "fnum":

                    2
            },

            "timestamp": 1615261767824

        },

        {

            "beacons": [

                {

                    "major":

                        10085,

                    "minor": 59810,

                    "rssi":

                        -60

                },

                {

                    "major": 50211,

                    "minor": 1018,

                    "rssi":

                        -61

                }

            ],

            "locPoint": {
                "x":

                    12686092.6611092, "y": 2559453.87022379, "fnum": 2
            },

            "timestamp":

                1615261768824

        }

    ],

        "startPoint":

    { "x": 12629799.73, "y": 2580119.303, "fnum": 2, "bid": "10007" },

    "accelerationList":

    ["x, y, z, timestamp", "x, y, z, timestamp"],

        "rotationRateList": ["alpha, beta, gama, 
    
    timestamp", "alpha, beta, gama, timestamp"], 
    
    "orientationList": ["alpha, beta, gama, 
    
    timestamp", "alpha, beta, gama, timestamp"], 
    
    "...": "..."}
```

