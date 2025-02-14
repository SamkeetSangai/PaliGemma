# PaliGemma

This repository provides an implementation of the **PaliGemma** multi-modal model, integrating both vision and language processing.

The model is designed for image-conditioned text generation and supports:

- **Vision-Language Fusion**: Combines image embeddings with text inputs for robust multi-modal understanding.
- **Rotary Embeddings**: Improves positional encoding in transformer layers.
- **KV Caching**: Enhances inference efficiency by storing and reusing key-value pairs.
- **Efficient Transformer Architecture**: Uses grouped query attention and efficient memory utilization.

## Model Architecture

PaliGemma extends the transformer architecture by integrating a vision backbone based on **Siglip** for image feature extraction. These extracted features are projected and concatenated with text tokens, which are then processed by the language model.



*Figure: The PaliGemma model architecture combining vision and text processing.*

## Example Input and Output

Below is an example of how PaliGemma processes an image along with a textual prompt to generate a relevant output.

### Image-to-Text Generation

#### **Input**

**Prompt:**

```plaintext
This building is
```

**Image:**


#### **Model Output**

```plaintext
This building is the Taj Mahal, a UNESCO World Heritage site in India known for its stunning white marble architecture and historical significance.
```

Above example demonstrate PaliGemma's ability to understand images and generate contextual response efficiently.

## Credits

- **Google DeepMind**: For advancements in vision-language models.
