# Text-to-Audio Project

A comprehensive text-to-speech (TTS) system using lightweight Hugging Face models that converts text questions to audio answers.

## Features

- **Lightweight TTS Models**: Uses efficient Hugging Face models for text-to-speech conversion
- **Text Processing**: Advanced text preprocessing and tokenization
- **Audio Output**: High-quality audio generation with multiple format support
- **Training Support**: Dataset integration for model fine-tuning
- **Easy Integration**: Simple API for embedding in other projects

## Project Structure

```
text-audio/
├── src/
│   ├── text_processor.py      # Text preprocessing and tokenization
│   ├── tts_model.py          # TTS model integration
│   ├── audio_processor.py    # Audio processing and output
│   └── main.py              # Main application
├── data/                    # Training datasets
├── models/                  # Saved models and checkpoints
├── output/                  # Generated audio files
├── examples/               # Example scripts and notebooks
├── requirements.txt        # Python dependencies
└── README.md              # This file
```

## Quick Start

1. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Run the Application**:
   ```python
   from src.main import TextToAudioConverter
   
   converter = TextToAudioConverter()
   audio_path = converter.convert_text("Hello, this is a test message!")
   print(f"Audio saved to: {audio_path}")
   ```

## Supported Models

- Microsoft SpeechT5 TTS
- Facebook FastSpeech2
- Other lightweight Hugging Face TTS models

## Training Datasets

- LJSpeech Dataset
- LibriTTS
- Custom dataset support

## Usage Examples

See the `examples/` directory for detailed usage examples and Jupyter notebooks.

## Requirements

- Python 3.8+
- PyTorch 2.0+
- Transformers 4.30+
- Audio drivers for playback

## License

MIT License