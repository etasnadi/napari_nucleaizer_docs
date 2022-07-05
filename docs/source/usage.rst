Usage
===============

Napari plugin
-------------

Open the plugin:

1. Start napari by calling `napari`.
2. Then, activate the plugin in the `Plugins` menu.

The GUI provides a tabbed interface. Click on the **New task...** button. It offers several tasks:

- **Prediction**: it creates a prediction tab. You can predict a single image loaded into the Napari stage.

- **New project...**: choose this if you want to train a nucleAIzer model. A file dialog will be opened to select the working directory.

- **Open project..**: choose this if you wish to open a previously created project. A dialog will open to select the project's working directory.

Prediction:

1. After adding a prediction tab you can predict single images or you can run batch prediction.
  
  - To predict a single image, load it into the stage first. Make sure that the correct layer is selected.
  
  - To predict multiple images, you have to first click on the **Batch prediction...** button. Select the input directory containing your images and the output directory. The predicted labelled masks by the model will be put into the output directory in 16-bit TIFF format.
  
  - After selecting the input and output directory, the images will be listed. If you click on an image, the image will be loaded into the **Quick view**. If a segmentation is available to the selected image in the output folder, then the segmentation will also outlined in the **Quick view**. If you double click on an image the image (and its seggmentation if available) will be loaded into the napari stage as separate layers. The images already having a segmentation marked with bold text. Using the checkboxes you can select which images you wish to predict.  You can also select all imagaes based on their status: **prediction exists** / **prediction does not exist**.

2. Click on the **Browse for models...** button and select the model you want to use for segmenting your image(s).

3. Most of the models are trained on resaceled images depending on the median size of the objects. You can specify the "Expected cell size" (in pixels) of your images. Then, your images will be rescaled accordingly to match the scale of the images the selected model was trained on. If you do not specify the cell size, then a default size will be used.

4. Click on the **Predict current image** or **Batch predict selected** to predict your image(s).

.. _usage: