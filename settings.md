# Image Generation Settings and Prompts

## Model Settings

* **Model:** Gemini-3-Pro-Image-Preview
* **API Version:** Standard `v1beta`
* **Hyperparameters:** Default settings (no overrides)
* **Package Version:** `google-genai==1.59.0`
* **Image Resolution:** 1408 × 768 pixels
* **Samples per Prompt:** 1

No additional preprocessing was performed.

---

## Prompt Template: Pathology, Pathology+Presentation, and Pathology+Numerosity

```text
Generate a single clinical photograph. Requirements:

- Absolutely NO text, labels, arrows, diagrams, charts, or any graphical overlays on the image.
- Show an adult patient with a clear, unmistakable presentation of this condition, while also following any additional instructions: [Condition prompt here]
- If multiple poses or viewpoints are requested, make one image for each. For example if frontal and lateral views are requested, you need to make two images.
- Never put multiple panels or frames in a single image.
- Only output images. Do not include text or other annotations.
- Choose pose, viewpoint, framing, clothing, and setting as needed so the condition is obvious to a clinician.
- Use natural lighting, realistic skin and fabric, and a photorealistic style.
- Avoid depicting other medical abnormalities unless they would necessarily result from the condition.
```

---

## Prompt Template: Pathology+Pathology, Pathology+Pose, and Pathology+Viewpoint

```text
Generate a single clinical photograph. Requirements:

- Absolutely NO text, labels, arrows, diagrams, charts, or any graphical overlays on the image.
- Show an adult patient with a clear, unmistakable presentation of this condition, while also following any additional instructions: [Condition prompt here]
- If multiple poses or viewpoints are requested, include them in a single image by using multiple panels or frames.
- Only output images. Do not include text or other annotations.
- Choose pose, viewpoint, framing, clothing, and setting as needed so the condition is obvious to a clinician.
- Use natural lighting, realistic skin and fabric, and a photorealistic style.
- Avoid depicting other medical abnormalities unless they would necessarily result from the condition.
```
