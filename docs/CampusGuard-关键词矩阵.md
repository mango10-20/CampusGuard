# CampusGuard 文献检索关键词矩阵

> 用途：为 CampusGuard 项目做文献综述时的检索词清单。
> 用法：每条概念给出一组同义词，检索时按 `A OR B OR C` 组合（同义词取并集），
> 不同概念之间按 `AND` 连接（交集），逐层缩小到目标文献。
> 建议数据库：Web of Science、Scopus、IEEE Xplore、ACM DL、Google Scholar、知网 / 万方 / 维普。
> 注：英文条目在 WoS / IEEE 里检索，中文条目在知网 / 万方里检索，两套词表并行使用。

---

## 0. 检索组合示例（先看这个）

| 你想找 | 检索式 |
| --- | --- |
| 火焰烟雾检测的整体进展 | `(fire OR flame) AND (smoke) AND (detection OR recognition) AND (deep learning OR YOLO OR CNN)` |
| 跌倒检测的方法对比 | `(fall detection) AND (vision-based OR video-based OR camera) AND (deep learning OR pose estimation OR keypoint)` |
| 禁区入侵 / 越界检测 | `(intrusion detection) AND (video surveillance) AND (virtual fence OR tripwire OR region of interest) AND (deep learning)` |
| 车辆违停检测 | `(illegal parking OR illegal stopping) AND (detection) AND (surveillance OR deep learning)` |
| 电子围栏 / 多边形区域 | `(electronic fence OR virtual fence OR geofence OR ROI polygon)` AND `(video analytics)` |
| 多目标跟踪 | `(multi-object tracking OR MOT) AND (ByteTrack OR tracking-by-detection) AND (surveillance)` |
| 单帧误报抑制 | `(false alarm reduction OR false positive suppression) AND (multi-frame OR temporal confirmation OR tracking) AND (video surveillance)` |
| 行为识别（后续拓展） | `(action recognition OR human behavior analysis OR anomaly detection) AND (video) AND (deep learning)` |

---

## 1. 领域与系统层

**核心概念**：视频监控 / 智能视频分析 / 校园安全 / 公共安全监控

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 视频监控 | video surveillance | CCTV, surveillance video, video monitoring, security camera network, IP camera system | 视频监控、安防监控、监控系统、闭路电视、摄像监控 |
| 智能视频分析 | intelligent video analytics (IVA) | video content analysis (VCA), smart surveillance, automated video analysis, video understanding, visual analytics | 智能视频分析、视频内容分析、视频理解、智能监控、视觉分析 |
| 校园安全 | campus security | school safety, campus safety, university security, educational institution security | 校园安全、学校安全、高校安全、校园安防 |
| 公共安全监控 | public safety surveillance | public security monitoring, urban surveillance, safe city, smart city security | 公共安全监控、城市安防、平安城市、智慧城市安防 |
| 风险预警 / 预警系统 | early warning system | risk alerting, alert generation, alarm system, pre-warning | 预警系统、风险预警、告警系统、报警系统 |
| 人机协同 | human-machine collaboration | human-in-the-loop, human-AI collaboration, human-machine symbiosis | 人机协同、人在回路、人机协作 |
| 监控摄像头网络 | camera network | multi-camera system, distributed cameras, camera topology | 摄像头组网、多摄像头系统、监控组网 |

---

## 2. 目标检测层（视觉算法核心）

