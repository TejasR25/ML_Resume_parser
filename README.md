# Resume Parsing and Job Recommendation System

## Aninditaa Chauhan, Govind Sunilkumar, Rashmi Ravindranath and Tejas Raju

This project implements a system to parse resumes, fine-tune a BERT model for job classification, and provide personalized job recommendations. The system uses a combination of PDF text extraction and NLP techniques to process resumes and match them to suitable job descriptions.


## Prerequisites

Ensure you have the following software and libraries installed:

## Prerequisites
Ensure you have the following software and libraries installed:
-Python 3.7+
-PyTorch
-Transformers
-Scikit-learn
-pandas
-pdfplumber
-pytesseract
-Pillow
-PyMuPDF
-tqdm

## System Requirements:
Tesseract OCR installed (apt-get install -y tesseract-ocr)
Google Colab (optional, for GPU usage)

## Steps to Run the Project
Run the Script: Open and run gt_(updated_test).py in a Python environment or Google Colab for best performance.

## Upload Resume: Upload a PDF file containing the resume. 
For example:
Saving Resume_tex_digital.pdf to Resume_tex_digital.pdf
Parsed Resume Output: The script parses and extracts details from the uploaded resume. For example:
yaml

## Parsed Resume:
Education: Masters of Science in Computer Engineering Aug 2023 - Dec 2024
Virginia Tech, Blacksburg CGPA: 4.0
B.Tech in Electronics and Communication Engineering Sep 2017 - May 2021
National Institute of Technology, Karnataka CGPA: 7.35/10
Professional Experience:
- RTL Systems Design Intern, Skyworks Solutions, Austin
- Embedded Hardware Engineer, Bharat Electronics Limited, Bangalore
Projects:
- Designed Hyper Dimensional Computing IC using 6T SRAM
- Designed 12-bit Multiplier logic and layout
Technical Skills:
- System Verilog, Python, C++, ASIC RTL design, FPGA prototyping, Physical Design
- When using Google Colab, mount your Google Drive:


1). Run the Notebook
• Open 906578048_NLI.ipynb using Google Colab

2). Provide a CSV file containing job categories and descriptions. The script uses this data to fine-tune the BERT model.

3). The BERT model is fine-tuned on the job dataset to classify resumes into relevant job categories.

4).  Upload a CSV file containing job descriptions for generating personalized recommendations.

5). Based on the similarity between the parsed resume and job descriptions, the script provides the top 5 recommended jobs. For example:

Top Recommended Jobs:
                      Category                         
0  Industrial Automation Engineer   
1      Robotics Hardware Engineer   
2  Hardware Verification Engineer   
3          Analog Design Engineer   
4   Sensor Integration Specialist   

                                           Resume  
0  Worked on automotive ECU hardware and CAN/LIN ...  
1  Expertise in power electronics design, includi...  
2  Experience in designing and debugging microcon...  
3  Skilled in FPGA prototyping and hardware verif...  
4  Hands-on experience in robotics hardware and s...  

## Saving and Loading Models
The fine-tuned model can be saved using:
torch.save(model.state_dict(), "fine_tuned_bert.pth")

To load the saved model:
model.load_state_dict(torch.load("fine_tuned_bert.pth"))


`````Notes
• Make sure that the dataset paths are correctly set based on your environment (Google Drive).
• Using a GPU is highly recommended.
• YoChange the hyperparameters and also can explore other models like BERT to improve performance.

