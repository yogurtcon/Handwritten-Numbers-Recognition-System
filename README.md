### 使用方法

train.ipynb训练并保存模型

my_model.h5是保存下来的模型

predict.ipynb进行手写数字识别

<br/>

### 希望实现 “保存与加载模型” 这一功能

new_model = keras.models.load_model(‘my_model.h5’)

报错： ValueError: Unknown initializer: GlorotUniform

解决方法是在‘keras’前面加‘tensorflow.’

tensorflow.keras.models.load_model(‘my_model.h5’)

<br/>

### 希望实现 “导入图片时将图片尺寸变成28*28” 这一功能

img = mpimg.imread('1.png')

img2 = img.resize((28,28))

报错:  AttributeError: ‘NoneType’ object has no attribute ‘shape’

解决办法是导入cv2，用他的resize方法

import cv2

img = mpimg.imread('1.png')

img2 = cv2.resize(img, (28,28))