**核心概念**：目标检测 / YOLO / 卷积神经网络

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 目标检测 | object detection | target detection, object localization, detection and recognition | 目标检测、物体检测、目标识别 |
| YOLO 系列 | YOLO (You Only Look Once) | YOLOv3/v5/v8, YOLOv8-seg, single-stage detector, real-time detector | YOLO 算法、单阶段检测器、实时检测模型 |
| 深度学习 | deep learning (DL) | deep neural network (DNN), representation learning, end-to-end learning | 深度学习、深度神经网络、表征学习 |
| 卷积神经网络 | convolutional neural network (CNN) | ConvNet, backbone network, ResNet, VGG, CSPDarknet | 卷积神经网络、骨干网络 |
| 两阶段检测器 | two-stage detector | Faster R-CNN, R-CNN, region proposal network (RPN), Cascade R-CNN | 两阶段检测器、候选区域网络 |
| Transformer 检测器 | transformer-based detector | DETR, Deformable DETR, DINO, Swin Transformer, ViT | Transformer 检测、注意力检测器 |
| 轻量化模型 | lightweight model | MobileNet, ShuffleNet, YOLO-nano, model pruning, knowledge distillation | 轻量化模型、模型压缩、剪枝、知识蒸馏 |
| 迁移学习 / 微调 | transfer learning | fine-tuning, domain adaptation, pretrained weights | 迁移学习、微调、域自适应、预训练权重 |
| 骨干 / 颈部 / 头部 | backbone-neck-head | FPN, PANet, feature pyramid, detection head | 特征金字塔、检测头、颈部网络 |
| 非极大值抑制 | non-maximum suppression (NMS) | Soft-NMS, IoU threshold, post-processing | 非极大值抑制、后处理 |
| 单阶段 vs 双阶段 | one-stage vs two-stage | anchor-based vs anchor-free, CenterNet, FCOS | 单阶段与两阶段、锚框与无锚框 |

---

## 3. 分割与姿态层（重叠判断与跌倒增强）

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 实例分割 | instance segmentation | Mask R-CNN, YOLOv8-seg, segmentation mask, panoptic segmentation | 实例分割、掩膜分割、全景分割 |
| 语义分割 | semantic segmentation | FCN, U-Net, DeepLab, pixel-level classification | 语义分割、像素级分类 |
| 人体姿态估计 | human pose estimation | pose estimation, skeleton extraction, YOLO-Pose, OpenPose, HRNet | 人体姿态估计、骨架提取、关键点检测 |
| 人体关键点 | human keypoints | joints, skeleton points, landmark detection, COCO keypoints | 人体关键点、关节节点、骨骼点 |
| 姿态识别（用于跌倒） | posture recognition | body posture classification, lying detection, pose-based action | 姿态识别、体态识别、卧姿检测 |
| 检测框宽高比 | bounding box aspect ratio | bbox ratio, box geometry, shape feature | 检测框宽高比、边框几何特征 |

---

## 4. 跟踪层

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 多目标跟踪 | multi-object tracking (MOT) | multi-target tracking (MTT), multiple object tracking, MOT | 多目标跟踪、多目标追踪 |
| 检测跟踪范式 | tracking-by-detection | TBD, detect-then-track, joint detection and tracking | 先检测后跟踪、检测跟踪一体化 |
| ByteTrack | ByteTrack | SORT, DeepSORT, OC-SORT, BoT-SORT, FairMOT | 目标跟踪算法、SORT 系列 |
| 数据关联 | data association | Hungarian algorithm, assignment problem, matching, IoU matching | 数据关联、匈牙利算法、匹配 |
| 卡尔曼滤波 | Kalman filter | motion model, state estimation, prediction model | 卡尔曼滤波、状态估计、运动模型 |
| 目标 ID 保持 | identity preservation | ID switch, ID consistency, re-identification (ReID), tracklet | 目标编号保持、ID 切换、重识别、轨迹片段 |
| 轨迹分析 | trajectory analysis | path analysis, motion trajectory, track history | 轨迹分析、路径分析、运动轨迹 |

---

## 5. 事件检测层（本项目的核心痛点）

