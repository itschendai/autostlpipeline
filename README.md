# Thingiver Downloader + STL Orientation Tweaker + Google Drive Uploader Tool

**Remember to put thingiverse API TOKEN** inside the file **api_credentials.ini**

**Remember to put Google API Credential** as file **credential.json**

**Remember to put google drive folder id** in the code if you want to use upload

## Use

Type in your terminal to know all the options:

```bash
python autostlpipeline.py --help
```

For example, if you want to search objects by keywords:

```bash
python autostlpipeline.py --search "star wars"
```
By default, the number of page to be download is 1 and items are sorted in from newest order.

[tweak], [upload], and [rename] takes argument 0 and 1.

For example, if you want to download 10 pages of gadgets, tweak them, rename to start with item id, and upload:

```bash
python autostlpipeline.py --search "gadgets" --pages 10 --tweak 1 --upload 1 --rename 1
```

## Tweaking Function
The Tweaking function is simplified version of github.com/ChristophSchranz/Tweaker-3, read this page for more detail of the tweaker algorithm.

## Where are the objects

All the stls of the objects are downloaded at the folder **stls**.
