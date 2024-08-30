# PyTorch_practice
PyTorch実践入門の学習

# セットアップ手順
1. GPUのドライバをインストール
    - NVIDIA：https://www.nvidia.com/ja-jp/drivers/
2. GPUを使用するためCUDAツールキットのインストール
    - `sudo apt-get install nvidia-cuda-toolkit`
3. PyTorchのインストール
    - `pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu124`
    ※ urlはドライバに対応するCUDAのバージョン

4. Jupyter Notebookのセットアップ
    - `pip install notebook`
    - 対応するvscodeの拡張機能をインストール

5. 動作確認
次のファイル(test.ipynb)を作成し、実行してGPUが認識されているか確認
```python
import torch
print(torch.cuda.is_available())
```