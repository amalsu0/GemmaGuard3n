# GemmaGuard3n

GemmaGuard3n reimagines child protection through a multimodal, adaptable, privacy-conscious lens. Powered by Gemma 3n, it analyzes video and multilingual audio from real-time CCTV Streams, movies, YouTube, and online content to detect personalized harm indicators adapted to each child's unique safety requirements.


---

## Submission Content

### 1. 📹 Video
🔗 Video Link: https://youtu.be/JneMslKJ8U0?feature=shared
### 2. 📓 Jupyter Notebook
- Contains Gemma 3N loading code, system logic code, testing code, and Gradio demo code.
- Includes testing examples (local video + YouTube links). Results and visualizations are shown inline in the notebook and saved in the `outputs/` folder.
- Provided as PDF and HTML in case of any rendering issues.
### 3. 🌐 Gradio Demo
🔗 Live Demo Link: https://50b6718d7592836380.gradio.live/ (valid for 7 days)
- You can upload your own video or paste a YouTube link.
- If the Gradio link expires (after 7 days), you can watch demo videos in the `demo_recordings/` folder.
- Due to limited resources, processing may take time.
- For faster testing, I included preloaded examples; their results were generated and shown in the notebook, then retrieved in the demo.
### 4. 📄 Technical Writeup
- Includes an explanation of the system, how Gemma 3N was used, and design decisions.


---

## 🚀 Features
- **Multimodal analysis**: Audio + visual inputs
- **Real-time and long-form video processing**
- **Sliding window inference** with overlap
- **Child-specific customization** of harm indicators
- **Multilingual audio support**
- **Timestamped harm scores** with visual feedback
- **Interactive web UI** with Gradio

---

## 🛠️ Installation

### 1. Create and activate the conda environment
```bash
conda create -n gemma3n_env python=3.10 -y
conda activate gemma3n_env
```

### 2. Install PyTorch with CUDA 12.4 support
```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio --index-url https://download.pytorch.org/whl/cu124
```

### 3. Install project dependencies
```bash
pip install \
  accelerate==1.8.1 aiofiles==24.1.0 annotated-types==0.7.0 anyio==4.9.0 \
  audioread==3.0.1 av==14.4.0 certifi==2025.6.15 cffi==1.17.1 charset-normalizer==3.4.2 \
  click==8.2.1 decorator==5.2.1 exceptiongroup==1.3.0 fastapi==0.115.13 ffmpy==0.6.0 \
  filelock==3.18.0 fsspec==2025.5.1 gradio==5.34.2 gradio-client==1.10.3 groovy==0.1.2 \
  h11==0.16.0 hf-transfer==0.1.9 hf-xet==1.1.5 httpcore==1.0.9 httpx==0.28.1 \
  huggingface-hub==0.33.0 idna==3.10 jinja2==3.1.6 joblib==1.5.1 lazy-loader==0.4 \
  librosa==0.11.0 llvmlite==0.44.0 markdown-it-py==3.0.0 markupsafe==3.0.2 mdurl==0.1.2 \
  mpmath==1.3.0 msgpack==1.1.1 networkx==3.4.2 numba==0.61.2 numpy==2.2.6 \
  nvidia-cublas-cu12==12.4.5.8 nvidia-cuda-cupti-cu12==12.4.127 nvidia-cuda-nvrtc-cu12==12.4.127 \
  nvidia-cuda-runtime-cu12==12.4.127 nvidia-cudnn-cu12==9.1.0.70 nvidia-cufft-cu12==11.2.1.3 \
  nvidia-curand-cu12==10.3.5.147 nvidia-cusolver-cu12==11.6.1.9 nvidia-cusparse-cu12==12.3.1.170 \
  nvidia-nccl-cu12==2.21.5 nvidia-nvjitlink-cu12==12.4.127 nvidia-nvtx-cu12==12.4.127 \
  orjson==3.10.18 packaging==25.0 pandas==2.3.0 pillow==11.2.1 platformdirs==4.3.8 \
  pooch==1.8.2 psutil==5.9.8 pycparser==2.22 pydantic==2.11.7 pydantic-core==2.33.2 \
  pydub==0.25.1 pygments==2.19.2 python-dateutil==2.9.0.post0 python-multipart==0.0.20 \
  pytz==2025.2 pyyaml==6.0.2 regex==2024.11.6 requests==2.32.4 rich==14.0.0 ruff==0.12.0 \
  safehttpx==0.1.6 safetensors==0.5.3 scikit-learn==1.7.0 scipy==1.15.3 semantic-version==2.10.0 \
  shellingham==1.5.4 six==1.17.0 sniffio==1.3.1 soundfile==0.13.1 soxr==0.5.0.post1 \
  spaces==0.37.1 starlette==0.46.2 sympy==1.13.1 threadpoolctl==3.6.0 timm==1.0.16 \
  tokenizers==0.21.2 tomlkit==0.13.3 tqdm==4.67.1 transformers==4.53.0 triton==3.1.0 \
  typer==0.16.0 typing-extensions==4.14.0 typing-inspection==0.4.1 tzdata==2025.2 \
  urllib3==2.5.0 uvicorn==0.34.3 websockets==15.0.1
```

### 4. Install additional packages
```bash
pip install opencv-python matplotlib yt_dlp
```

---

## 📦 Technologies Used
- **OpenCV** – For efficient frame sampling and real-time video stream handling
- **Pydub + Librosa** – For processing and segmenting audio streams
- **Gradio** – For building an interactive web-based user interface
- **Gemma 3N** – Google's multilingual multimodal model used for harm detection
- **yt-dlp** – For downloading and processing YouTube videos securely
- **Matplotlib** – To visualize harm scores and timelines
- **Torch + Transformers** – For deep learning inference with HuggingFace support


