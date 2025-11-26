# Gowthamtj17-SeamlessSpeech-Multilingual-Speech-Text-Translator

A powerful Gradio-based interface built on Facebook’s SeamlessM4T-v2 model for multilingual speech ↔ text translation and generation.

<img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-36-02" src="https://github.com/user-attachments/assets/215ad49d-0078-4c03-b099-b681a551fcb4" />


This project supports:

   1) ASR — Automatic Speech Recognition (Audio → Text)  <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-28-16" src="https://github.com/user-attachments/assets/01110fc8-f784-4033-bad7-ca6f075e9a06" />

   2) S2TT — Speech → Translated Text <img width="1920" height="1080" alt="Screenshot from 2025-11-26 15-59-36" src="https://github.com/user-attachments/assets/2b732e54-3313-4110-b609-21cc5c9948f2" />

   3) S2ST — Speech → Speech Translation <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-24-28" src="https://github.com/user-attachments/assets/725f3a82-2f23-493d-a3d8-813d93ee5ef1" />

   4) T2ST — Text → Speech Generation <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-12-08" src="https://github.com/user-attachments/assets/69eae1c6-f723-4c0e-9eb4-59d9c314a7c7" />

   5) T2TT — Text → Text Translation <img width="1920" height="1080" alt="Screenshot from 2025-11-26 16-08-53" src="https://github.com/user-attachments/assets/b1c426ce-b82b-4b7a-85d0-f2489cc522ba" />


🚀 Features

   1) Multilingual speech & text translation    
   2) Upload or record audio
   3) Convert speech to speech, speech to text, text to speech, and text to text
   4) Automatic 16 kHz audio preprocessing
   5) Supports GPU acceleration via PyTorch    
   6) Clean Gradio UI with task-based flow   
   7) Audio output saved as .wav
				
Install dependencies

        pip install torch torchvision torchaudio
        pip install transformers soundfile librosa gradio numpy

📘 Supported Tasks:

 1. ASR (Audio → Text):
    
    Upload audio
       
    Click Run
     
    Output displays recognized text

 3. S2TT (Speech → Translated Text):
    
    Upload audio
    
    Select target language
    
    Produces translated text

 4. S2ST (Speech → Speech Translation):
    
    Upload audio
    
    Choose target language
    
    Generates translated .wav output

 5. T2ST (Text → Speech Translation):
    
    Provide text
    
    Choose source & target language
    
    Generates spoken audio output
    
 6. T2TT (Text → Text Translation):
    
    Enter text
    
    Select target language
    
    Produces translated text

🌍 Available Languages

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

⚙️ How It Works

1) Audio is always resampled to 16 kHz using librosa.	
2) Model outputs either:
   1) text tokens → decoded via processor.decode
   2) audio tensors → saved as .wav    
3) GPU is automatically used if available (torch.cuda.is_available())

🧪 Troubleshooting

  Issue	Fix

  1) Slow processing	Use GPU runtime (especially in Colab)
  2) CUDA OOM	Reduce input length or switch to CPU
  3) Audio not playing	Ensure file is written correctly at 16 kHz
  4) Wrong translation	Verify tgt_lang code