**这是文档里最"不够主流叫法"的一块，检索时要注意：厂里的叫法（违停、占用、入侵）不是学术词，学术对应词在右边。**

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 视频事件检测 | video event detection | event detection, complex event processing (CEP), event recognition | 视频事件检测、事件识别、复合事件检测 |
| 时序 / 多帧确认 | temporal confirmation | multi-frame verification, temporal reasoning, sequence-based decision, frame aggregation | 多帧确认、时序推理、连续帧判断 |
| 异常检测 | anomaly detection | abnormal event detection, outlier detection, novelty detection, one-class classification | 异常检测、异常事件检测、离群检测 |
| 行为识别（拓展） | action recognition | human action recognition (HAR), activity recognition, behavior analysis | 动作识别、行为识别、人体行为分析 |
| 时序动作检测 | temporal action detection | temporal action localization, TAL, video grounding | 时序动作检测、动作定位 |
| 明火检测 | fire detection | flame detection, fire recognition, early fire detection | 火焰检测、明火识别、火灾早期检测 |
| 烟雾检测 | smoke detection | smoke recognition, early smoke detection | 烟雾检测、烟感识别 |
| 人员跌倒检测 | fall detection | human fall detection, fall recognition, elderly fall monitoring | 跌倒检测、摔倒识别、跌倒预警 |
| 禁区入侵检测 | intrusion detection | forbidden zone intrusion, region intrusion, line crossing, perimeter intrusion | 入侵检测、越界检测、区域入侵、周界防范 |
| 车辆违停检测 | illegal parking detection | illegal stopping, parking violation detection, unauthorized parking, vehicle violation | 违停检测、违规停车、违章停车检测 |
| 消防通道占用 | fire lane occupancy | fire lane blockage, emergency lane occupation, forbidden zone parking, fire access obstruction | 消防通道占用、消防车道堵塞、应急通道占用 |
| 人群聚集 / 人数统计 | crowd counting / gathering detection | people counting, crowd density estimation, crowd analysis | 人群计数、人数统计、人群密度估计、聚集检测 |
| 攀爬 / 翻越围栏 | fence climbing | intrusion climbing, perimeter climbing, fence breach | 翻越围栏、攀爬入侵 |
| 打架 / 暴力行为 | violence detection | fight detection, aggressive behavior recognition, physical violence | 打架检测、暴力行为识别 |
| 徘徊 / 滞留 | loitering detection | lingering behavior, suspicious loitering, abnormal stay | 徘徊检测、滞留检测、异常停留 |
| 交通事件检测 | traffic incident detection | traffic event detection, road anomaly, accident detection | 交通事件检测、道路异常检测 |

---

## 6. 规则与空间判断层

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 电子围栏 | electronic fence / geofence | virtual fence, virtual boundary, safe zone, forbidden region | 电子围栏、虚拟围栏、虚拟边界、警戒区 |
| 感兴趣区域 | region of interest (ROI) | detection region, mask region, polygon mask, zone area | 感兴趣区域、检测区域、多边形区域、掩膜区 |
| 多边形区域 | polygon region | polygonal ROI, mask polygon, area annotation | 多边形区域、区域标注 |
| 区域关系判断 | spatial relation reasoning | spatial reasoning, point-in-polygon (PIP), region overlap, containment test | 区域关系判断、点在多边形内、区域重叠、包含判断 |
| 交并比 | intersection over union (IoU) | box overlap, region overlap ratio, IoA | 交并比、重叠度、重叠比例 |
| 滞留 / 停留时长 | dwell time | stay duration, residence time, sojourn time, lingering time | 停留时长、滞留时间、驻留时间 |
| 静止状态判断 | stationary detection | motionless detection, stillness, motion state analysis | 静止状态、静止判断、运动状态分析 |
| 阈值规则 | rule-based threshold | parameter threshold, decision threshold, confidence threshold | 阈值规则、参数阈值、置信度阈值 |
| 规则引擎 | rule engine | business rule engine (BRE), rule-based system, expert system | 规则引擎、业务规则引擎、专家系统 |
| 冷却时间 | cooldown period | cooldown time, alarm suppression window, refractory period | 冷却时间、告警抑制、静默期 |
| 状态机 | state machine | finite state machine (FSM), temporal state machine, state transition | 状态机、有限状态机、状态流转 |

---

