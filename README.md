![](https://tcs.teambition.net/storage/111t15940627f4ff94eb138dc4e8b2058bb5?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTU5MzU5MDYxMSwiaWF0IjoxNTkyOTg1ODExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQxNTk0MDYyN2Y0ZmY5NGViMTM4ZGM0ZThiMjA1OGJiNSJ9.kH5aHHXGlA_tny5Gm63gtuLZ2x6Ia3PtSKFCyvlhx6c&download=image.png "")

Supervised by  Dr Kerry Nice the University of Melbourne

***

# Summary

- Connectionwith previous research progress

- TMS-Tokyo Dataset

- Transport Mode Detection: MSCNN+

- Experimental Evaluations

***

## Can we use street view to predict  city level travel patterns?

> Goel R, Garcia LMT,Goodman A, Johnson R, Aldred R, et al. (2018) Estimating city-level travel patterns usingstreet imagery: A case study of using Google Street View in Britain. PLOS ONE13(5): e0196521. [__https://doi.org/10.1371/journal.pone.0196521__](https://doi.org/10.1371/journal.pone.0196521)

![](https://tcs.teambition.net/storage/111t723db6e2a19281d286334fbca8b3095f?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTU5MzU5MDYxMSwiaWF0IjoxNTkyOTg1ODExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ3MjNkYjZlMmExOTI4MWQyODYzMzRmYmNhOGIzMDk1ZiJ9.tlmxgZXe3dpLzmL-0nxjLddliloYCnTjJnaaSIqBAXI&download=image.png "")

***

# TMS-Tokyo Dataset

> **Transport Mode Share-Tokyo Dataset**

## Dataset Overview

![](https://tcs.teambition.net/storage/111t8f1849b9eaa6f1c31d7d9923ad08cad9?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTU5MzU5MDYxMSwiaWF0IjoxNTkyOTg1ODExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ4ZjE4NDliOWVhYTZmMWMzMWQ3ZDk5MjNhZDA4Y2FkOSJ9.zycchwVGT5a31GAbob0kwUaUgo9kvvJZLYGLVqiLU2w&download=image.png "")

- Number of Instances: 50827

- Image size: 512*512

- Eight categories: __car, pedestrians, bus, truck, motor, van, cyclist andparked cycle.__

- Division of dataset:

```text
Number of training sam:19803
Number of val sam:6601
Number of test sam:6601
Total: 33461
```

| Dataset                                                     | Annotation method | #Categories | #Instances | #Images |
| ----------------------------------------------------------- | ----------------- | ----------- | ---------- | ------- |
| Tsinghua-Daimler Cyclist Benchmark(Xiaofei Li et al., 2016) | Horizontal BBox   | 7           | 32,361     | 14,674  |
| Cityscape(Cordts et al., 2016)                              | Segmentation      | 30          | NA         | 25,000  |
| KITTI(Geiger et al., 2012)                                  | Segmenation       | 5           | 80,256     | 14,999  |
| Mapillary Vistas(Neuhold et al., 2017)                      | Segmentation      | 66          | 2,000,000  | 25,000  |
| BDD 100K(Yu et al., 2020)                                   | Horizontal BBox   | 10          | 3,300,000  | 100,000 |
| Apolloscapes(Huang et al., 2020)                            | 3D semantic point | 24          | 143,906    | 89,430  |
| TMS-Tokyo (Ours)                                            | Horizontal BBox   | 8           | 50,827     | 33,461  |

***

### Dataset Samples

![](https://tcs.teambition.net/storage/111tcc23eb123de25ba5bca4f6bd62769497?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTU5MzU5MDYxMSwiaWF0IjoxNTkyOTg1ODExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXRjYzIzZWIxMjNkZTI1YmE1YmNhNGY2YmQ2Mjc2OTQ5NyJ9.eLrGro7oSHQ7IFixlvV04Mb4kWFfu-C9DkXXrts6Sdo&download=image.png "")

***

### Statistical Results of transport modes of eight categories in Tokyo

![](https://tcs.teambition.net/storage/111ud34e43bc36eaa0af8d71c54972dcc82f?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MzYwMjIwNywiaWF0IjoxNTkyOTk3NDA3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXVkMzRlNDNiYzM2ZWFhMGFmOGQ3MWM1NDk3MmRjYzgyZiJ9.RkRL-92UojtKxzsnAjHnsG4UbAE710lB3Ro1yQRcqRs&download=Screen+Shot+2020-06-24+at+9.16.42+PM.png "")

# Methodology

## MSCNN+

![](https://tcs.teambition.net/storage/111uf0ae0046556593e79cfd427aad11c35b?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MzYwMjUxOCwiaWF0IjoxNTkyOTk3NzE4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXVmMGFlMDA0NjU1NjU5M2U3OWNmZDQyN2FhZDExYzM1YiJ9.azO1elrcU0fIg2Krl8DZ3Sfmmeq1p515FdVi0splr8U&download=Screen+Shot+2020-06-24+at+9.21.53+PM.png "")

![](https://tcs.teambition.net/storage/111te7ba0dfadc43934daefc7b430f8dccf4?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTU5MzU5MDYxMSwiaWF0IjoxNTkyOTg1ODExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXRlN2JhMGRmYWRjNDM5MzRkYWVmYzdiNDMwZjhkY2NmNCJ9.hcuDN4wKN9Gr1nj6fPfC8vjNRQsWIjIHg095-Lsw4Ts&download=image.png "")

| Detector​                      | AP​  | AP50 | AP75 | APS | APM  | APL  |
| ------------------------------ | ---- | ---- | ---- | --- | ---- | ---- |
| Two-stage method:              |      |      |      |     |      |      |
| Faster R-CNN​                  | 63.4 | 76.6 | 73.7 | 2.5 | 58.7 | 78.2 |
| Libra R-CNN                    | 62.8 | 74.1 | 72.1 | 0.9 | 58.8 | 78.3 |
| One-stage method:              |      |      |      |     |      |      |
| FCOS                           | 61.4 | 78.0 | 74.6 | 3.3 | 59.0 | 74.2 |
| SSD                            | 57.4 | 69.6 | 66.8 | 0.8 | 55.8 | 71.2 |
| Our method:                    |      |      |      |     |      |      |
| MSCNN                          | 61.8 | 79.2 | 74.8 | 5.0 | 58.3 | 74.8 |
| MSCNN+(MSCNN with GA and ATSS) | 68.7 | 82.6 | 78.8 | 4.4 | 62.6 | 84.0 |

***

### Detection Results

![](https://tcs.teambition.net/storage/111ua623937b4ea290233e30691c64c95ece?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MzYwMjY0MiwiaWF0IjoxNTkyOTk3ODQyLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXVhNjIzOTM3YjRlYTI5MDIzM2UzMDY5MWM2NGM5NWVjZSJ9.4ArMNJl3euX9ypBRmJR7BlwcZqkNE8b0OTSObNQxPNQ&download=image.png "")

### 

***

![](https://tcs.teambition.net/storage/111tb2b92298815f8d780a09f8ef9477aee1?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTU5MzU5MDYxMSwiaWF0IjoxNTkyOTg1ODExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXRiMmI5MjI5ODgxNWY4ZDc4MGEwOWY4ZWY5NDc3YWVlMSJ9.wM6T3bcaN9ACLsE4NDj41ed7I_2SqN_DfeeQ3V65Yew&download=image.png "")



__**How to get more labelled datawithout so much manual workload? **__

# Weakly Supervised Deep Learning

![](https://tcs.teambition.net/storage/111t762650f70e10b43f03201b21cf03da38?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTU5MzU5MDYxMSwiaWF0IjoxNTkyOTg1ODExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ3NjI2NTBmNzBlMTBiNDNmMDMyMDFiMjFjZjAzZGEzOCJ9.nR3CYUl7XcE7mIs8FyQczg5MZjnV3xNWhUWZt_Y5vYE&download=image.png "")

***

# My Project Contribution

- Build Pytorch and mmdetection toolbox for efficient experiments

- We proposed anadvanced approach for street-view transport object detection.

- Createa new street-view dataset by street view images for Computer Vision Community

- Proposed Weakly supervised learning method as a direction for future work






