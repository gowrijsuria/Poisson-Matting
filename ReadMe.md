# Poisson Matting

Implementation of the paper - 'Poisson Matting by Jian Sun, Jiaya Jia, Chi-Keung Tang and Heung-Yeung Shum'

## Packages Required

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install scipy, pillow, imageio, and cv2.

```bash
pip3 install scipy
```
```bash
pip3 install pillow
```
```bash
pip3 install imageio
```
```bash
pip3 install opencv-python
```
The basic packages of numpy and matplotlib are also required.
```bash
pip3 install numpy
```
```bash
pip3 install matplotlib
```

If imageio/pillow is already installed, make sure to upgrade the version of pillow being used before running the code.
```bash
pip3 install --upgrade pillow
```

## Downloading the repository

Use the commands bash terminal
```bash
git clone {url of the page}
```
or

Click 'Clone or Download' on the top right hand side of the repository.


## Usage
Go into the directory which holds all the files. Then open the Jupyter Notebook using the command -

```bash
jupyter-notebook
```

## Working of the code
The inputs of the code are 
1) An input image
2) Trimap of the input image (of the same size as the input)
3) The desired background (of a size bigger than the foreground images)

Running each cell in order would give the desired results - the foreground of input image pasted on a different background.

While doing Local poisson matting, the user needs to manually select the region where the operations need to be performed. Looking at the image after global matting, we can see the range of the x and y coordinates where the pixels need to be altered. Hence this code can be customised depending on the input images and the needs of each user.

The final matte can be further refined by using methods like boosting and highpass filtering. For these two methods, the user must select the regions where the operations are to be done, and set the x and y coordinates in the code accordingly. For this particular image, we are using these two methods. You can also use methods like cloning and channel selection as per your needs.
