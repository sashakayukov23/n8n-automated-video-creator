# n8n Workflow: Automated Content Creation Pipeline for AI-Generated Videos

This project showcases an n8n workflow designed to automate the creation of assets for short-form social media videos. It functions as an end-to-end pipeline that takes a simple story idea and generates a complete set of visual and audio components ready for final assembly.

## What It Does

The workflow is a multi-stage process that leverages several AI models and services to:

1.  **Write a Story:** Takes a user's short message and uses an AI Story agent to generate a structured 8-scene story in a specific cinematic format.
2.  **Generate Images:** For each of the 8 scenes, it engineers a detailed prompt with character consistency guards and uses an AI model to generate a unique image.
3.  **Generate Video Clips:** It then converts each of the 8 images into short video clips.
4.  **Create Voiceover & Captions:** In parallel, it writes a voiceover script in a specific character voice, generates the audio using a Text-to-Speech service (ElevenLabs), and prepares a text file for captions.
5.  **Compose Music:** Finally, it analyses the story's emotional arc to write a detailed prompt for an AI music generator to create a fitting background score.

## A Highly Adaptable Template

While this workflow was built to generate a story of **Frankenstein navigating the modern world**, it is designed to be a flexible template. You can easily adapt it to your own creative projects:

-   **Change the Story:** Modify the prompts inside the AI agents and the initial user input to create stories about any character, topic, or theme.
-   **Swap the AI Models:** The workflow uses HTTP requests to connect to various APIs. You are not locked in! You can easily connect different LLMs, Image/Video/Audio generation models, or other services to suit your needs.

## Part of a Bigger Vision

This workflow successfully generates all the required individual assets. The next logical step could be to fully automate the final assembly and social media publishing.

For example, to achieve this, the chain can be extended with tools like:

-   **Remotion.dev, Blotato.com, or Shotstack.io:** To programmatically merge the video clips and layer the voiceover and music tracks.
-   **Cloudinary:** Its video transformation API can also be used to combine all the assets.
-   **n8n Social Media Nodes or Blotato.com:** Once a final video is rendered, it can be automatically posted to platforms like YouTube, TikTok, and Instagram.

While this workflow is just a fraction of a larger, undisclosed project, it remains a **powerful tool for automating your content creation process**.

**P.S.** This workflow was created before more advanced text-to-video models like Sora 2 were publicly available.

<img width="1644" height="664" alt="n8n_flow-automated-video-creator" src="https://github.com/user-attachments/assets/b25957c6-ed10-4a07-9b0f-f6ec1ea9d1dc" />


<img width="2560" height="1440" alt="Frankenstein Hits the Swiss Alps" src="https://github.com/user-attachments/assets/8ec9e2bc-3400-4a6a-bab0-9d6cf98a6c2e" />
<img width="2560" height="1440" alt="Frank_in_da_City" src="https://github.com/user-attachments/assets/fe4421ec-caca-4613-aee2-0729f938980b" />
<img width="2560" height="1440" alt="Frank_City" src="https://github.com/user-attachments/assets/60941493-c882-410e-854a-8fb9f382550a" />


