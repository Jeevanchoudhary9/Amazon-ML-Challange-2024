# Amazon ML Challenge: Entity Extraction from Product Images

## Problem Statement

In the Amazon ML Challenge, we aim to extract and predict various product details such as weight, volume, voltage, wattage, and dimensions from images of products. The challenge focuses on leveraging machine learning techniques to accurately identify and extract these entity values, which can greatly enhance product information retrieval and improve user experience in online shopping.

### Objectives:
- Develop a robust machine learning model to extract entity values from images.
- Map extracted values to predefined units specified in the challenge guidelines.
- Ensure high accuracy in predictions while handling various formats and representations of unit data.

## Our Approach

To tackle the problem, we adopted the following approach:

1. **Image Text Extraction**:
   - We utilized the [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) framework to perform Optical Character Recognition (OCR) on product images. This allowed us to extract textual information that potentially contains relevant entity values and their associated units.

2. **Data Preprocessing**:
   - The extracted text underwent a preprocessing phase where we cleaned the data to remove any noise or irrelevant characters. This step is crucial for ensuring the accuracy of our predictions.

3. **Entity Value Extraction**:
   - We implemented a series of regular expressions to identify numerical values and their corresponding units from the cleaned text data. This involved creating mappings for various unit representations to standardize the outputs.

4. **Unit Mapping and Conversion**:
   - We constructed a mapping for recognized units to their standard forms. The system was designed to account for variations in unit representations, ensuring that values were accurately interpreted.

5. **Model Training and Evaluation**:
   - We trained our model on the processed dataset and evaluated its performance based on accuracy and precision metrics. This phase included fine-tuning the model parameters to achieve optimal results.

## Lessons Learned

Throughout the development process, we encountered several challenges and wasted time on specific issues:

- **Data Quality Issues**: The extracted text often contained inconsistencies due to varying image quality, leading to difficulties in accurately capturing entity values. Initial attempts to preprocess data without sufficient cleaning resulted in significant delays.
  
- **Regex Complexity**: Creating robust regular expressions for value extraction proved to be more complex than anticipated. Early versions of the regex patterns failed to account for certain edge cases, necessitating multiple iterations to refine them.

- **Unit Mapping Challenges**: Establishing a comprehensive unit mapping took longer than expected, especially in recognizing all possible variations. A lack of initial clarity on accepted unit formats contributed to misalignment in our mapping efforts.

- **Model Training Time**: The model training phase required extensive computational resources and time, particularly as we explored different architectures and hyperparameters. This highlighted the importance of efficient resource management and optimization strategies.

## Conclusion

The Amazon ML Challenge presented an exciting opportunity to apply machine learning techniques to a real-world problem. Through iterative development and continuous learning, we have made significant progress in extracting valuable product details from images. While we faced challenges along the way, these experiences have greatly enhanced our understanding of text extraction and unit mapping in machine learning applications.

## Installation and Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/amazon-ml-challenge.git
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the main script:
   ```bash
   python main.py --input <path_to_images>
   ```

4. The output will be saved in `output.csv` containing the extracted entity values and units.

## Acknowledgments

- [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) for the OCR framework used.
- The organizers of the Amazon ML Challenge for providing this exciting problem to solve.

## Document Author

Jeevan Choudhary
