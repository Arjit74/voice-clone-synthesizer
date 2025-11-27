# Synthesizer Model

This directory contains the pre-trained synthesizer model for voice conversion.

## Model Details
- **File**: `synthesizer.pt`
- **Size**: ~370.6 MB
- **Input**: Text or linguistic features + Speaker embeddings
- **Output**: Mel-spectrograms

## Usage
```python
# Load the synthesizer model
synthesizer = torch.load('synthesizer.pt')

# Generate mel-spectrogram from text and speaker embedding
with torch.no_grad():
    mel_output = synthesizer(text_input, speaker_embedding)
```

## Dependencies
- PyTorch
- NumPy
- Text processing utilities (for text input)
- Audio processing libraries (for mel-spectrogram conversion)

## Model Configuration
See `config.json` for model architecture and training parameters.