# NLP-Welfare-Scheme-Poster-Generator
## Introduction
The primary objective of this assignment was to leverage Large Language Models (LLMs) and other advanced NLP techniques to enhance the interpretability and accessibility of welfare scheme documents through automated summarization and visualization. Our project entailed generating concise and informative write-ups for each scheme, developing effective image prompts, and creating relevant visual representations of the schemes using DALL-E 3. By implementing various iterations and approaches, we aimed to improve consistency, readability, and clarity across textual and visual outputs. Additionally, we evaluated the effectiveness of different transformer models (e.g., T5 and Pegasus) to summarize welfare scheme content accurately.<br><br>

## Implementation
### Step 1: Information Extraction (same as before)
The first step involves processing welfare scheme documents to extract critical details. These documents typically contain information about the scheme’s goals, target audience, location, and other specific elements like beneficiaries, resources, and timelines.
Techniques are applied to extract key entities such as names of people, organizations, locations, and dates, as well as important phrases that describe the scheme’s objectives. For example, extracting "education for girls in rural areas" would lead to the creation of a more targeted visual representation.<br>
### Step 2: Image Prompt Generation (same as before)
After extracting the relevant information, the next step is to convert this data into descriptive image prompts. These prompts are designed with enough detail to guide text-to-image model (dall-e-3) in generating appropriate visuals. The same prompt as submission-1 was used.<br>
### Step 2.5: Generating Character Descriptions and Art Style (introduced later)
Before generating the images, we introduce an important step: generating detailed character descriptions and specifying the art style for the welfare scheme visuals. This step ensures that the characters are represented consistently and in line with the intended aesthetic for the posters.<br>
In this step, the LLM is tasked with generating descriptions for 2-3 main characters, along with the art style to be used in the images. The descriptions focus on the outward appearance of the characters, ensuring they are clearly defined in terms of their physical features, without specifying the background or facial expressions. The art style is also specified in broad terms, such as realistic, manga, or cartoon, based on the nature of the scheme.<br>
 These generated descriptions and art style details are appended to the image generation prompts, providing clear guidance for the text-to-image models. This helps maintain consistency across character representations while leaving the background and facial expressions to be determined by the context and scene later in the process.<br>
### Step 3: Initial Image Generation (same as before)
The structured prompts are then inputted into a text-to-image generation model (dall-e-3). This model generates an initial set of images based on the provided prompts. During this stage, several parameters are crucial:<br>
● Style Consistency: Ensuring the generated images maintain a consistent artistic style.<br>
● Entity Representation: Accurately portraying key entities mentioned in the prompt (e.g.,people, locations, resources).<br>
These generated images are stored for evaluation in subsequent steps.<br>
### Step 4: Generating IBQ and PVQ
Along with generating images, prompts are structured to facilitate efficient evaluation using Image based Questions (IBQ) and Prompt Verification Questions (PVQ):<br>
1. Prompt Verification Questions (PVQ):<br>
PVQs are designed to verify whether the generated image accurately matches the description provided in the prompt. These questions focus on confirming whether key elements, such as characters, actions, objects, and settings mentioned in the prompt, are represented correctly in the image. For instance, a PVQ might ask:<br>
○ "Does the image accurately depict the rural setting mentioned in the prompt?"<br>
○ "Are the key figures or objects from the prompt, such as a classroom or children, visible and correctly represented?"<br>
The goal is to ensure the alignment of the image with the intent of the prompt and to check if the generated image includes all the necessary components.<br>
2. Image-Based Questions (IBQ):
IBQs encourage a deeper, more detailed observation of the image. These questions focus on aspects that may not have been explicitly stated in the prompt but are important for understanding the image in its entirety. For example, IBQs could ask about:<br>
○ "What is the significance of the background elements in the image?"<br>
○ "Can you identify any cultural or contextual details that add meaning to the scene?"<br>
○ "How are the characters’ clothing or posture reflecting the actions or environment?"<br>
These questions are meant to help assess the subtle details, emotional tone, and narrative conveyed through the visual content, going beyond the explicit instructions in the prompt. <br>
### Step 5: Evaluation of Generated Images
Once the initial images are generated, they are evaluated based on their alignment with the original prompt. The evaluation process includes several key metrics:<br>
● Relevance: How accurately the image represents the extracted information from the prompt.<br>
● Coherence: The logical flow and harmony within the image, ensuring all elements work together effectively.<br>
● Text Legibility: Ensuring that any textual content in the image is clear and readable.<br>
Gemini-flash-002 was provided with the generated image and asked to answer both Prompt Verification Questions (PVQ) and Image-Based Questions (IBQ). These questions were designed to:<br>
● Verify whether the key elements mentioned in the prompt, such as characters, actions, objects, and settings, are accurately reflected in the image (PVQs).<br>
● Encourage a detailed analysis of the visual elements in the image, such as specific objects, attire, and background elements that may not be explicitly mentioned in the prompt (IBQs).<br>
This evaluation process helps ensure that the generated image aligns well with the intended vision, highlighting areas of strength and areas for improvement in the image quality and accuracy.<br>
### Step 6: Iterative Refinement
Based on the answers from Prompt Verification Questions (PVQs) and Image-Based Questions (IBQs), the original prompt is refined to better align with the desired outcome. Key insights are used to identify and address issues such as:<br>
● Inconsistencies in character representation: Adjusting details like appearance or role if they do not match the image.<br>
● Missing details: Adding specific elements (e.g., setting or actions) that were overlooked.<br>
● Art style misalignment: Clarifying or adjusting the style description if it doesn't match the generated image.<br>
These changes ensure the prompt more accurately reflects the intended characters, setting, and style, leading to better-aligned image generation in subsequent iterations.<br>

## General Architecture:
![NLP-block diagram](https://github.com/user-attachments/assets/056d9ea8-f19b-446d-b4cb-67afc8e90c7b)

## Conclusions:
Our project successfully applied the principles from GenAssist: Making Image Generation Accessible to develop a robust system for generating culturally relevant, coherent, and clear visual content for welfare schemes in India. By addressing challenges specific to this context, such as cultural sensitivity, text clarity in Indian languages, and ensuring consistency in character and art style, we were able to improve upon existing systems in generating visuals that effectively communicate welfare scheme information.<br>
Through an iterative refinement process involving detailed prompt generation, prompt verification, and visual quality assessments, we were able to significantly enhance the quality and relevance of the generated images. By leveraging advanced models like DALL-E-3, GPT-4o, and Gemini-flash-002, we ensured that each iteration brought us closer to the desired outcomes, ultimately achieving a high level of accuracy in terms of visual coherence, entity consistency, and alignment with the original prompt.<br>
The automation pipeline we developed further ensures that this process can be scaled efficiently, making it easier to generate a large volume of customized visuals for various welfare schemes. This will help bridge the communication gap in underserved communities, ensuring that welfare schemes are more accessible and engaging to the target audience.<br>
Despite challenges in text legibility and occasional inconsistencies in art style, our project demonstrates the potential of combining advanced AI models with iterative feedback loops to refine image generation for specific contexts, and at reasonable costs (~₹80 per scheme).<br>

## Credits
Dhruv Shrimali - https://github.com/DhruvShrimali<br>
Parth Sudan - https://github.com/twosegfaults<br>



