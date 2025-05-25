# FramePack CLI Usage

Teraz możesz używać `demo_gradio.py` zarówno w trybie Gradio jak i CLI.

## Tryb CLI

Aby uruchomić w trybie CLI, dodaj flagę `--cli`:

### Podstawowe użycie
```bash
python demo_gradio.py --cli --input_image path/to/image.jpg --prompt "Your prompt here"
```

### Przykłady

1. **Podstawowe generowanie wideo:**
```bash
python demo_gradio.py --cli -i my_photo.jpg -p "The person dances gracefully"
```

2. **Z niestandardowymi parametrami:**
```bash
python demo_gradio.py --cli -i dancer.jpg -p "Graceful dance movements" --length 8.0 --seed 12345 --output my_video.mp4
```

3. **Wysokiej jakości ustawienia:**
```bash
python demo_gradio.py --cli -i portrait.jpg -p "Gentle nodding" --steps 35 --mp4_crf 0
```

4. **Optymalizacja pamięci:**
```bash
python demo_gradio.py --cli -i photo.jpg -p "Subtle movement" --gpu_memory 12.0 --no_teacache
```

## Wszystkie opcje CLI

### Wymagane:
- `--cli` - Włącz tryb CLI
- `--input_image`, `-i` - Ścieżka do obrazka
- `--prompt`, `-p` - Prompt tekstowy

### Opcjonalne:
- `--output`, `-o` - Ścieżka wyjściowa (domyślnie: auto w ./outputs/)
- `--negative_prompt`, `-n` - Negatywny prompt (domyślnie: pusty)
- `--seed`, `-s` - Seed (domyślnie: 31337)
- `--length`, `-l` - Długość w sekundach (domyślnie: 5.0)
- `--steps` - Liczba kroków (domyślnie: 25)
- `--cfg` - CFG scale (domyślnie: 1.0)
- `--distilled_cfg` - Distilled CFG scale (domyślnie: 10.0)
- `--cfg_rescale` - CFG rescale (domyślnie: 0.0)
- `--gpu_memory` - Pamięć GPU w GB (domyślnie: 6.0)
- `--no_teacache` - Wyłącz TeaCache
- `--mp4_crf` - Kompresja MP4 (domyślnie: 16)
- `--latent_window_size` - Rozmiar okna (domyślnie: 9)

## Tryb Gradio (domyślny)

Bez flagi `--cli` uruchamia się normalny interfejs Gradio:

```bash
python demo_gradio.py
python demo_gradio.py --share
python demo_gradio.py --server 127.0.0.1 --port 7860
```

## Pomoc

```bash
python demo_gradio.py --help
``` 