# Thingiverse Downloader + STL Orientation Tweaker + Google Drive Uploader Tool

## Thingiverse APP Token

**To download from Thingiverse, you would need to paste thingiverse APP TOKEN inside the *api_credentials.ini* file**

You can get thingiverse developer api at:
https://www.thingiverse.com/developers

You can follow the tutorial for more detailed instruction (Getting Yout Access Keys section):
https://womenin3dprinting.com/how-to-use-the-thingiverse-api-basic-read-access/

**Example:**
![image](https://user-images.githubusercontent.com/31602239/211939113-083029a3-0e49-4022-9861-5b4fb765c8af.png)

![image](https://user-images.githubusercontent.com/31602239/211939301-9873a9b7-4e7f-425c-a91f-ad9070932da1.png)


## Google Cloud API
**You would need a OAuth Client ID .JSON file and a folder ID from Google to use the upload feature**

**1. Save and replace OAuth Client ID .JSON you download as the *credentials.json* file**

You can create Google cloud API and client ID at:
https://console.cloud.google.com/apis

You can follow this tutorial for more detailed instruction:
https://www.youtube.com/watch?v=6bzzpda63H0&t=2s

**2. Put google drive folder id of the folder you want to upload to in *line 20 of autostlpipeline.py* file**

You can find the folder id right in its *URL*, for example:
https://drive.google.com/drive/u/0/folders/[drive folder id]

![image](https://user-images.githubusercontent.com/31602239/211940770-845314a5-4739-4513-acbc-3b145b50fee4.png)

![image](https://user-images.githubusercontent.com/31602239/211941036-d3a7a1a5-d0b8-4080-b3dd-a74a28207234.png)


## Exanple Use

**To get started, make sure you cd to the correct terminal directory where this folder is located**

Type in your terminal to know all the options:

```bash
python autostlpipeline.py --help
```

For example, if you want to search objects by keywords:

```bash
python autostlpipeline.py --search "star wars"
```
By default, the number of page to be download is 1 and items are sorted in the newest order.

*[tweak], [upload], and [rename] take argument 0 and 1.*

For example, if you want to download 10 pages of "gadgets", tweak them into the best orientation, rename them to start with object id (based on the order it is downloaded), and upload to a google drive folder:

```bash
python autostlpipeline.py --search "gadgets" --pages 10 --tweak 1 --upload 1 --rename 1
```

## Tweaking Function
The Tweaking function is simplified version of github.com/ChristophSchranz/Tweaker-3, read this page for more detail of the tweaker algorithm.

## Download File Location

All the stls of the objects are downloaded in the folder **/stls**.
