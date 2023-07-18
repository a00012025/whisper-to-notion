# Whisper To Notion

## Quick Start

1. Register OpenAI API Key and Notion API token

2. Install [whisper.cpp](https://github.com/ggerganov/whisper.cpp)

3. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

4. Run following command

   ```bash
   export OPENAI_API_KEY=<your-openai-api-key>
   export NOTION_TOKEN=<your-notion-token>
   <path-to-whisper>/stream -m ./models/ggml-large.bin -l ja -t 8 --step 12000 --length 15000 -vth 0.6 --audio-ctx 0 | python write-to-notion.py
   ```
