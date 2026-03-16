# Moodboard-Agent

# AI Moodboard Generator Workflow (n8n + Gemini + Hugging Face)
This project is an automated pipeline built in n8n that transforms a simple text idea into a fully generated moodboard-style image.
It integrates Google Gemini 2.5 Flash for prompt engineering and Hugging Face’s FLUX Schnell model for final image synthesis.

The workflow is lightweight, modular, and designed for creative automation, prototyping, and AI-assisted design tools.

## Features

Real-time chat input → capture user requests instantly

LLM-powered prompt engineering using Gemini

Custom JS cleaning layer for safe API payloads

Image generation via Hugging Face Inference API

End-to-end workflow orchestration inside n8n

Produces high-quality PNG moodboard images

## Workflow Overview
User Message → Gemini Prompt Generator → JS Clean Prompt → Hugging Face Image Generator → PNG Output

1. Chat Trigger

Captures any user input (e.g., “Scandinavian living room with a round jute rug”).

2. Prompt Generation (Gemini 2.5 Flash)

Transforms short or vague ideas into highly detailed, structured prompts suitable for image generation.
Includes a system prompt that behaves like a professional image prompt engineer.

3. Clean Prompt (JavaScript Function)

Removes markdown, extra spacing, and sanitizes quotes to ensure compatibility with external APIs.

4. Image Generation (Hugging Face FLUX Schnell)

Sends the cleaned prompt to Hugging Face’s inference endpoint and returns a PNG image.


## Tech Stack

n8n (workflow automation)

Google Gemini 2.5 Flash (LLM prompt engineering)

JavaScript (data cleaning)

Hugging Face Inference API (image generation)

FLUX Schnell Model (visual synthesis)

## Screenshots
<img width="1807" height="837" alt="Screenshot 2025-12-02 at 10 47 08 PM" src="https://github.com/user-attachments/assets/65c7119b-a4d6-417f-9a3c-c48152a584c1" />

<img width="1031" height="463" alt="Screenshot 2025-12-02 at 10 47 43 PM" src="https://github.com/user-attachments/assets/f635a6f1-34d9-480d-8463-729ae42617f0" />

<img width="1848" height="879" alt="Screenshot 2025-12-02 at 10 48 35 PM" src="https://github.com/user-attachments/assets/8a686905-647f-4308-a3f1-0525eaf3f79a" />

<img width="1877" height="788" alt="Screenshot 2025-12-02 at 10 48 54 PM" src="https://github.com/user-attachments/assets/93a6adb8-1961-4ed3-b84d-f1c3faabe272" />

<img width="1871" height="826" alt="Screenshot 2025-12-02 at 10 49 20 PM" src="https://github.com/user-attachments/assets/a62c9878-f5dc-473f-91b7-f1aefa3e955d" />

<img width="1577" height="616" alt="Screenshot 2025-12-02 at 10 49 52 PM" src="https://github.com/user-attachments/assets/75068e8b-4981-45bc-805f-8edb3514e558" />



## Why I Built This

I wanted to explore how LLMs and image models could be orchestrated inside a no-code/low-code environment. This workflow demonstrates:

LLM chaining

Prompt engineering patterns

API orchestration

Data sanitation in automation pipelines

Rapid prototyping for creative AI workflows



## Future Improvements

Add a feedback loop to refine prompts automatically

Support multiple image models (SDXL, Midjourney API wrappers, etc.)

Allow users to choose style presets

Add logging + analytics for prompt/image quality tracking


## Demo Video
https://www.loom.com/share/49461636da0f454bb39b419e2e114150




