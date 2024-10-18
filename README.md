## AI MEME GENERATOR

## Overview

The AI Meme Generator is a free and open-source Python program that fully automates the process of generating AI-driven memes. It uses GPT-4 for text generation and multiple image generation APIs (such as ClipDrop and Stability AI’s DreamStudio) to create images, combining the two to deliver hilarious, fully automatic memes. The program is highly customizable, allowing users to provide specific instructions for memes or let the AI decide the content.

This tool is perfect for creating memes about anything, from computers to cats, and is open-source, meaning anyone can modify and improve it. Additionally, a Twitter bot using this generator posts memes automatically every six hours.

## Features

- **100% AI-generated memes**: Fully automated, from text creation to image generation.
- **GPT-4 Powered**: Uses GPT-4 API for creating meme text and image prompts.
- **Multiple Image Generators**: Supports image generation platforms like ClipDrop and Stability AI for varied results.
- **Customizable**: Control meme topics, visual styles, and more through customizable settings.
- **Command-Line Options**: Fully automate meme creation with optional command-line arguments.
- **Executable Version**: An easy-to-use `.EXE` version will be available soon.
- **Automated Twitter Bot**: A Twitter bot generates and posts memes automatically using this tool.

## Installation

1. **Clone the Repository**:
   bash
   git clone https://github.com/your-repo-link/AI-Meme-Generator.git
   cd AI-Meme-Generator
   

2. **Install Dependencies**:
   The program requires Python and several packages, which can be installed with:
   bash
   pip install -r requirements.txt
   

3. **Set Up API Keys**:
   - You need an **OpenAI API key** for generating meme text via GPT-4.
   - Optionally, get a **ClipDrop API key** or **Stability AI (DreamStudio) API key** for generating better-quality images.

   Create a file named `api_keys.txt` in the project directory and add the following lines:
   bash
   OPENAI_API_KEY=your_openai_key_here
   CLIPDROP_API_KEY=your_clipdrop_key_here (optional)
   STABILITY_API_KEY=your_stability_key_here (optional)
   

4. **Run the Program**:
   You can launch the program using the following command:
   bash
   python main.py
   

## How It Works

1. The program sends an API request to GPT-4 with a prompt to create meme text.
2. GPT-4 generates the meme text and an image prompt.
3. The image prompt is sent to an image generation API (ClipDrop, Stability AI, or other supported services).
4. The program combines the generated text and image to produce the final meme.
5. The meme is saved in the `output` folder along with a log file for reference.

### Example Usage

- **General Meme**: Run the program without any specific input, and it will generate a random meme.
- **Custom Meme**: You can specify a topic like "cats and computers" for more specific memes.
  
bash
# Example: Create a meme about cats and computers
python main.py --subject "cats and computers"


## Configuration

The program creates a `settings.ini` file on the first run. You can edit this file to customize various parameters such as:

- **Default Meme Topics**: Specify default meme themes like "funny memes about cars."
- **Image Styles**: Choose whether the images are photographic, illustrations, or other styles.
- **Font Choices**: Customize the meme text font.


# Basic settings
MEME_TOPIC="computers"
IMAGE_STYLE="photographic"
FONT="Arial"

## Command-Line Arguments

You can also pass options into the program via command-line arguments.

### API Key Arguments:
- `--openaikey`: OpenAI API key.
- `--clipdropkey`: ClipDrop API key.
- `--stabilitykey`: Stability AI API key.

### Basic Meme Arguments:
- `--userprompt`: A meme subject or concept to send to the AI. If not specified, the user will be prompted for input.
- `--memecount`: The number of memes to generate (default is 1).

### Advanced Meme Settings:
- `--imageplatform`: Choose the image generation platform (`clipdrop`, `stability`, `openai`).
- `--temperature`: Adjust GPT-4 creativity (default is 1.0).
- `--basicinstructions`: Instructions for the AI regarding meme style.
- `--imagespecialinstructions`: Instructions for how the image should look.

### Binary Arguments:
- `--nouserinput`: Skips user input, using default values or arguments.
- `--nofilesave`: The meme will not be saved, only returned as a virtual file.

## Example Output with Log
![Example Meme](https://github.com/ThioJoe/Full-Stack-AI-Meme-Generator/assets/12518330/6400c973-f7af-45ed-a6ad-c062c2be0b64)

```
Meme File Name: meme_2023-07-13-15-34_ZYKCV.png
AI Basic Instructions: You will create funny memes.
AI Special Image Instructions: The images should be photographic.
User Prompt: 'cats'
Chat Bot Meme Text: "When you finally find the perfect napping spot... on the laptop."
Chat Bot Image Prompt: "A photograph of a cat laying down on an open laptop."
Image Generation Platform: ClipDrop
```

## Optional Settings and Instructions

- **Special Image Instructions**: Specify image styles like "photographic" or "illustration." You can even specify more unique characteristics, such as always featuring cats.
- **Font Settings**: Customize the meme font for a unique look.

## Automated Twitter Bot

A fully automated Twitter bot generates and posts memes every six hours using this tool. Follow it [here](https://twitter.com/your-twitter-bot-link).

## How to Build the .EXE Version

1. **Install PyInstaller**:
   ```bash
   pip install pyinstaller
   ```

2. **Build the .EXE**:
   Run the following command from the project directory:
   ```bash
   python -m PyInstaller main.spec
   ```



## License

This project is licensed under the MIT License.

## Links

- [GitHub Repository](https://github.com/ThioJoe/Full-Stack-AI-Meme-Generator)
- [Youtube tutorial] (https://www.youtube.com/watch?v=7LBLESXAJh0)

