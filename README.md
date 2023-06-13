# Segment Anything Labelling Tool (SALT)

Uses the Segment-Anything Model By Meta AI and adds a barebones interface to label images and saves the masks in the COCO format.

Under active development, apologies for rough edges and bugs. Use at your own risk.

## Installation
### For mac M1 
Open your terminal and run 
```shell
conda env create -f environment.yaml
```
```shell
conda activate sam 
```
### For Win/Linux 
```shell
conda create -n sam python=3.9 
```
```shell
conda activate sam 
```
```shell
pip install -r requirements.txt
```

## Usage
1. Please use the hcmus account to download the dataset in this [link](https://studenthcmusedu.sharepoint.com/:u:/r/sites/Thgicmytnh/Shared%20Documents/%C4%90%E1%BB%93%20%C3%A1n/DATASET/dataset.zip?csf=1&web=1&e=6VtJTd), and extract it to the current folder
2. Download the .onnx model in this [link](https://github.com/quyen228/salt/releases/download/v0.1.0/sam_onnx.570_520.onnx), and save it to `models` folder
3. Run:
```shell
python segment_anything_annotator.py 
```
    There are a few keybindings that make the annotation process fast.
    - Click on the object using left clicks and right click (to indicate outside object boundary).
    - `n` adds predicted mask into your annotations. (Add button)
    - `r` rejects the predicted mask. (Reject button)
    - `a` and `d` to cycle through images in your your set. (Next and Prev)
    - `l` and `k` to increase and decrease the transparency of the other annotations.
    - `Ctrl + S` to save progress to the COCO-style annotations file.

## Demo

![How it Works Gif!](https://github.com/anuragxel/salt/raw/main/assets/how-it-works.gif)

## Contributing

Follow these guidelines to ensure that your contributions can be reviewed and merged. Need a lot of help in making the UI better.

If you have found a bug or have an idea for an improvement or new feature, please create an issue on GitHub. Before creating a new issue, please search existing issues to see if your issue has already been reported. 

When creating an issue, please include as much detail as possible, including steps to reproduce the issue if applicable.

Create a pull request (PR) to the original repository. Please use `black` formatter when making code changes.

## License

The code is licensed under the MIT License. By contributing to SALT, you agree to license your contributions under the same license as the project. See LICENSE for more information.
