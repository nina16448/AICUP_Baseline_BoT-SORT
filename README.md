# AICUP Baseline: BoT-SORT
更改的檔案只有 ReID Module 的 config file：fast_reid/configs/AICUP/bagtricks_R50-ibn.yml
以及 YOLOv7 的 yolov7/data/AICUP.yaml

因此訓練部分執行步驟皆與 baseline 程式碼相同。

## Tracking and creating the submission file for AICUP (Demo)

下載已訓練好的 YOLOv7 模型：https://drive.google.com/file/d/1d-LZeEMssHTHSE9kxdl_5UIzL6vNAp7_/view?usp=sharing

下載已訓練好的 ReID 模型：https://drive.google.com/drive/folders/1M2alql7dlB_n5r4p5_6yWpFDmMzrXyYE?usp=sharing

跑預測結果：
```shell
bash tools/track_all_timestamps.sh --weights "best.pt" --source-dir "AI_CUP_MCMOT_dataset/train/images" --device "0" --fast-reid-config "fast_reid/configs/AICUP/bagtricks_R50-ibn.yml" --fast-reid-weights "bagtricks_R50-ibn/model_0098.pth"
```
