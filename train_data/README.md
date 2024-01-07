# Training data for BapuBomma AI LoRA based on SDXL v1.5

## About

This folder contains all the data created for BapuBomma AI, a fine tuned version of SDXL trained on Bapu's work.

Sathiraju Lakshminarayana (15 December 1933 – 31 August 2014) know as Bapu(బాపు), is a famous artist from India and his work is very popular in the Telugu states of India. He is also known for his work in the Telugu film industry and his books and paintings are very popular among the Telugu people. BapuBomma is a word play on Bapu and Bomma which usually means a beautiful girl/woman in Telugu.

## Data format

Images(screenshots) are taken from the [source](https://bapuartcollection.com/). All images are in PNG format and there are 3 books and from some other works in the dataset. 


## Data source

Majority of the images in the dataset are from 3 books sourced from [bapuartcollection.com](https://bapuartcollection.com/):

1. **Hanumanthudi Kadha**
2. **Janani**
3. **Wedding**

Several other images are also included in the dataset which are not part of the mentioned 3 books but are from the same source like Bapus work published in newspapers through out the years and few specially from **Kiriti** and **Bangaram singaram**.

## Dataset creation

After handpicking the best of all 3 books and from the other sources. The images were edidted to remove "noise" and to make the images more clear.

Noise here is just random white space around the images and in some case some of the artifacts and texts in the images were removed to make the images more clear.

No resizing was done to the images except for cropping the images to remove the white space around the images in most of the imagesin v1.

V1.5 has images upscaled by 4x using [Playground AI](playgroundai.com).

## Dataset format

A zip file is then created with all the images and uploaded to vkolagotla.gitlab.io pages on gitlab to make it publicly available.

## Change log

### v1.5
After the results from v1 training, it was obvious that the data quality could make a significant difference in the model performance as the images are screenshots and very low in dimensions. 

Here are the dimensions of top 3 images in v1 dataset: sorted by num of pixels, high to low

```
Width Height image_name
1034 726 zimg_09.png
1262 593 yimg_04.png
693 591 zimg_13.png 
```

and the dimentions of last 3 images
```
Width Height image_name
355 287 zimg_19.png
193 236 zimg_18.png
400 217 zimg_29.png
```

As you can see a lot of the images are very low in resolution and i think this could be the reason for the model to not perform as well as i hoped.

So i used [Playground AI](playgroundai.com)(I think they use an upscaller from stability AI?) to upscale the images by 4x and removed some example as they did not look good after the upscaling.

Here are the top and bottom 3 images dimensions after upscaling, v1.5 dataset: Width x Height

```
Width Height image_name
4136 2904 zimg_09.png 
5048 2372 yimg_04.png 
2772 2364 zimg_13.png 
```

```
Width Height image_name
2060 720 img_11.png
988 716 img_02_1.png
984 704 img_02_0.png
```

Replicate does upscale the images from zip folder as they state in the docs but i wanted to create a good dataset for future trainings and to see if it makes any difference in the model performance.

The dataset now has 40 images with a zip file size of 102.1MB. For comparison the v1 dataset had 44 images with a zip file size of 9.9MB.

## Credits/License

This is purely a personal project and is not intended for commercial use. All the images are from the [source](https://bapuartcollection.com/) and can only be used for personal and non-commercial purposes.
