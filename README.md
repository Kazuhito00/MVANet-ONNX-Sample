# MVANet-ONNX-Sample

DIS(Dichotomous Image Segmentation)モデルである[qianyu-dlut/MVANet](https://github.com/qianyu-dlut/MVANet)のPythonでのONNX推論サンプルです。<br>
変換自体を試したい方は、Google Colaboratory上で[Convert2ONNX.ipynb](Convert2ONNX.ipynb)を使用ください。<br>
> [!NOTE]
> ONNX変換に際して、Adaptive Average Pooling を Average Pooling で代替しています<br>
> その結果、オリジナルモデルと比べ、推論速度や精度が劣る可能性があります
> 
![image](https://github.com/user-attachments/assets/626b20d5-3e85-473d-b96f-ea7895e2ceb6)

# Requirement 
* OpenCV 4.5.3.56 or later
* onnxruntime 1.11.0 or later
* tqdm 4.66.1 or later  # model/mvanet_1024x1024.onnx ファイルダウンロードを行う場合

# Convert
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Kazuhito00/MVANet-ONNX-Sample/blob/main/Convert2ONNX.ipynb)<br>
Colaboratoryでノートブックを開き、上から順に実行してください。<br>
※GPU RAMの都合上、L4 GPUインスタンス以上必須

# Demo
デモの実行方法は以下です。
```bash
python demo_onnx.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --movie<br>
動画ファイルの指定 ※指定時はカメラデバイスより優先<br>
デフォルト：指定なし
* --model<br>
ロードするモデルの格納パス<br>
デフォルト：model/mvanet_1024x1024.onnx
* --score_th<br>
マスク値の閾値 ※指定する場合は0.5など小数値を指定<br>
デフォルト：None

# Reference
* [qianyu-dlut/MVANet](https://github.com/qianyu-dlut/MVANet)

# Author
高橋かずひと(https://twitter.com/KzhtTkhs)
 
# License 
MVANet-ONNX-Sample is under [MIT License](LICENSE).

# Note
サンプルの画像は[ぱくたそ](https://www.pakutaso.com/)様の「[攻撃ヘリコプターアパッチ（AH-64）](https://www.pakutaso.com/20171004291ah-64-1.html)」を使用しています。
