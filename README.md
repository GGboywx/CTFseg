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



