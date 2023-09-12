# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4
Display the modified image output.

### Step5:
End the program.



## Program:

Developed By: T S Yamunaasri

Register Number: 212222240117
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()
```
ii) Image Scaling
```import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,50],
              [0,1,50],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 
```

iii)Image shearing

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("cat.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:150 ,10:250]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
<br>
![Screenshot 2023-09-12 090835](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/54e2152f-c83e-4061-8177-bb74294bc668)

<br>

### ii) Image Scaling
<br>
![Screenshot 2023-09-12 090909](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/05e8cbbe-e7a1-46d4-88ff-bf889ba1c2ec)

<br>


### iii)Image shearing
<br>
![Screenshot 2023-09-12 090939](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/19d978ff-18d1-4857-a87a-e4ab682f001b)

![Screenshot 2023-09-12 090948](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/150c64c8-1e5b-4727-a027-faaf5cab7695)

<br>


### iv)Image Reflection
<br>
![Screenshot 2023-09-12 091135](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/ed31d036-7784-43f7-8d7f-92fe434519f3)

<br>
![Screenshot 2023-09-12 091143](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/e8a2b4a0-3c33-47b6-b0fa-af78acf55782)

<br>



### v)Image Rotation
<br>
![Screenshot 2023-09-12 091031](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/052903a6-be7d-46a0-9020-e8412a010d08)

<br>



### vi)Image Cropping
<br>
Original

![Screenshot 2023-09-12 091255](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/de164b31-dc93-488d-8a35-11012d93d2c1)

<br>
Cropped

![Screenshot 2023-09-12 091304](https://github.com/Yamunaasri/IMAGETRANSFORMATION/assets/115707860/0ecbcd91-559e-49e0-952e-a96fab56f2bf)

<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
