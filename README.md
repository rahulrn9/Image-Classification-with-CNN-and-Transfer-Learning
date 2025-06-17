Animal Classifier with CNN & Transfer Learning
📄 Project Overview
Binary image classification (cats vs. dogs) using:

MobileNetV2 backbone (TensorFlow/Keras)

Data augmentation & transfer learning

📂 Structure
bash
Copy
Edit
animal_classifier/
│
├── data/
│   ├── cats/    # PNG samples  
│   └── dogs/    # PNG samples  
│
├── src/
│   ├── data_loader.py   # Sets up ImageDataGenerators  
│   ├── train.py         # Builds & compiles model  
│   ├── evaluate.py      # Plots training curves + metrics  
│   └── utils.py         # Helpers (plots, IO)  
│
├── requirements.txt     # tensorflow, scikit-learn, Pillow  
└── README.md            # (This file excerpt)
⚙️ Prerequisites
Python 3.8+

TensorFlow 2.x

Pillow

🛠️ Installation & Setup
bash
Copy
Edit
git clone https://github.com/rahulrn9/Image-Classification-with-CNN-and-Transfer-Learning.git
cd Image-Classification-with-CNN-and-Transfer-Learning
python -m venv venv
source venv/bin/activate      # or venv\Scripts\activate
pip install -r requirements.txt
🗄️ Data
data/cats/ and data/dogs/: small PNG sets (replace with larger dataset for production)

🔄 Workflow
Load & augment
python src/data_loader.py --data_dir data/ --img_size 128 128 --batch_size 32

Train
python src/train.py --epochs 10 --out models/mobilenetv2_animals.h5

Evaluate
python src/evaluate.py --model models/mobilenetv2_animals.h5 --data_dir data/

📊 Sample Results
Validation Accuracy ~85–90%

Loss/Accuracy curves

