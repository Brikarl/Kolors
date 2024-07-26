


## <a name="Introduction"></a>📖 Introduction

We provide two ControlNet weights and inference code based on Kolors-Basemodel: Canny and Depth. You can find some example images below.


**1、ControlNet Demos**

<table >
  
   <tr>
    <td align="center">Condition Image </td>
    <td align="center">Prompt </td>
    <td align="center">Result Image </td>
  </tr>

  <tr>
    <td align="center"><img src="outputs/Canny_dog_condition.jpg" width=400px/></td>
    <td align="center"><font style="font-size:12px">全景，一只可爱的白色小狗坐在杯子里，看向镜头，动漫风格，3d渲染，辛烷值渲染。</p> Panorama of a cute white puppy sitting in a cup and looking towards the camera, anime style, 3d rendering, octane rendering. </font> </td> 
    <td align="center"><img src="outputs/Canny_dog.jpg" width=400px/></td>
  </tr>

  <tr>
    <td align="center"><img src="outputs/Depth_woman_2_condition.jpg" width=400px/></td>
    <td align="center"><font style="font-size:12px">新海诚风格，丰富的色彩，穿着绿色衬衫的女人站在田野里，唯美风景，清新明亮，斑驳的光影，最好的质量，超细节，8K画质。</p> Makoto Shinkai style, rich colors, a woman in a green shirt standing in the field, beautiful scenery, fresh and bright, mottled light and shadow, best quality, ultra-detailed, 8K quality. </font> </td> 
    <td align="center"><img src="outputs/Depth_woman_2.jpg" width=400px/></td>
  </tr>


</table>



**2、ControlNet and IP-Adapter-Plus Demos**

We also support joint inference code between Kolors-IPadapter and Kolors-ControlNet.

<table >
   <tr>
    <td align="center">Reference Image </td>
    <td align="center">Condition Image </td>
    <td align="center">Prompt </td>
    <td align="center">Result Image </td>
  </tr>

  <tr>
    <td align="center"><img src="../ipadapter/asset/2.png" width=400px/></td>
    <td align="center"><img src="outputs/Depth_woman_2_condition.jpg" width=400px/></td>
    <td align="center"><font style="font-size:12px">一个红色头发的女孩，唯美风景，清新明亮，斑驳的光影，最好的质量，超细节，8K画质。</p> A girl with red hair, beautiful scenery, fresh and bright, mottled light and shadow, best quality, ultra-detailed, 8K quality. </font> </td> 
    <td align="center"><img src="outputs/Depth_ipadapter_woman_2.jpg" width=400px/></td>
  </tr>

  <tr>
    <td align="center"><img src="assets/woman_1.png" width=400px/></td>
    <td align="center"><img src="outputs/Depth_1_condition.jpg" width=400px/></td>
    <td align="center"><font style="font-size:12px">一个漂亮的女孩，最好的质量，超细节，8K画质。</p> A beautiful girl, best quality, super detail, 8K quality. </font> </td> 
    <td align="center"><img src="outputs/Depth_ipadapter_1.jpg" width=400px/></td>
  </tr>

</table>

<br>




## <a name="Evaluation"></a>📊 Evaluation
To evaluate the performance of models, we compiled a test set of more than 200 images and text prompts. We invite several image experts to provide fair ratings for the generated results of different models. The experts rate the generated images based on four criteria: visual appeal, text faithfulness, conditional controllability, and overall satisfaction. Conditional controllability measures controlnet's ability to preserve spatial structure, while the other criteria follow the evaluation standards of BaseModel. The specific results are summarized in the table below, where Kolors-ControlNet achieved better performance in various criterias.

**1、Canny**

|       Model       |  Average Overall Satisfaction | Average Visual Appeal | Average Text Faithfulness | Average Conditional Controllability |
| :--------------: | :--------: | :--------: | :--------: | :--------: |
| SDXL-ControlNet-Canny |	3.14	| 3.63	| 4.37	| 2.84 |
| **Kolors-ControlNet-Canny**  | **4.06** |  **4.64**  | **4.45** | **3.52** |



**2、Depth**

|       Model       |  Average Overall Satisfaction | Average Visual Appeal | Average Text Faithfulness | Average Conditional Controllability |
| :--------------: | :--------: | :--------: | :--------: | :--------: |
| SDXL-ControlNet-Depth |	3.35	| 3.77	| 4.26	| 4.5 |
| **Kolors-ControlNet-Depth**  | **4.12** |  **4.12**  | **4.62** | **4.6** |


