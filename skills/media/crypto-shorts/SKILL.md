# Crypto Shorts (MP4) Skill

Generate a 1080x1920 crypto Shorts video (mp4) with:
- CoinGecko description + logo
- English voiceover (Edge TTS)
- Bottom subtitles
- ffmpeg render

## Use
Ask for example:
- "make a crypto video about Bitcoin"
- "create a short video explaining Solana"

## Requirements (WSL Ubuntu)
terminal(command="sudo apt update && sudo apt install -y ffmpeg python3 python3-venv python3-pip", timeout=600)
terminal(command="python3 -m pip install --upgrade pip && python3 -m pip install edge-tts", timeout=600)

## Generate 1 video (mp4)
# Replace bitcoin with any coin name/symbol (e.g. ethereum, solana, dogecoin)
terminal(command="python3 SKILL_DIR/scripts/make_crypto_short.py --coin bitcoin --out_dir ./out", timeout=900)

## Verify output
terminal(command="ls -lt out/*.mp4 | head -n 3", timeout=60)
