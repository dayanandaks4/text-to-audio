# 🎵 Text-to-Audio Conversion System

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-red)](https://pytorch.org)
[![Transformers](https://img.shields.io/badge/🤗%20Transformers-4.30%2B-yellow)](https://huggingface.co/transformers)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

A **complete text-to-speech (TTS) system** using lightweight Hugging Face models that converts text questions to high-quality audio answers. Perfect for creating educational content, audiobooks, accessibility tools, and voice assistants.

## ✨ Features

- 🤖 **Lightweight TTS Models**: Uses efficient Hugging Face models (Microsoft SpeechT5)
- 📝 **Advanced Text Processing**: Smart preprocessing and tokenization
- 🎵 **High-Quality Audio**: Multiple format support (WAV, MP3, FLAC, OGG)
- 🎓 **Question-Answer Mode**: Perfect for educational content
- 📦 **Batch Processing**: Handle multiple texts efficiently
- 🔧 **Easy Integration**: Simple API for embedding in other projects
- 📊 **Training Support**: Dataset integration for model fine-tuning
- 🎯 **Production Ready**: Comprehensive error handling and logging

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/text-to-audio-huggingface.git
cd text-to-audio-huggingface

# Install dependencies
pip install -r requirements.txt
```

### Basic Usage

```python
from src.main import TextToAudioConverter

# Initialize converter
converter = TextToAudioConverter()

# Convert text to audio
audio_path = converter.convert_text("Hello, this is a test message!")
print(f"Audio saved to: {audio_path}")

# Question-Answer format
qa_pairs = [
    {
        "question": "What is AI?",
        "answer": "Artificial Intelligence is the simulation of human intelligence in machines."
    }
]
audio_files = converter.convert_questions_and_answers(qa_pairs)
```

### Run Examples

```bash
# Simple example
python examples/simple_example.py

# Question-Answer demo
python examples/qa_example.py

# Batch processing
python examples/batch_example.py

# Interactive Jupyter notebook
jupyter notebook examples/text_to_audio_demo.ipynb
```

## 📁 Project Structure

```
text-to-audio-huggingface/
├── 📂 src/
│   ├── 🐍 main.py                 # Main application
│   ├── 🐍 text_processor.py       # Text preprocessing
│   ├── 🐍 tts_model.py           # TTS model integration
│   ├── 🐍 audio_processor.py     # Audio processing
│   └── 🐍 dataset_manager.py     # Dataset management
├── 📂 examples/
│   ├── 🐍 simple_example.py       # Basic usage
│   ├── 🐍 qa_example.py          # Q&A demo
│   ├── 🐍 batch_example.py       # Batch processing
│   ├── 🐍 dataset_example.py     # Dataset demo
│   ├── 🐍 integration_test.py    # Full testing
│   └── 📓 text_to_audio_demo.ipynb # Interactive notebook
├── 📂 data/                      # Training datasets
├── 📂 models/                    # Model storage
├── 📂 output/                    # Generated audio files
├── 📄 requirements.txt           # Dependencies
├── 📄 README.md                  # This file
└── 📄 PROJECT_SUMMARY.md         # Detailed project info
```

## 🎯 Use Cases

- 🎓 **Educational Content**: Convert textbooks to audiobooks
- ❓ **FAQ Systems**: Generate audio answers for common questions
- ♿ **Accessibility**: Text-to-speech for visually impaired users
- 🤖 **Voice Assistants**: Create custom voice responses
- 📚 **Content Creation**: Generate narration for videos/podcasts
- 🌐 **Multilingual Support**: Convert text in different languages

## 🤖 Supported Models

| Model | Provider | Type | Quality | Speed |
|-------|----------|------|---------|-------|
| SpeechT5 TTS | Microsoft | Single-speaker | High | Fast |
| FastSpeech2 | Facebook | Single-speaker | High | Very Fast |
| VITS | Various | Multi-speaker | Very High | Medium |

## 📊 Training Datasets

- 📀 **LJSpeech**: High-quality single speaker dataset
- 📚 **LibriTTS**: Multi-speaker English dataset
- 🌍 **Common Voice**: Community-driven multilingual dataset
- 🔧 **Custom Datasets**: Support for your own data

## 🔧 Advanced Configuration

```python
# Custom configuration
converter = TextToAudioConverter(
    model_name="microsoft/speecht5_tts",
    output_dir="my_audio_files",
    device="cuda"  # Use GPU if available
)

# Update settings
converter.update_config(
    audio_format="mp3",
    normalize_audio=True,
    apply_fade=True,
    noise_reduction=True
)
```

## 📈 Performance

- ⚡ **Real-time Processing**: Faster than audio playback
- 💾 **Memory Efficient**: Optimized for production use
- 🎵 **High Quality**: 16kHz audio output
- 📦 **Batch Ready**: Process multiple texts efficiently

## 🧪 Testing

```bash
# Run comprehensive tests
python examples/integration_test.py

# Expected output:
# 🎉 ALL TESTS PASSED! System is fully functional.
# Tests passed: 4/4 (100% success rate)
```

## 🛠 System Requirements

- **Python**: 3.8 or higher
- **PyTorch**: 2.0 or higher
- **Memory**: 2GB RAM minimum (4GB recommended)
- **Storage**: 1GB for models and dependencies
- **Audio**: System audio drivers for playback

## 📋 Dependencies

Core packages automatically installed:
- `torch>=2.0.0` - Deep learning framework
- `transformers>=4.30.0` - Hugging Face models
- `soundfile>=0.12.1` - Audio I/O
- `librosa>=0.10.0` - Audio processing
- `datasets>=2.12.0` - Dataset management
- `nltk>=3.8` - Text processing

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Hugging Face](https://huggingface.co) for the amazing Transformers library
- [Microsoft](https://microsoft.com) for the SpeechT5 model
- [Facebook Research](https://research.facebook.com) for FastSpeech2
- The open-source community for datasets and tools

## 📞 Support

If you encounter any issues or have questions:

1. Check the [examples/](examples/) directory for usage examples
2. Run the integration test: `python examples/integration_test.py`
3. Open an issue on GitHub
4. Check the [PROJECT_SUMMARY.md](PROJECT_SUMMARY.md) for detailed information

---

**⭐ If this project helped you, please give it a star on GitHub! ⭐**