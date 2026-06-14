# 期末專案-NeRF

## 需求套件

### Python 套件
```bash
pip install torch numpy matplotlib imageio Pillow tqdm scikit-image
```

### 外部工具
- **COLMAP**（結構從運動重建）：需下載 Windows CUDA 版本，並在 notebook 中設定正確的 `COLMAP.bat` 路徑。
  - 下載網址： https://github.com/colmap/colmap/releases

## 訓練說明

因為背景有雜物的照片很難被colmap抓取，所以訓練資料集到15張

且原先15張照片訓練的colmap_past_out檔案以及其訓練完的模型遺失，但訓練結果有截圖

試著重新訓練但結果不同了，所以以截圖為主

背景為純色、無雜物干擾完整的被colmap抓到，所以資料集有到30張

N_ITERS15000 都是在本機上訓練，N_ITERS30000 則是在學校的DGX訓練

colmap_out都是在本機跑完再給DGX，因為我在DGX無法下在colmap