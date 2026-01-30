# V-JEPA-Tutorial.ipynb
Demo code for V-Jepa inference
>* Frameworks: pytorch in Colab
>* Model : "facebook/vjepa2-vitl-fpc16-256-ssv2"
>* Dataset : moving_mnist
>* Tactics : Zero shot application of the model to the dataset

## Results
![a9676af9-f19f-4d69-b388-257f8b2674cf](https://github.com/user-attachments/assets/1d333fa2-75d7-4129-9c5f-3a6cfe6a8600) <br>
Top Prediction Index: 43
Inference Wording: Moving [something] down

# V-JEPA2-Demo.ipynb
## Methods & Materials
>* Frameworks: pytorch in Colab
>* Model: facebook/vjepa2-vitg-fpc64-384 or facebookresearch/vjepa2, vjepa2_vit_giant_384 used by torch.hub.load().
>* Datasets: An .mp4 video file named as "sample_video.mp4" available at "https://huggingface.co/datasets/nateraw/kinetics-mini/resolve/main/val/bowling/-WH-lxmGJVY_000005_000015.mp4" <br>

https://github.com/user-attachments/assets/b078a497-4148-4540-afd0-a773cdb7e284

## Results
Pretrained weights found at ./weights/ssv2-vitg-384-64x2x3.pt and loaded with msg: <All keys matched successfully> <br>
Classifier output shape: torch.Size([1, 174]) <br>
Top 5 predicted class names:<br>
**Putting [something] into [something] (45.151634216308594%)**<br>
Stuffing [something] into [something] (27.54499053955078%)<br>
Putting [something] onto [something] (15.023070335388184%)<br>
Failing to put [something] into [something] because [something] does not fit (7.21915864944458%)<br>
Putting [number of] [something] onto [something] (5.061150550842285%)<br>
/tmp/ipython-input-2987202713.py:85: UserWarning: Implicit dimension choice for softmax has been deprecated. Change the call to include dim=X as an argument.<br>
  top5_probs = F.softmax(out_classifier.topk(5).values[0]) * 100.0  # convert to percentage<br>