## 7. 误报抑制与评价层

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 误报 | false positive (FP) | false alarm, false detection, spurious detection, 误检 | 误报、误检、错误告警 |
| 漏报 | false negative (FN) | miss detection, missed alarm, 漏检 | 漏报、漏检、漏警 |
| 误报率 / 漏报率 | false positive rate (FPR) | false alarm rate (FAR), miss rate, FNR | 误报率、漏报率、虚警率 |
| 召回率 | recall | sensitivity, true positive rate (TPR), detection rate (DR) | 召回率、查全率、灵敏度 |
| 精确率 | precision | positive predictive value (PPV), 查准率 | 精确率、查准率 |
| F1 值 | F1-score | F-measure, F1 measure, harmonic mean | F1 值、F 值 |
| 平均精度 | mean average precision (mAP) | mAP@0.5, mAP@0.5:0.95, AP, COCO metric | 平均精度、mAP |
| 检测延迟 | detection latency | inference latency, alert latency, end-to-end delay | 检测延迟、推理时延、告警延迟 |
| 吞吐 / 帧率 | FPS | frames per second, throughput, processing rate | 帧率、处理速度、吞吐量 |
| 困难样本 | hard example / hard negative | difficult sample, hard sample mining, challenging sample | 困难样本、难例、困难负样本 |
| 数据泄漏 | data leakage | train-test leakage, frame leakage, temporal leakage | 数据泄漏、训练测试污染 |
| 数据集划分 | dataset split | train/val/test split, cross-validation, hold-out | 数据集划分、交叉验证、留出法 |
| 数据增强 | data augmentation | image augmentation, oversampling, synthetic data | 数据增强、图像增广、样本扩充 |
| 类别不平衡 | class imbalance | long-tail distribution, rare class, imbalanced dataset | 类别不平衡、长尾分布、稀有类 |

---

## 8. 业务闭环与信息系统层

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 事件管理系统 | incident management system | event management, case management, alarm management | 事件管理、告警管理、工单系统 |
| 闭环处置 | closed-loop disposal | closed-loop workflow, closed-loop management, workflow closure | 闭环处置、闭环管理、流程闭环 |
| 工单派发 | task dispatch | work order dispatch, task assignment, dispatching, ticket assignment | 任务派发、工单派发、派单 |
| 人工复核 | manual review | human verification, human-in-the-loop verification, alarm triage | 人工复核、人工核实、告警分级审核 |
| 证据留存 / 归档 | evidence archiving | record keeping, event archiving, chain of custody | 证据归档、事件归档、留痕 |
| 可追溯性 | traceability | auditability, provenance, audit trail | 可追溯性、审计追踪、溯源 |
| 巡检报告 | inspection report | patrol report, periodic report, analytics report | 巡检报告、巡查报告、统计报告 |
| 角色权限控制 | role-based access control (RBAC) | access control, permission management, authorization | 角色权限控制、访问控制、权限管理 |
| 数据脱敏 | data anonymization | de-identification, privacy masking, face blurring | 数据脱敏、去标识化、隐私遮蔽 |
| 监控数据隐私 | surveillance privacy | privacy-preserving surveillance, GDPR compliance, video privacy | 监控隐私、隐私保护、合规 |

---

## 9. 工程与部署层

| 概念 | 英文主词 | 英文同义词 | 中文同义词 |
| --- | --- | --- | --- |
| 边缘计算 | edge computing | edge inference, edge AI, on-device inference | 边缘计算、边缘推理、端侧推理 |
| 模型量化 | model quantization | INT8 quantization, pruning, model compression, distillation | 模型量化、模型压缩、剪枝 |
| 实时视频流 | real-time video stream | live stream, RTSP, streaming inference, video pipeline | 实时视频流、视频流处理、拉流 |
| 视频抽帧 | frame sampling | frame extraction, frame skipping, keyframe selection | 视频抽帧、帧采样、关键帧选取 |
| 容器化部署 | containerized deployment | Docker, Docker Compose, Kubernetes, microservice | 容器化部署、微服务、容器编排 |
| 消息推送 | real-time notification | WebSocket push, message queue, pub/sub, MQTT | 实时推送、消息队列、发布订阅 |
| 微服务架构 | microservice architecture | service-oriented architecture (SOA), service decomposition | 微服务架构、服务拆分、面向服务架构 |
| 多路视频调度 | multi-stream scheduling | multi-channel processing, load balancing, GPU scheduling | 多路视频调度、多通道处理、负载均衡 |
| 云边协同 | cloud-edge collaboration | edge-cloud synergy, distributed inference, hierarchical deployment | 云边协同、边云协同、分布式推理 |

