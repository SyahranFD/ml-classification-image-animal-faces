# Animal Faces Image Classification Project

This project focuses on classifying images of animal faces using a dataset sourced from Kaggle. This project also made for Second Submission in Dicoding Belajar Pengembangan Machine Learning course

## Dataset

You can find the dataset at the following link: [Animal Faces Dataset](https://www.kaggle.com/datasets/andrewmvd/animal-faces)

## Credits

The dataset is provided by Andrew Mvd on Kaggle. Full credit for the dataset goes to the original creator.

## Steps to Use the Inference Code

1. **Install Docker**

    Open your terminal, Command Prompt, or PowerShell and run the following command to pull the TensorFlow Serving Docker image:
    ```sh
    docker pull tensorflow/serving
    ```

2. **Run the Docker Container**

    Execute the following command to start the Docker container:
    ```sh
    docker run -it -v YOUR_PATH\saved_model:/models -p 8501:8501 --entrypoint /bin/bash tensorflow/serving
    ```

3. **Start the TensorFlow Model Server**

    Inside the Docker container, run:
    ```sh
    tensorflow_model_server --rest_api_port=8501 --model_name=animal_faces_model --model_base_path=/models/animal_faces_model/
    ```

Replace `YOUR_PATH` with the actual path to your saved model.
