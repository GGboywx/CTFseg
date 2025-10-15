🌊 CTFSeg: Multi-scale Attention Network for Chinese Tidal Flat Segmentation

CTFSeg is a high-precision semantic segmentation framework for coastal tidal flat remote sensing images. It integrates a Multi-scale Feature Transformer (MFT) with an Edge-Guided Fuzzy Decoder (EGD), effectively capturing the fuzzy boundary features between tidal flats and water, wet sand, and vegetation.This project also releases the CTF (China Tidal Flat) dataset, which covers both typical and atypical tidal flat areas in eastern China. It is currently the first publicly available coastal tidal flat remote sensing semantic segmentation dataset with 10 m resolution, multi-region coverage, and pixel-level annotations.

🚀 At present, only the training and validation sets are publicly released; the model and test set will be published gradually in the future!

📘 Highlights

✅ CTFSeg Network Innovations

🧠 Multi-scale Feature Transformer (MFT): Integrates ASPP and Transformer structures to model local multi-scale context and global semantic dependencies. 

🎯 Perceptual Attention (PA): Dynamically focuses on key intertidal zones, enhancing the recognition of small tidal channels and fine-grained textures. 

🌀 Fuzzy Layer + Edge-Guided Decoder (EGD): Models fuzzy boundaries using membership functions, explicitly supervises edge features, improving boundary IoU by 7.1%. 

⚙️ Cross-edge Fusion Module (CEF): Deeply interacts edge and semantic features, strengthening the recognition of transitional zones in tidal flats.

✅ Features of the CTF Dataset

🌍 Covers 12 typical and atypical tidal flat areas (Yueqing Bay, Yellow River Estuary, Hangzhou Bay, Min River Estuary, Liao River Estuary, Pearl Harbor, Yalu River Estuary, etc.);

🛰 Constructed based on Sentinel-2 MSI imagery, with a spatial resolution of 10 m;🗓 Time range: 2020–2024;

🧩 Total of 1,136 samples (training 743, validation 343, testing 50);

💡 Annotations were created using the EISeg tool by multiple remote sensing experts;

📈 After consistency verification, annotation performance: OA = 94.6%, Kappa = 0.89, boundary Dice = 0.93.


@article{gu2025ctfseg,
  title={CTFSeg: A Multi-scale Attention Semantic Segmentation Network for Chinese Tidal Flats},
  author={Gu, Wenxuan and Others},
  journal={},
  year={2025},
  doi={}
}


graph TD
    %% 定义样式
    classDef data_style fill:#DFF0D8,stroke:#4CAF50,stroke-width:2px,color:#333;
    classDef model_style fill:#E0F2F7,stroke:#2196F3,stroke-width:2px,color:#333;
    classDef innovation_style fill:#FFF9C4,stroke:#FFC107,stroke-width:3px,color:#333;
    classDef eval_style fill:#FBEFF2,stroke:#F44336,stroke-width:2px,color:#333;
    classDef output_style fill:#F5F5F5,stroke:#9E9E9E,stroke-width:2px,color:#333;
    classDef start_end_style fill:#F0F0F0,stroke:#666,stroke-width:2px,color:#333;

    %% 节点定义
    A[研究启动与文献综述]:::start_end_style
    
    subgraph 数据构建与预处理
        B(Sentinel-2 原始影像获取)
        C(影像预处理: 大气校正, 几何校正等)
        D{CTFSeg数据集构建与标注}
        E[标准化训练集/验证集/测试集]:::data_style
    end
    
    subgraph CTFSeg模型设计与训练
        F[改进型骨干网络<br>(如: ResNet/Swin Transformer)]:::model_style
        G[**多尺度特征转换器 (MFT)**<br>全局上下文建模]:::innovation_style
        H[**边缘引导解码器 (EGD)**<br>细粒度边界刻画]:::innovation_style
        I[**模糊融合机制 / 跨边缘融合**<br>光谱模糊处理]:::innovation_style
        J[CTFSeg模型架构<br>(完整集成)]:::model_style
        K[多目标损失函数优化<br>(BCE+Tversky+Focal+Edge)]:::model_style
        L[模型训练与参数调优]:::model_style
    end

    subgraph 模型评估与验证
        M[消融实验]:::eval_style
        N[性能对比<br>(精度, 效率)]:::eval_style
        O[跨区域/跨时相泛化性测试]:::eval_style
    end

    P[**研究成果输出**<br>高质量论文, 开源代码, CTFSeg数据集]:::output_style
    Q[研究结题]:::start_end_style

    %% 流程连接
    A --> B
    B --> C
    C --> D
    D --> E
    
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --> M
    M --> N
    N --> O
    O --> P
    P --> Q
