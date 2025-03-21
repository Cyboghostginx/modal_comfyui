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
git clone https://github.com/yourusername/wan2.1-automation.git
cd wan2.1-automation
```

The installation script will:
1. Clone the Wan2.1 repository
2. Install all required dependencies
3. Allow you to select which model(s) to download
4. Provide instructions for installing additional models later

## Usage

### Running Locally

1. Make the scripts executable:
   ```bash
   chmod +x install_wan2.1.sh generate_wan2.1.sh
   ```

2. First, run the installation script:
   ```bash
   ./install_wan2.1.sh
   ```

3. After installation completes, run the generation script:
   ```bash
   ./generate_wan2.1.sh
   ```

4. Follow the interactive prompts to:
   - Select your model (1.3B or 14B)
   - Choose video orientation and resolution
   - Enter your text prompt or provide an image path
   - Wait for generation to complete

5. Find your generated videos in the `Wan2.1/wan_videos` directory

### Running on Cloud GPU Services

#### Google Colab

1. Create a new notebook in Google Colab
2. Select a GPU runtime (T4 or better recommended)
3. Paste and run the following code:

```python
# Clone the repository
!git clone https://github.com/yourusername/wan2.1-automation.git
%cd wan2.1-automation

# Make the scripts executable
!chmod +x install_wan2.1.sh generate_wan2.1.sh

# Run installation script
!bash install_wan2.1.sh

# Run generation script
!bash generate_wan2.1.sh
```

4. Follow the interactive prompts in the output
5. Generated videos can be found in `Wan2.1/wan_videos/` directory

#### RunPod / Vast.ai / Lambda Labs

1. Create a new instance with at least 24GB VRAM (for 14B models)
2. Connect to the instance via SSH or JupyterLab
3. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/wan2.1-automation.git
   cd wan2.1-automation
   ```
4. Make the scripts executable:
   ```bash
   chmod +x install_wan2.1.sh generate_wan2.1.sh
   ```
5. Run the installation script:
   ```bash
   ./install_wan2.1.sh
   ```
6. Run the generation script:
   ```bash
   ./generate_wan2.1.sh
   ```
7. Follow the interactive prompts
8. Download the generated videos from the `Wan2.1/wan_videos/` directory

## Models to be added

| Model              | Classification |
|--------------------|----------------|
| Flux          | Photo Gen             | 
| Wan (soon)           | Video Gen            | 
| loading..     | soon           | 

## Tips for Better Results

- **H100 GPU**: I usually choose H100 in the script for faster inferencing.
- many more..

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
