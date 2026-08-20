# Hajimi Vertex models

Custom model list for Hajimi on Google Cloud Gemini Enterprise Agent Platform (formerly Vertex AI Generative AI).

Render environment variable:

```text
VERTEX_MODELS_CONFIG_URL=https://raw.githubusercontent.com/APK0/hajimi-vertex-models/main/vertexModels.json
```

## Adding a new Gemini model

1. Check the official [Google models catalog](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/google-models) and [model lifecycle page](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/model-versions).
2. Open the model's documentation page and copy its exact **Model ID**. Do not infer the ID from the marketing name.
3. Test the model against the Hajimi OpenAI-compatible endpoint before publishing it.
4. Edit `vertexModels.json` and add the model ID to `vertex_models` only. Add it to `vertex_express_models` only after separately verifying Vertex Express mode.
5. Commit the file, then restart or manually redeploy the Render service so Hajimi reloads the JSON.

Do not add Live API, embedding, robotics, or other models that are not compatible with Hajimi's Chat Completions route.

