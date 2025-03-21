# ComfyUI for Modal.com

This repository provides simple modal run files to run and get a link to use comfyUI hosted on powerful GPUs from (Modal)[https://modal.com]

![Wan2.1 Example](https://github.com/cyboghostginx/images.jpeg)

## Features

- Text-to-Video generation (480p or 720p)
- Image-to-Video generation (480p or 720p)
- Support for both landscape and portrait orientations
- Easy-to-use interactive script for model selection and configuration
- Compatible with local and cloud GPU environments

## Requirements

- NVIDIA GPU with CUDA support (at least 8GB VRAM for 1.3B model, 24GB+ recommended for 14B models)
- CUDA 12.x
- Python 3.8+
- Git

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

## Models and Capabilities

The script supports the following Wan2.1 models:

1. **1.3B Text-to-Video (T2V) model**:
   - Fastest generation
   - Supports 480p resolution
   - Lower resource requirements (8GB+ VRAM)
   - Good for simple scenes and concepts

2. **14B Text-to-Video (T2V) model**:
   - Higher quality generation
   - Supports both 480p and 720p
   - Higher resource requirements (24GB+ VRAM)
   - Better for complex scenes and concepts

3. **14B Image-to-Video (I2V) 480p model**:
   - Animates a still image
   - Maintains visual fidelity to input image
   - Requires 24GB+ VRAM

4. **14B Image-to-Video (I2V) 720p model**:
   - Higher resolution animation of still images
   - Best visual quality
   - Requires 32GB+ VRAM

## Resolution Options

| Model              | Landscape 480p | Landscape 720p | Portrait 480p | Portrait 720p |
|--------------------|----------------|----------------|---------------|---------------|
| 1.3B T2V           | ✅             | ❌             | ✅            | ❌            |
| 14B T2V            | ✅             | ✅             | ✅            | ✅            |
| 14B I2V (480p)     | ✅             | ❌             | ✅            | ❌            |
| 14B I2V (720p)     | ❌             | ✅             | ❌            | ✅            |

## Tips for Better Results

- **Prompting**: Be detailed and specific in your text prompts. Include style descriptions, lighting, composition details.
- **Image Inputs**: For I2V models, use clear, high-quality source images without text or watermarks.
- **VRAM Management**: Close other applications when running locally to free up VRAM.
- **Multiple Generations**: Try different prompts and seeds for varied results.

## Troubleshooting

### Common Issues

- **CUDA Out of Memory**: Try using a smaller model or lower resolution. Close other GPU applications.
- **Model Download Failures**: Check your internet connection and Hugging Face login status.
- **Dependencies Installation Errors**: Try running `pip install -r requirements.txt` manually.

### VRAM Requirements

| Model              | Minimum VRAM | Recommended VRAM |
|--------------------|--------------|------------------|
| 1.3B T2V           | 8GB          | 12GB             |
| 14B T2V (480p)     | 16GB         | 24GB             |
| 14B T2V (720p)     | 24GB         | 32GB             |
| 14B I2V (480p)     | 24GB         | 32GB             |
| 14B I2V (720p)     | 32GB         | 48GB             |

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- This script is a wrapper for the [Wan2.1](https://github.com/Wan-Video/Wan2.1) model
- Models created by Wan-AI

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
