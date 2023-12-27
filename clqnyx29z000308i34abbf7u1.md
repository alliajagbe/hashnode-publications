---
title: "How to Deploy Your ML Model with Gradio"
seoTitle: "How to Deploy Your ML Model with Gradio"
datePublished: Wed Dec 27 2023 16:05:58 GMT+0000 (Coordinated Universal Time)
cuid: clqnyx29z000308i34abbf7u1
slug: how-to-deploy-your-ml-model-with-gradio
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1703671122900/829528da-453f-4937-a55d-93c31d49ca2a.png
tags: artificial-intelligence, deployment, data-science, machine-learning, machine-learning-models

---

A common pitfall for most individuals entering the machine learning and data science fields is concluding their projects solely within a Jupyter Notebook file. However, this should not be the case as machine learning is a powerful field, and sharing your models with others in an interactive manner can be exciting and rewarding. This is where Gradio comes in.

## What is Gradio?

[Gradio](https://www.gradio.app/), an [open-source Python library](https://github.com/gradio-app/gradio) developed by [HuggingFace](https://huggingface.co/), is a user-friendly library that simplifies the deployment process, allowing us to create interfaces for our models with just a few lines of code.

For a demonstration, we'll be using a pre-trained image captioning model from *Salesforce* called BLIP (Bootstrapped Language-Image Pre-training) in just 4 steps.

## Deploying the ML Model with Gradio

The following steps outlined below detail how to deploy an image captioning machine learning model using Gradio.

### Step 1: Setting Up the Environment for the Model

Provided that we do not have the necessary libraries installed, we install them using the following commands via the terminal.

```bash
pip install transformers
pip install gradio
```

Now, we import the required libraries in our Python script.

```python
import warnings 
warnings.filterwarnings("ignore") # optional

from PIL import Image
from transformers import BlipProcessor, BlipForConditionalGeneration
import gradio as gr
```

### Step 2: Loading the Pre-Trained Model

BLIP is a state-of-the-art image captioning model, and I'll be using the HuggingFace Transformers library to load it.

```python
processor = BlipProcessor.from_pretrained("Salesforce/blip-image-captioning-large")
model = BlipForConditionalGeneration.from_pretrained("Salesforce/blip-image-captioning-large")
```

`processor` creates an instance of the BlipProcessor class by loading a pre-trained model called `Salesforce/blip-image-captioning-large`. `processor` is responsible for preprocessing the image before it can be passed to the captioning model.

`model` creates an instance of the BlipForConditionalGeneration class by loading the same pre-trained model `Salesforce/blip-image-captioning-large`. `model` is responsible for generating captions for the input image.

### Step 3: Integrating the Model with Gradio

Now that the model has been loaded, we can now integrate it with Gradio to create an interactive interface where users can upload images and using the model from Salesforce, we generate a descriptive caption for that image.

```python
def caption_image(raw_image):
    raw_image = Image.fromarray(raw_image.astype('uint8'), 'RGB')
    inputs = processor(raw_image, return_tensors="pt")
    out = model.generate(**inputs)
    caption = processor.decode(out[0], skip_special_tokens=True)
    return caption

input_type = gr.Image()
output_type = gr.Textbox()

gr.Interface(fn=caption_image, inputs=input_type, outputs=output_type).launch()
```

In the above code, we define a function `caption_image` that takes `raw_image` as input, we then do the necessary transformation before passing it to the pre-trained model from *Salesforce*. The function returns the generated caption from the model.

Since our input type is an image, we use the `Image` component provided by Gradio. Similarly, for the output, we use the `Textbox` component. `gr.Interface` then wraps the `caption_image` function, while taking the input and output component types to create an interface for the user in their browser. To create a public link, set `share=True` in `launch()`.

### Step 4: Launching the App

The app is now ready and can simply be run the same way we run any Python file.

```bash
python name_of_our_file.py
```

With the above command, the script is executed and Gradio provides a link to the locally hosted app. We can open the link in our browser, and now, we have an interactive interface where we can either upload images, drag and drop images, or take one via webcam, and receive descriptive captions.

The interface should be similar to this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703669944933/41a011ca-ef71-4b06-90ee-44fcc6eb105d.png align="center")

## Conclusion

The app is now ready for public use! Your ML project does not have to end in a jupyter notebook. Go ahead and deploy with Gradio!

Thank you for engaging!