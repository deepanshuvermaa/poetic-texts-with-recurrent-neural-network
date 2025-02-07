Shakespeare Text Generator

This project is a text generation model trained on Shakespeare's works. It uses a Recurrent Neural Network (RNN) with LSTM layers to generate text based on a given seed. The model is built using TensorFlow and Keras.

Installation

1-Clone this repository:

git clone https://github.com/your-username/shakespeare-text-generator.git
2- Navigate to the project directory:

cd shakespeare-text-generator
3- Create a virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
4- Install the required packages:

pip install -r requirements.txt

Usage

1- Download the pre-trained model (text_generator.model) or train your own by uncommenting the data preprocessing and training code.

2- Run the main.py script to generate text with different temperatures:

python main.py
3- The output will include generated text with different temperature values (0.2, 0.4, 0.6, 0.8, 1.0), showcasing how temperature affects the randomness of predictions.

How It Works

1- Data Preprocessing

The model uses text from Shakespeare's works. The text is processed into sequences of 40 characters, with a step size of 3. Each sequence is mapped to its corresponding next character for training.

2- Model Architecture

The model consists of a single LSTM layer with 128 units, followed by a dense layer with a softmax activation function.

3Text Generation
The generate_text function generates new text based on a random seed. It uses a sampling function to introduce randomness based on a temperature value:

->Low temperature (e.g., 0.2): More predictable, repetitive text. ->High temperature (e.g., 1.0): Creative but can produce incoherent text.

Examples

Here are some generated samples with different temperatures:

->Temperature: 0.2 i have no reason to love him, nor for any man. i will not say what i think. i will not say

->Temperature: 0.8 as a ship may bear a bear a great gentleman, when i was born to the sword in this tale!

->Temperature: 1.0 for thy name will see thy knights. let us see. away, but that it is for me or tarry not!


![poetry generation](https://github.com/user-attachments/assets/a83b5ec3-4658-472f-84e3-65e29f8440d2)
![poetry generation_output](https://github.com/user-attachments/assets/d4f98d11-eccb-42d1-8193-311bc6f88bd5)
![poetry generation2](https://github.com/user-attachments/assets/e868bd62-b95a-4106-be21-35db27ec6210)
![poetry generation3](https://github.com/user-attachments/assets/d3bac540-eb77-4a0d-a1c6-4dff64738970)

License
This project is licensed under the MIT License. Feel free to modify and use it as you wish.
