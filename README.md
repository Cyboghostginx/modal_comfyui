# ComfyUI for Modal.com

This repository provides simple modal run files to run and get a link to use comfyUI hosted on powerful GPUs from [Modal](https://modal.com)

![comfy Example](https://github.com/Cyboghostginx/modal_comfyui/blob/main/images.jpeg)

## Features

- One-run python installation
- Auto-downloaded needed models
- Auto-downloaded comfy manager
- Persistency in run, and you can always add on models, or nodes later on 
- many more...

## Requirements

- Account at [Modal](https://modal.com)
- Python 11+
- Your computer (:

## Installation

Clone this repository:

```bash
git clone https://github.com/Cyboghostginx/modal_comfyui.git
cd modal_comfyui
pip install -r requirements.txt
```

## Usage

### Running Locally

1. Navigate to the models folder then choose (video-gen or picture-gen or sound-gen) based on your need:
   ```bash
   cd models/{wherever_you_want_eg_wan_is_in_video-gen}
   ```
   
2. Configure your modal with your token:
   ```bash
   pip install modal
   modal setup
   ```
   or if modal setup doesn't work
   ```bash
   python -m modal setup
   ```
   Then follow the link to authenticate and your modal will save everything from your account and ready to use

4. Run Whichever model you like:
   ```bash
   modal run {model_you_want)
   ```

5. Optionally, you can run in detach mode meaning even ctrl+c end won't end your running script:
   ```bash
    modal run -d {model_you_want)
   ```

4. At the end of The run, and all downloads, you will get a tunneling link to access comfyUI:

## Models to be added

| Model              | Classification |
|--------------------|----------------|
| Flux (soon)          | Photo Gen (picture-gen)            | 
| Wan (uploaded)           | Video Gen (video-gen)            | 
| loading..     | soon           | 

## Tips for Better Results

- **H100 GPU**: I usually choose H100 in the script for faster inferencing.
- many more..

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
