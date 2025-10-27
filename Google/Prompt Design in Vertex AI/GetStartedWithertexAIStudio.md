
# Get Started with Vertex AI Studio
>*Created: 27 October 2024 | Last Updated: 27 October 2024*

## Navigation
[Environment Setup](#environment-setup)
[Prompt Creation](#prompt-creation)
[Prompt Engineering](#prompt-engineering)
[Application Deployment](#application-deployment)
[Prompt Comparison](#prompt-comparison)
[Multimodal Processing](#multimodal-processing)
[Model Technical Flows](#model-technical-flows)
[Advanced Features](#advanced-features)
[Error Handling](#error-handling)
[Production Considerations](#production-considerations)
[Technical Parameters](#technical-parameters)
[Model Selection](#model-selection)

---

## Environment Setup
1. Access Google Cloud Console
2. Navigate: Vertex AI > Vertex AI Studio
3. Use temporary lab credentials for secure access
4. Ensure required APIs are enabled:
   - Vertex AI API
   - Cloud Run API
   - Cloud Build API

## Prompt Creation
### Create New Chat Prompt
- Navigation: New > Chat
- Title prompt appropriately

### Configure System Instructions
- Sets global context for all interactions
- Applied before user prompts
- Defines AI assistant role and behavior

### Model Settings Configuration:
- Select model (Gemini 2.5 Flash/Pro)
- Set region (Global)
- Configure parameters:
  - Temperature: 0.1 for factual, 0.8+ for creative
  - Output token limit: 1024 for constrained responses
  - Top-P: 0.8 for focused sampling
  - Thinking Budget: Auto/Manual for reasoning depth

## Prompt Engineering
### Zero-shot Prompting:
- Direct instruction without examples
- Test baseline performance

### Few-shot Prompting:
- Add examples via Examples interface
- Format: Input/Output pairs
- Guide model on expected format and behavior

### Submit and Evaluate:
- Click Submit or press Enter
- Analyze response quality
- Iterate on prompt design

## Application Deployment
### Save Prompt:
- Save to specific region (us-central1)
- Wait for confirmation

### Generate Deployment Code:
- Click Code button
- Select: Deploy > Deploy as app

### Cloud Run Deployment:
- Enable required APIs automatically
- Build container image via Cloud Build
- Deploy to Cloud Run service
- Provide public URL endpoint

### Access Deployed App:
- Open app in new browser tab
- Test with new inputs
- Monitor responses

## Prompt Comparison
### Access Compare Feature:
- Three dots menu > Compare
- Side-by-side interface

### A/B Testing:
- Left pane: Original prompt/config
- Right pane: Modified version
- Changes can include:
  - System instructions
  - Model parameters (Temperature, Top-P)
  - Different models (Flash vs Pro)

### Evaluate Differences:
- Response quality
- Reasoning depth
- Formatting accuracy
- Speed of response

## Multimodal Processing
### Image Analysis with Gemini:
- Import image: + button > Cloud Storage
- Chain prompts for complex analysis:
  1. Describe image
  2. Extract text
  3. Perform calculations/reasoning

### Media Generation:
#### Image Generation (Imagen):
- Navigation: New > Image
- Configure: Model, aspect ratio, count
- Generate and review
- Use AI tools: Inpaint/Outpaint

#### Voice Generation (Chirp):
- Switch to Audio interface
- Configure: Model, language, voice
- Generate and playback

## Model Technical Flows
### Gemini 2.5 Pro vs Flash Comparison
Workflow for complex reasoning tasks:
1. Left pane: Gemini 2.5 Flash + Thinking Budget Off
2. Right pane: Gemini 2.5 Pro + Default settings
3. Submit complex prompt with guidelines
4. Compare:
   - Flash: Fast, general responses
   - Pro: Detailed, precise reasoning with guideline citation

### Imagen Technical Pipeline
#### Text-to-Image Generation:
- Prompt → Imagen model → Image generation
- Safety filtering applied
- SynthID watermark embedded

#### Post-generation Processing:
- Inpaint: Mask areas for regeneration
- Outpaint: Extend image boundaries
- Export with optional upscaling

## Advanced Features
### Grounding Options:
- Google Search: Real-time information retrieval
- Your Data: RAG from custom data sources
- Structured Output: Force specific response formats (JSON)

### Safety Settings:
- Content filtering thresholds
- Harmful content blocking
- Configurable safety levels

## Error Handling
### Deployment Failures:
- Wait 1 minute for permission propagation
- Click "Update app" in Manage web app dialog
- Confirm retry

### API Enablement:
- Automatic enabling of required services
- Wait for service activation

### Response Quality Issues:
- Adjust temperature lower for factual tasks
- Add more examples for complex formatting
- Modify system instructions for better guidance

## Production Considerations
### Security:
- Default: Public unauthenticated access
- Production: Configure IAM and authentication

### Scaling:
- Cloud Run automatic scaling
- Serverless infrastructure

### Monitoring:
- Cloud Run logs and metrics
- Response quality monitoring
- Usage analytics

## Technical Parameters
| Parameter | Purpose | Recommended Values |
|-----------|---------|-------------------|
| Temperature | Controls randomness | 0.1 (factual) - 0.8 (creative) |
| Top-P | Token selection focus | 0.8 (focused) - 1.0 (diverse) |
| Output Token Limit | Response length control | 1024 (short) - 8192 (long) |
| Thinking Budget | Reasoning depth | Auto/Manual (128-8192 tokens) |

## Model Selection
- **Gemini 2.5 Flash**: Fast responses, cost-effective, straightforward tasks
- **Gemini 2.5 Pro**: Complex reasoning, analytical tasks, detailed responses
- **Imagen**: Image generation and editing
- **Chirp**: Text-to-speech synthesis
