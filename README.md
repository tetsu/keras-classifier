# Keras Image Classifier
Classify images by Deep Learning using Keras with TensorFlow backend.

## How to Setup

1. Download Anaconda from [anaconda.com](https://www.anaconda.com/), and install it.
1. Setup new python environment with Anacond-Navigator
1. Open a terminal window, and do following installations
1. Install modules by typing following command in terminal.

    ```
    pip install tensorflow flickrapi pillow sklearn keras Flask
    ```

1. Go to your working folder, and clone this repository by typing following command in terminal.

    ```
    git clone git@github.com:tetsu/animal-classifier.git
    ```

1. Create a [Flickr](https://www.flickr.com/) account, and enter Flickr Key and Secret in `config/env_sample.py`, and rename the file to `env.py`.

    ```python
    FLICKR_KEY = "{your flickr key}"
    FLICKR_SECRET = "{your flickr secret}"
    CLASSES = ["monkey", "boar", "crow"]
    IMAGE_SIZE = 50
    NUMBER_OF_IMAGES = 400
    ```

1. Go to the top folder of this project, and download images of assigned classes by typing following command in terminal.

    ```
    python download.py
    ```

1. Check folders under "images" folder, and remove images that are not proper for learning, such as unclear images, wrong images, images with other animals or breeds, etc.

1. Convert images to NUMPY data to use on Keras by typing following command in terminal.

    ```
    python gen_data.py
    ```

1. Train model, generate trained neural network h5 file, and evaluate the result by typing following command in terminal.

    ```
    python image_cnn.py
    ```

1. Classify an image file by typing following command in terminal.

    ```
    python predict.py {an image file path}
    ```

1. You can also classify an image file on a web page by typing following command in terminal, and check it on [web browser](http://127.0.0.1:5000/).
    ```
    FLASK_APP=index.py flask run
    ```
