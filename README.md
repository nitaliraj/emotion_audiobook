#  Emotion-Aware Multi-Voice Generative Audiobook System

## Overview

The **Emotion-Aware Multi-Voice Generative Audiobook System** is an AI-powered application that transforms plain literary text into immersive, expressive audiobooks using Generative AI, Natural Language Processing (NLP), and Text-to-Speech (TTS) technologies.

Unlike conventional audiobook generators that produce monotonous narration, this system understands the emotional context of a story, identifies different characters, assigns distinct voices, and generates emotion-aware speech with appropriate tone, pitch, speed, and volume.

It also integrates AI-generated sound effects and background ambience to create a more engaging and cinematic listening experience.

##  Key Features

- **AI-Powered Narrative Analysis:** Uses Gemini 2.5 Flash to understand story context, identify characters, analyze dialogue, and detect emotions.
- **Emotion-Aware Voice Generation:** Adjusts pitch, speaking rate, and volume according to the emotional context of each segment.
- **Multi-Voice Character Assignment:** Assigns consistent and distinguishable voices to different characters.
- **Multiple TTS Engines:** Integrates Edge-TTS, Parler-TTS, gTTS, and eSpeak for speech generation.
- **AI-Generated Sound Effects:** Uses AudioLDM to generate contextual sound effects based on story events.
- **CLAP-Based Sound Selection:** Uses Contrastive Language-Audio Pretraining (CLAP) to rank and select relevant sound effects.
- **Background Ambience:** Combines narration with environmental audio to improve immersion.
- **Audio Processing:** Supports audio mixing, normalization, and segment-level processing.
- **Interactive Application:** Provides a Streamlit interface for generating and reviewing audiobooks.
- **Segment Regeneration:** Allows individual audio segments to be reviewed and regenerated.

##  System Architecture

The system follows an 11-stage generative AI pipeline:

1. **Text Input:** Accepts raw literary text as input.
2. **Text Preprocessing:** Cleans and prepares the input for analysis.
3. **Narrative Analysis:** Uses Gemini 2.5 Flash to understand the story, context, characters, and emotions.
4. **Speaker Segmentation:** Identifies dialogue and associates it with individual characters.
5. **Emotion Detection:** Determines the emotional state of each narrative segment.
6. **Emotion-to-Prosody Mapping:** Converts detected emotions into speech parameters such as pitch, rate, and volume.
7. **Voice Assignment:** Maps characters to consistent voices using a voice-mapping mechanism.
8. **Speech Generation:** Generates narration using multiple TTS engines.
9. **Sound Effect Generation:** Uses AudioLDM to generate contextually relevant sound effects.
10. **Audio Selection and Mixing:** Applies CLAP-based ranking, background ambience, audio mixing, and normalization.
11. **Final Audiobook Generation:** Produces the final expressive audiobook for listening and review.

##  Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Frontend | Streamlit |
| Generative AI | Gemini 2.5 Flash |
| NLP | Transformers |
| Text-to-Speech | Edge-TTS, Parler-TTS, gTTS, eSpeak |
| Audio Generation | AudioLDM, Diffusers |
| Audio-Text Similarity | CLAP |
| Audio Processing | Librosa |
| Speech Evaluation | Whisper |
| Data Processing | NumPy, Pandas |
| Visualization | Matplotlib |
| Development Environment | Google Colab, Jupyter Notebook |
| GPU Environment | NVIDIA Tesla T4 / CUDA |

##  Model Evaluation

The project incorporates both objective and subjective evaluation techniques.

**Evaluation metrics include:**

- Word Error Rate (WER)
- Character Error Rate (CER)
- Emotion classification Precision, Recall, and F1-score
- Audio quality measurements
- Mean Opinion Score (MOS)
- CLAP-based sound effect relevance
- Processing time and Real-Time Factor (RTF)

**Reported experimental results:**

| Metric | Result |
|---|---:|
| Word Error Rate (WER) | 5.73% |
| Character Error Rate (CER) | 1.68% |
| Real-Time Factor (RTF) | 0.183 |
| CLAP sound-effect selection improvement | 7 out of 9 evaluated effects |

These results are based on the project's experimental evaluation.

##  Getting Started

### Prerequisites

- Python 3.10 or compatible environment for the selected dependencies
- pip
- Google Gemini API key
- Internet connection for cloud-based services
- GPU support recommended for resource-intensive generative models

### 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_PROJECT_FOLDER>
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows:**
```bash
venv\Scripts\activate
```

**macOS / Linux:**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API Keys

Configure your Gemini API key using an environment variable:

```bash
GEMINI_API_KEY=your_api_key_here
```

Do not upload API keys, credentials, or other sensitive information to GitHub.

### 5. Run the Application

Launch the Streamlit application:

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal to access the application.

##  Project Components

The main project components include:

- `app.py` – Streamlit-based interactive application.
- Evaluation Notebook – Model evaluation, experimental analysis, performance metrics, and visualizations.
- Narrative Analysis – LLM-based story understanding and emotion extraction.
- Voice Mapping – Character identification and consistent voice assignment.
- TTS Integration – Speech generation using multiple TTS engines.
- Sound Generation – Contextual sound effect generation using AudioLDM.
- Audio Processing – Sound effect selection, ambience integration, mixing, and normalization.

Refer to the repository for the complete implementation and supporting files.

## 🔬 Research and Innovation

The project explores the integration of multiple generative AI technologies into a unified audiobook generation framework.

Its primary contributions include:

- Emotion-driven speech synthesis instead of conventional text-to-speech narration.
- Consistent multi-character voice assignment.
- Context-aware sound effect generation.
- CLAP-based sound effect relevance ranking.
- Integration of speech generation, sound design, and audio processing into a single pipeline.
- Human-in-the-loop review and segment-level regeneration.

##  Future Enhancements

- Support for additional languages and multilingual audiobooks.
- Improved emotional intelligence and contextual emotion recognition.
- More realistic and expressive character voices.
- Real-time audiobook generation.
- Enhanced speaker consistency across longer stories.
- Improved sound effect generation and synchronization.
- Cloud deployment for scalable audiobook generation.

##  Project Status

**Working Prototype – Core functionality implemented.**

The system integrates narrative understanding, emotion-aware speech generation, multi-character voice assignment, contextual sound effects, and audio composition into an interactive audiobook generation application.

## 📜 License

This project is intended for academic and research purposes. Licensing and third-party model usage are