<font color=gray style="font-size:12px">*The [SDXL-ControlNet-Canny](https://huggingface.co/diffusers/controlnet-canny-sdxl-1.0) and [SDXL-ControlNet-Depth](https://huggingface.co/diffusers/controlnet-depth-sdxl-1.0) load [DreamShaper-XL](https://civitai.com/models/112902?modelVersionId=351306) as backbone model.*</font>


<table >
  <tr>
    <td colspan="4" align="center">Compare Result</td>
  </tr>
  
   <tr>
    <td align="center">Condition Image </td>
    <td align="center">Prompt </td>
    <td align="center">Kolors-ControlNet Result </td>
    <td align="center">SDXL-ControlNet Result </td>
  </tr>

  <tr>
    <td align="center"><img src="outputs/Canny_woman_1_condition.jpg" width=400px/></td>
    <td align="center"><font style="font-size:12px">一个漂亮的女孩，高品质，超清晰，色彩鲜艳，超高分辨率，最佳品质，8k，高清，4K。</p> A beautiful girl, high quality, ultra clear, colorful, ultra high resolution, best quality, 8k, HD, 4K. </font> </td> 
    <td align="center"><img src="outputs/Canny_woman_1.jpg" width=400px/></td>
    <td align="center"><img src="outputs/Canny_woman_1_sdxl.jpg" width=400px/></td>
  </tr>


  <tr>
    <td align="center"><img src="outputs/Depth_bird_condition.jpg" width=400px/></td>
    <td align="center"><font style="font-size:12px">一只颜色鲜艳的小鸟，高品质，超清晰，色彩鲜艳，超高分辨率，最佳品质，8k，高清，4K。</p> A colorful bird, high quality, ultra clear, colorful, ultra high resolution, best quality, 8k, HD, 4K. </font> </td> 
    <td align="center"><img src="outputs/Depth_bird.jpg" width=400px/></td>
    <td align="center"><img src="outputs/Depth_bird_sdxl.jpg" width=400px/></td>
  </tr>



</table>


------


## <a name="Usage"></a>🛠️ Usage

### Requirements

The dependencies and installation are basically the same as the [Kolors-BaseModel](https://huggingface.co/Kwai-Kolors/Kolors).

<br>


### Weights download
```bash
# Canny - ControlNet
huggingface-cli download --resume-download Kwai-Kolors/Kolors-ControlNet-Canny --local-dir weights/Kolors-ControlNet-Canny

# Depth - ControlNet
huggingface-cli download --resume-download Kwai-Kolors/Kolors-ControlNet-Depth --local-dir weights/Kolors-ControlNet-Depth
```

If you intend to utilize the depth estimation network, please make sure to download its corresponding model weights.
```
huggingface-cli download lllyasviel/Annotators ./dpt_hybrid-midas-501f0c75.pt --local-dir ./controlnet/annotator/ckpts  
```


### Inference


**a. Using canny ControlNet:**

```bash
python ./controlnet/sample_controlNet.py ./controlnet/assets/woman_1.png 一个漂亮的女孩，高品质，超清晰，色彩鲜艳，超高分辨率，最佳品质，8k，高清，4K Canny

python ./controlnet/sample_controlNet.py ./controlnet/assets/dog.png 全景，一只可爱的白色小狗坐在杯子里，看向镜头，动漫风格，3d渲染，辛烷值渲染 Canny

# The image will be saved to "controlnet/outputs/"
```

**b. Using depth ControlNet:**

```bash
python ./controlnet/sample_controlNet.py ./controlnet/assets/woman_2.png 新海诚风格，丰富的色彩，穿着绿色衬衫的女人站在田野里，唯美风景，清新明亮，斑驳的光影，最好的质量，超细节，8K画质 Depth

python ./controlnet/sample_controlNet.py ./controlnet/assets/bird.png 一只颜色鲜艳的小鸟，高品质，超清晰，色彩鲜艳，超高分辨率，最佳品质，8k，高清，4K Depth

# The image will be saved to "controlnet/outputs/"
```



**c. Using depth ControlNet + IP-Adapter-Plus:**

If you intend to utilize the kolors-ip-adapter-plus, please make sure to download its corresponding model weights.

```bash
python ./controlnet/sample_controlNet_ipadapter.py ./controlnet/assets/woman_2.png ./ipadapter/asset/2.png  一个红色头发的女孩，唯美风景，清新明亮，斑驳的光影，最好的质量，超细节，8K画质 Depth

python ./controlnet/sample_controlNet_ipadapter.py ./ipadapter/asset/1.png ./controlnet/assets/woman_1.png  一个漂亮的女孩，最好的质量，超细节，8K画质 Depth

# The image will be saved to "controlnet/outputs/"
```

<br>


### Acknowledgments
- Thanks to [ControlNet](https://github.com/lllyasviel/ControlNet) for providing the codebase.

<br>


