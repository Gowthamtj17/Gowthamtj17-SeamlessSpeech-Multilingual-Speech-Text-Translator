<h1>🎙️SeamlessSpeech-Multilingual-Speech-Text-Translator</h1>

A powerful Gradio-based interface built on Facebook’s SeamlessM4T-v2 model for multilingual speech ↔ text translation and generation.

<img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-36-02" src="https://github.com/user-attachments/assets/215ad49d-0078-4c03-b099-b681a551fcb4" />


<h3>📝 This project supports:</h3>

   <h4>1) ASR — Automatic Speech Recognition (Audio → Text)</h4>  <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-28-16" src="https://github.com/user-attachments/assets/01110fc8-f784-4033-bad7-ca6f075e9a06" />

   <h4>2) S2TT — Speech → Translated Text</h4> <img width="1920" height="1080" alt="Screenshot from 2025-11-26 15-59-36" src="https://github.com/user-attachments/assets/2b732e54-3313-4110-b609-21cc5c9948f2" />

   <h4>3) S2ST — Speech → Speech Translation</h4> <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-24-28" src="https://github.com/user-attachments/assets/725f3a82-2f23-493d-a3d8-813d93ee5ef1" />

   <h4>4) T2ST — Text → Speech Generation</h4> <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-12-08" src="https://github.com/user-attachments/assets/69eae1c6-f723-4c0e-9eb4-59d9c314a7c7" />

   <h4>5) T2TT — Text → Text Translation</h4> <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-08-53" src="https://github.com/user-attachments/assets/b1c426ce-b82b-4b7a-85d0-f2489cc522ba" />


<h3>🚀 Features</h3>

   1) Multilingual speech & text translation    
   2) Upload or record audio
   3) Convert speech to speech, speech to text, text to speech, and text to text
   4) Automatic 16 kHz audio preprocessing
   5) Supports GPU acceleration via PyTorch    
   6) Clean Gradio UI with task-based flow   
   7) Audio output saved as .wav
				
<h3>📦Install dependencies</h3>

        pip install torch torchvision torchaudio
        pip install transformers soundfile librosa gradio numpy

<h3>📘 Supported Tasks:</h3>

 1. ASR (Audio → Text):
    
    1) Upload audio
       
    2) Click Run
     
    3) Output displays recognized text

 3. S2TT (Speech → Translated Text):
    
	1) Upload audio
    
    2) Select target language
    
    3) Produces translated text

 4. S2ST (Speech → Speech Translation):
    
    1) Upload audio
    
    2) Choose target language
    
    3) Generates translated .wav output

 5. T2ST (Text → Speech Translation):
    
    1)  Provide text
    
    2) Choose source & target language
    
    3) Generates spoken audio output
    
 6. T2TT (Text → Text Translation):
    
    1) Enter text
    
    2) Select target language
    
    3) Produces translated text

<h3>🌍 Available Languages</h3>

		English     → eng
		Hindi       → hin
		Tamil       → tam
		Telugu      → tel
		Malayalam   → mal
		Spanish     → spa
		French      → fra
		German      → deu
		Chinese     → zho
		Japanese    → jpn
		Arabic      → ara
		Russian     → rus  
   You can extend this list anytime.

<h3>⚙️ How It Works</h3>

1) Audio is always resampled to 16 kHz using librosa.	
2) Model outputs either:
   1) text tokens → decoded via processor.decode
   2) audio tensors → saved as .wav    
3) GPU is automatically used if available (torch.cuda.is_available())

<h3>🧪 Troubleshooting</h3>

  <h4>Issue	Fix</h4>

  1) Slow processing	Use GPU runtime (especially in Colab)
  2) CUDA OOM	Reduce input length or switch to CPU
  3) Audio not playing	Ensure file is written correctly at 16 kHz
  4) Wrong translation	Verify tgt_lang code
