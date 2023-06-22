# Python-course
This course will introduce the essential steps of setting up an image analysis workflow for your research. It will cover the topics of microscopy data loading, processing and quantification. It will illustrate how to extract relevant information from an image using common Python packages. To run the notebook on the server, copy and paste the following link into the browser: 

http://10.91.193.124/hub/user-redirect/git-pull?repo=https://github.com/u-schulze/Python-course&branch=main&app=lab


# Download data folder
The data that we will be using during this course can be found [here](https://cloud.mrc-lmb.cam.ac.uk/s/LwKn2ieBfmpEBrw/download/data.zip). To download it and unzip, copy and run the following codes in a cell of your notebook.
```
from urllib.request import urlopen
from io import BytesIO
from zipfile import ZipFile

def download_and_unzip(url, extract_to='.'):
    http_response = urlopen(url)
    zipfile = ZipFile(BytesIO(http_response.read()))
    zipfile.extractall(path=extract_to)

url = 'https://cloud.mrc-lmb.cam.ac.uk/s/LwKn2ieBfmpEBrw/download/data.zip'
data_folder = './'
download_and_unzip(url, data_folder) 
```
After you have run the above-mentioned codes, you should have a folder named 'data' in the path directory you are working on. Copy and run the following codes to test the display of one of the data:
```
from scyjava import config
from aicsimageio import AICSImage
import matplotlib.pyplot as plt

file = AICSImage('data/airyscan-4colors.tif')
img = file.data
plt.imshow(img[0,1,0]) 
```