---

## 10. 组合检索建议（按章节对应）

> 下面把矩阵词表组织成可直接粘贴的检索式，按你写论文的章节顺序排列。

### 10.1 综述 / 引言（Related Work）

```
# 智能监控综述
("intelligent video surveillance" OR "video analytics") AND ("survey" OR "review" OR "overview")

# 深度学习在监控中的应用
("deep learning" OR "CNN") AND ("video surveillance") AND ("object detection" OR "anomaly detection")

# 校园 / 公共安全
("campus security" OR "school safety" OR "public safety") AND ("video surveillance" OR "computer vision")
```

### 10.2 双模型架构部分

```
# 通用检测
("object detection") AND ("YOLO" OR "one-stage detector") AND ("real-time" OR "surveillance")

# 专项检测（烟火 / 跌倒）
("fire detection" OR "smoke detection" OR "fall detection") AND ("deep learning" OR "YOLO" OR "CNN")

# 迁移学习 / 微调
("transfer learning" OR "fine-tuning") AND ("pretrained" OR "pretrained weights") AND ("small dataset" OR "domain adaptation")
```

### 10.3 跟踪 + 规则模块部分

```
# 跟踪
("multi-object tracking" OR "ByteTrack" OR "tracking-by-detection") AND ("surveillance" OR "video")

# 空间规则
("virtual fence" OR "geofence" OR "region of interest") AND ("intrusion" OR "detection")

# 时序 / 多帧确认
("temporal" OR "multi-frame" OR "sequence") AND ("confirmation" OR "verification" OR "aggregation") AND ("surveillance")

# 误报抑制
("false alarm reduction" OR "false positive suppression") AND ("tracking" OR "temporal") AND ("video surveillance")
```

### 10.4 事件检测方案部分

```
# 违停 / 占用
("illegal parking" OR "parking violation" OR "fire lane") AND ("detection" OR "monitoring")

# 跌倒（含姿态）
("fall detection") AND ("pose estimation" OR "keypoints" OR "skeleton" OR "YOLO-Pose")

# 人群
("crowd counting" OR "people counting" OR "crowd density") AND ("deep learning" OR "CNN" OR "detection")
```

### 10.5 工程 / 部署部分

```
# 边缘部署
("edge computing" OR "edge AI") AND ("video analytics" OR "real-time inference")

# 模型轻量化
("model compression" OR "quantization" OR "pruning") AND ("object detection" OR "YOLO")
```

### 10.6 评价 / 实验部分

```
("mAP" OR "precision" OR "recall" OR "F1") AND ("object detection") AND ("evaluation")

("false alarm rate" OR "miss rate" OR "detection latency") AND ("surveillance system")
```

---

## 11. 使用建议

1. **中文文献走知网 / 万方**，用第 2、5、6 列的中文同义词；英文文献走 WoS / IEEE / Scopus，用第 3、4 列。
2. **优先级排序**：先检索 `第 5 节 事件检测` + `第 7 节 误报抑制`，这两块是你文档最强调的差异点，也是文献最需要支撑的地方。
3. **警惕名词陷阱**：文档里 `消防通道占用`、`车辆违停`、`禁区入侵` 都是**业务命名**，不是学术术语。学术对应词是 `fire lane occupancy` / `illegal parking` / `intrusion detection`，用业务词检索几乎搜不到论文。
4. **同义词取并集**：一个概念如果只用一个词检索，召回会非常低。务必组成 `A OR B OR C` 再和别的概念 `AND`。
5. **注意时间窗口**：YOLO 相关最好限定近 3~5 年（`YOLOv5/v8/v11` 之后），经典 CTC、传统 HOG 检测可作为背景引用。

---

*生成日期：2026-10-11 ｜ 来源：CampusGuard 系统设计文档 v1*
