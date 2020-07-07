# road sign tagging

Tagging the images which have the road signs 


<table>
  <thead>
    <tr>
      <th>Input</th>
      <th>Output</th>
    </tr>
  </thead>
  <tr>
    <td>
      <img src="https://www.guide2dubai.com/Portals/0/Images/Living/Transportation/dubai-road-signs.jpg" width="400">
    </td>
    <td>
      <pre>
{
  'tag': 'road_sign', 
  'score': 0.9429549
}
</pre>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://live.staticflickr.com/4169/34649653051_9e31056a0a_b.jpg" width="400">
    </td>
    <td>
      <pre>
{
  'tag': 'non_road_sign', 
  'score': 0.7540367
}
</pre>
    </td>
  </tr>
</table>


### Installation


to install the road sign tagging model, you need Python 3.7.7 

```bash
git clone https://github.com/gaoyuanliang/road_sign_tagging.git

cd road_sign_tagging

pip3 install -r requirements.txt

wget https://github.com/fchollet/deep-learning-models/releases/download/v0.4/xception_weights_tf_dim_ordering_tf_kernels_notop.h5
```

download the pretrain model of cheque detection from this url [https://drive.google.com/file/d/1lGkgRc1VU1tVJPiMUSVyCV2Elm1Gy8_-/view?usp=sharing](https://drive.google.com/file/d/1lGkgRc1VU1tVJPiMUSVyCV2Elm1Gy8_-/view?usp=sharing) to the folder road_sign_tagging


### Using

down load an image of road sign 

```base
wget https://c8.alamy.com/comp/FPMFN8/road-signs-dubai-uae-FPMFN8.jpg
```

this image looks like

![](https://c8.alamy.com/comp/FPMFN8/road-signs-dubai-uae-FPMFN8.jpg)


import the model in python3

```python
from road_sign_tagging import road_sign_tagging
```

run the tagging program

```python
road_sign_tagging('road-signs-dubai-uae-FPMFN8.jpg')
```

you will see the following output:

```python
{'tag': 'road_sign', 'score': 0.9429549}
```

now lets download another example of image which does not have any road sign

```base
wget https://live.staticflickr.com/4169/34649653051_9e31056a0a_b.jpg
```

it looks like 

![](https://live.staticflickr.com/4169/34649653051_9e31056a0a_b.jpg)

run the tagging program

```python
road_sign_tagging('34649653051_9e31056a0a_b.jpg')
```

and it has the following output since it has no road sign

```python
{'tag': 'non_road_sign', 'score': 0.7540367}
```

feel free to contact me if you have any problem with this package or you are hiring data scientist/AI engineer. I am actively looking for data science/AI related jobs

My email: gaoyuanliang@outlook.com
