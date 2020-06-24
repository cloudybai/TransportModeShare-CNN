# TransportModeShare-CNN
# Object detection based on deep convolutional neural networks for transportation mode share analysis
![](https://tcs.teambition.net/storage/111t15940627f4ff94eb138dc4e8b2058bb5?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMDU4NywiaWF0IjoxNTkwMzI1Nzg3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQxNTk0MDYyN2Y0ZmY5NGViMTM4ZGM0ZThiMjA1OGJiNSJ9.qiA2foyhIu472kdWkAhMRQTfPQePQ0Eu7situfLE9WY&download=image.png "")

Supervised by  Dr Kerry Nice， the University of Melbourne
School of Computing and Information Systems, Melbourne School of Engineering
## This Project is under Transport, Health, Urban Design Research Hub (THUD), Melbourne School of Design.
***

# Summary

- Connection with previous research progress

- Transport Object Detector: MSCNN+

- TMS-Dataset

- Future Work

***

## Can we use streetview to predict  city leveltravel patterns?

![](https://tcs.teambition.net/storage/111t688ba44e3506696a57c023890a2cb7b2?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMDc3MCwiaWF0IjoxNTkwMzI1OTcwLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ2ODhiYTQ0ZTM1MDY2OTZhNTdjMDIzODkwYTJjYjdiMiJ9.b65R9fz5c40KHRkTpFM_NFQMtVxt9ZxYWh2kEm8QEd8&download=image.png "")

> Goel R, Garcia LMT,Goodman A, Johnson R, Aldred R, et al. (2018) Estimating city-level travel patterns usingstreet imagery: A case study of using Google Street View in Britain. PLOS ONE13(5): e0196521. [__https://doi.org/10.1371/journal.pone.0196521__](https://doi.org/10.1371/journal.pone.0196521)

![](https://tcs.teambition.net/storage/111t723db6e2a19281d286334fbca8b3095f?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMDgwMSwiaWF0IjoxNTkwMzI2MDAxLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ3MjNkYjZlMmExOTI4MWQyODYzMzRmYmNhOGIzMDk1ZiJ9.dcVpMhUa4L3xYkDonk36n4mop00xAjDYBb8cBIBjR-I&download=image.png "")

## What is Convolutional NeuralNetworks?

[__https://github.com/cloudybai/cnn-explainer#cnn-explainer__](https://github.com/cloudybai/cnn-explainer#cnn-explainer)



***

## My Project Structure

- Part1:  Single-class transport objectdetection (Cyclists)

- Part2: Multi-classtransport object detection

|                       |   Single Class Object Detection   |   Multi Class Object Detection   |
| --------------------- | --------------------------------- | -------------------------------- |
|   Category            |   Cyclists                        |   8  classes road users          |
|   Dataset             |   Tsinghua-Daimler                |   GSV  Tokyo                     |
|   CNN  Model          |   ATSS                            |   Guided  Anchoring              |
|   Samples  Location   |   Beijing                         |   Tokyo                          |
|   Performance(mAP)    |   78%                             |   85.7%                          |



***

## ToolBox

[__https://github.com/cloudybai/mmdetection__](https://github.com/cloudybai/mmdetection)

***

### Part 1 Single-class Cyclist Detection

> Tsinghua-DaimlerCyclist Dataset

![](https://tcs.teambition.net/storage/111t8d0ffa89e172058911462adcf2ab6035?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTExNiwiaWF0IjoxNTkwMzI2MzE2LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ4ZDBmZmE4OWUxNzIwNTg5MTE0NjJhZGNmMmFiNjAzNSJ9.1MqqbPVkRoWwgPaCdvKzfCYXsm6ah6E3e7px5xM0tds&download=image.png "")

|   Dataset  Statistics   |   Training   |   Validation   |   Test    |   Non-VRU   |   Total   |
| ----------------------- | ------------ | -------------- | --------- | ----------- | --------- |
|   Image  Frames         |   9741       |   1019         |   2914    |   1000      |   14674   |
|   Cyclist  BBs          |   16202      |   1314         |   4657    |   0         |   22173   |
|   Pedestrain  BBs       |   0          |   1541         |   7401    |   0         |   8942    |
|   Other  rider BBs      |   0          |   190          |   1105    |   0         |   1295    |
|   Total  BBs            |   16202      |   3045         |   13163   |   0         |   32410   |

### Methodology

ATSS (Adaptive Training SampleSelection)

![](https://tcs.teambition.net/storage/111tcb5fad2fda01e90d1801831e3a7a9977?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTE1MywiaWF0IjoxNTkwMzI2MzUzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXRjYjVmYWQyZmRhMDFlOTBkMTgwMTgzMWUzYTdhOTk3NyJ9.4OLBzvdQS7l0JIFAW0MxNBChKxYUa9WMpSIaanh37Dk&download=image.png "")

***

### Part2: Multi-class transport object detection

![](https://tcs.teambition.net/storage/111tcc23eb123de25ba5bca4f6bd62769497?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTE5MiwiaWF0IjoxNTkwMzI2MzkyLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXRjYzIzZWIxMjNkZTI1YmE1YmNhNGY2YmQ2Mjc2OTQ5NyJ9.y7nn4gUOQ49IIpqd5Tta4yEP48FZP76v47cRtZ9G2SM&download=image.png "")

### GSV Tokyo Dataset Overview

- Number of Instances: 50827

- Image size: 512*512

- Eight categories: __car, pedestrians, bus, truck, motor, van, cyclist andparked cycle.__

- Division of dataset

- Number of training sam:19803

- Number of val sam:6601

- Number of test sam:6601

- Total: 33461

![](https://tcs.teambition.net/storage/111t8f1849b9eaa6f1c31d7d9923ad08cad9?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTI5OCwiaWF0IjoxNTkwMzI2NDk4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ4ZjE4NDliOWVhYTZmMWMzMWQ3ZDk5MjNhZDA4Y2FkOSJ9.EyCdW_PjgUq_g4VFBEBkM3OvfJfXBTC97LODXN-yXqY&download=image.png "")

***

> **Guided Anchoring**

![](https://tcs.teambition.net/storage/111te7ba0dfadc43934daefc7b430f8dccf4?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTMzNSwiaWF0IjoxNTkwMzI2NTM1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXRlN2JhMGRmYWRjNDM5MzRkYWVmYzdiNDMwZjhkY2NmNCJ9.9jnzToWvPy5fJI3QVCAHamIy13RNYx-I8ufEpqXN0x4&download=image.png "")

![](https://tcs.teambition.net/storage/111t2b95eff5b4dd96085ff502dab0d9c6ba?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTM1NCwiaWF0IjoxNTkwMzI2NTU0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQyYjk1ZWZmNWI0ZGQ5NjA4NWZmNTAyZGFiMGQ5YzZiYSJ9.SLv2BnZ-ke5KP9kj-mwXHioRJwd_GNtOuoY8jaOlxHA&download=image.png "")

***

|                       |   mAP     |   Time per image/s   |   Issues                                                                     |
| --------------------- | --------- | -------------------- | ---------------------------------------------------------------------------- |
|   Faster R-CNN        |   0.832   |   0.08935            |   •Multiple detection frames for the  same target  •few GT frames detected   |
|   ATSS                |   0.848   |   0.06860            |   Detected unlabeled targets                                                 |
|   Libra R-CNN         |   0.839   |   0.15861            |   Few GT frames detected                                                     |
|   Guided  Anchoring   |   0.857   |   0.12988            |   Detected unlabeled targets                                                 |

***

## Exsiting Issues and discussions:

![](https://tcs.teambition.net/storage/111t76d7b876b6488d8a250fcf55f23b1458?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTQzNSwiaWF0IjoxNTkwMzI2NjM1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ3NmQ3Yjg3NmI2NDg4ZDhhMjUwZmNmNTVmMjNiMTQ1OCJ9._g9Y26ClSspwXtJOtEGjkKICkGBzcUhh8K8Nyde17k8&download=image.png "")



![](https://tcs.teambition.net/storage/111tb2b92298815f8d780a09f8ef9477aee1?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTUyMSwiaWF0IjoxNTkwMzI2NzIxLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXRiMmI5MjI5ODgxNWY4ZDc4MGEwOWY4ZWY5NDc3YWVlMSJ9.pYTyc--dv2VXDFQ9WegJt_P5lkVNZlVBIfbSb27D1-4&download=image.png "")



__**How to get more labelled datawithout so much manual workload? **__

# Weakly Supervised Deep Learning

![](https://tcs.teambition.net/storage/111t762650f70e10b43f03201b21cf03da38?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVkZGRmZjcxMzMwODBkMDAwMTZlODg2ZSIsImV4cCI6MTU5MDkzMTU2NCwiaWF0IjoxNTkwMzI2NzY0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzExMXQ3NjI2NTBmNzBlMTBiNDNmMDMyMDFiMjFjZjAzZGEzOCJ9.sYOGymMryxSFWiwGmAt7a7jojMtzd35AopZ5U0SgWcg&download=image.png "")

***

# My Project Contribution

- Build Pytorch and mmdetection toolbox for efficient experiments

- We proposed anadvanced approach for street-view transport object detection.

- Createa new street-view dataset by GSV Tokyo images for Computer Vision Community

- Proposed Weakly supervised learning method as a direction for future work



