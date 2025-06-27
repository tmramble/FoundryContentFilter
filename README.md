# Exercise: Content Filtering in Azure AI Foundry

**Author:** Taylor Ramble

## Overview

This exercise demonstrates how to use default and custom content filters in Azure AI Foundry to prevent harmful content in generative AI applications.

Content filtering in AI Foundry ensures that AI-generated outputs are safe, ethical, and aligned with legal, business, and user expectations. It blocks harmful, offensive, or non-compliant content, helping maintain brand integrity, regulatory compliance, and a positive user experience. Filtering also supports customization for specific domains, making AI deployment more controlled and responsible.

---

## Steps & Configuration Details

### 1. Deploy a Model in Azure AI Foundry

- Open [Azure AI Foundry](https://ai.azure.com) and sign in.
- Search for `Phi-4` and click **Use this model**.

**Configuration:**
- **Azure AI Foundry Resource:** Enter a valid name  
- **Subscription:** Select your Azure subscription  
- **Resource Group:** Select or create a new one  
- **Region:** Choose from:
  - East US  
  - East US 2  
  - North Central US  
  - South Central US  
  - Sweden Central  
  - West US  
  - West US 3  
- **Deployment Name:** `Phi-4` (default)

---

### 2. Test Default Content Filtering

- Open **Chat Playground** and ensure `Phi-4` is selected.  
- Test the following prompts:

```text
Prompt: What should I do if I cut myself?
→ Expected: Appropriate guidance.
```
## 3. Create and Apply a Custom Content Filter
Navigate to Guardrails + Controls → Content Filters.
Click + Create Content Filter.
Configuration Items:
Filter Name: A valid name.
Input Filter Categories:
Violence: Block Low, Medium, High
Hate: Block Low, Medium, High
Sexual: Block Low, Medium, High
Self-harm: Block Low, Medium, High
Output Filter Categories:
Same settings as input filters.
Deployment: Apply to Phi-4 model.
Click Create Filter.

## 4. 5. Test the Custom Content Filter
Open Chat Playground.
Ensure Phi-4 is selected.
Submit prompts:
What should I do if I cut myself?
The custom filter should block this prompt.

