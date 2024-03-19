# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>
### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
```python
Developed By: Siva Chandran R
Register Number: 212222240099
```

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "/content/dip2.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dip2.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


iii)Image shearing

``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dip2.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()

```

iv)Image Reflection
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dip2.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  


```


v)Image Rotation


``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dip2.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 
```

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("/content/dip2.jpeg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[2000:3000 ,1000:2500]
plt.imshow(cropped_img)
plt.show()
```

## Output:


### i)Image Translation

![download](https://github.com/SivaChandranR07/IMAGE-TRANSFORMATIONS/assets/113497395/f15996d0-29c4-4076-890e-cd5d589ba9f8)



### ii) Image Scaling
#### Scaled Image:
![download](https://github.com/SivaChandranR07/IMAGE-TRANSFORMATIONS/assets/113497395/c77576e4-7447-4b65-a5a6-901e6171d9fa)









### iii)Image shearing


![download](https://github.com/SivaChandranR07/IMAGE-TRANSFORMATIONS/assets/113497395/1b7b6707-f153-408b-b85e-9e2da10266e2)



### iv)Image Reflection

![download](https://github.com/SivaChandranR07/IMAGE-TRANSFORMATIONS/assets/113497395/a6be825f-b07b-4da8-a3a3-e64fedc34deb)



### v)Image Rotation
![download](https://github.com/SivaChandranR07/IMAGE-TRANSFORMATIONS/assets/113497395/15f27a8e-bffc-4708-981b-7317b20995e3)



### vi)Image Cropping

![download](https://github.com/SivaChandranR07/IMAGE-TRANSFORMATIONS/assets/113497395/34f6b952-6c73-408f-a6b8-0c2330fd7432)





## Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
