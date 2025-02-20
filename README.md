 # Image's Invoice Using Gemini 

This is a Streamlit app that demonstrates the usage of Gemini-Pro-Vision model from Google's Generative AI platform to extract available informations from images. This app allows users to upload an image and provide a text prompt, and then generates a response based on the image and text input.


#### 1. Import the necessary libraries
- `google.generativeai` is the library that provides access to the Gemini-Pro-Vision model.
- `PIL` is the Python Imaging Library, which is used to load and process images.
- `textwrap` is used to wrap text to a specified width.
- `pathlib` is used to work with file paths.
- `os` is used to access the environment variables.
- `streamlit` is used to create the Streamlit app.
- `dotenv` is used to load environment variables from a `.env` file.

#### 3. Define the `get_gemini_response` function

```python
def get_gemini_response(input, image, prompt):
    model = genai.GenerativeModel('gemini-pro-vision')
    response = model.generate_content([input, image[0], prompt])
    return response.text
```

The `get_gemini_response` function takes three arguments:

- `input`: The text prompt that the user provides.
- `image`: The image that the user uploads.
- `prompt`: The prompt that is used to generate the response.

The function first creates a `GenerativeModel` object for the Gemini-Pro-Vision model. Then, it calls the `generate_content` method


