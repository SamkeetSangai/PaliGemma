# PaliGemma

This repository provides an implementation of the **PaliGemma** multi-modal model, integrating both vision and language processing.

The model is designed for image-conditioned text generation and supports:

- **Vision-Language Fusion**: Combines image embeddings with text inputs for robust multi-modal understanding.
- **Rotary Embeddings**: Improves positional encoding in transformer layers.
- **KV Caching**: Enhances inference efficiency by storing and reusing key-value pairs.
- **Grouped Query Attention**: Uses grouped query attention and efficient memory utilization.

## Model Architecture

PaliGemma extends the transformer architecture by integrating a vision backbone based on **Siglip** for image feature extraction. These extracted features are projected and concatenated with text tokens, which are then processed by the language model.

![image](https://github.com/user-attachments/assets/cc907773-c34f-49ce-80cc-3714679c3678)

*Figure: The PaliGemma model architecture combining vision and text processing. Image credit: [Hugging Face](https://huggingface.co/blog/paligemma).*

## Example Input and Output

Below is an example of how PaliGemma processes an image along with a textual prompt to generate a relevant output.

### Image-to-Text Generation

#### **Input**

**Prompt:**

```plaintext
Name of this building is 
```

#### **Model Output**

```plaintext
Name of this building is Taj Mahal
```

Above example demonstrate PaliGemma's ability to understand images and generate contextual response efficiently.

## Credits

- **Google DeepMind**: For developing the original PaliGemma model and providing the pre-trained weights.
- **Umar Jamil**: For architecture code contributions.
