# 项目中文名
基于X模态的跨模态行人重识别
# 项目英文名
XIVReID(Infrared-Visible Cross-Modal Person Re-Identification with an X Modality)
# 作者
Diangang Li, Xing Wei, Xiaopeng Hong, Yihong Gong
# 项目简介
## 1. 功能
跨模态行人重识别
## 2. 性能
在SYSU-MM01和RegDB上达到当前最优性能
在SYSU-MM01上，rank 1 = 49.92%，mAP = 50.73%；
在RegDB上，rank 1 = 62.21%，mAP = 60.18%；
## 3. 评估指标
rank1  mAP
## 4. 使用数据集
SYSU-MM01 
RegDB
# 运行环境与依赖
类别  | 名称 |  版本 |
--------- | --------| --------|
os | ubuntu |16.04.4|
深度学习框架 | pytorch | 1.1.0|

# 输入与输出
|名称|说明|
|输入|红外图像|
|输出|RGB图像|
# 运行方式
在terminal下运行以下命令：
```训练
python tools/train.py --config_file='configs/all.yml' MODEL.DEVICE_ID "('your device id')"  OUTPUT_DIR "('your path to save checkpoints and logs')"
```
```测试
python tools/test-sysu.py --config_file='configs/all.yml' MODEL.DEVICE_ID "('your device id')" TEST.WEIGHT "('your path to trained checkpoints')"
```
