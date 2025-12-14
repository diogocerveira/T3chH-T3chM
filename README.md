# A personified Framework for Machine model Teaching

## Description
The framework is built around a [[Student]]-[[Teacher]]-[[Classroom]] metaphor — a model that is trained and evaluated in a run environment with specific properties.
Each classroom has one single way of teaching (e.g. multi-label) a certain subject matter (i.e. dataset), while allowing for different kinds of models to be evaluated through different tests.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Model Architecture](#model-architecture)
- [Training and Evaluation](#training-and-evaluation)
- [Contributing](#contributing)
- [License](#license)


## Contributing
(tbd)

## License
(tbd)

## Acknowledgments

# User Manual
## Installation
To set up the project environment, clone the repository and install the required packages:

git clone https://github.com/yourusername/surgical-nn.git
cd surgical-nn
pip install -r requirements.txt

## Usage
Create a config file (template available at settings/). Dynamic args not finished.

## Functions
Each function kind has a personified object class associated.

### Data-related
Handled by [[The Virtual Cataloguer]] and [[SampledVideoDataset]].
Direction: Raw Video → Labeled Video Frames [→ Frame Splits] → Batches of Frames

### Teaching-related
Handle by [[Machine Teacher]].
Direction: Batches of Frames → Model Predictions → Performance Scores

### Model-related
Handled by [[Machine  Student]].

### Run-related
Handled by [[Machine Classroom]] and Interface.
From the perspective of the user, the framework follows a three-action structure:
- Train: Train and Export model (as state dicts, with logging);
- Evaluate: Test (generate a prediction bundle) and assess performance;
- Process: Extra manipulation (e.g. preprocessing, feature extraction, and post-processing results with a mode filter).

## Use Requirements
Brain, computer with high-grade GPUs.

# Developer Manual
## Folder Structure
**settings/**: Configuration files for framework-user interaction.
**data/**: Contains local and/or external datasets, samples, labels, and annotations.
**logs/**: Stores run outputs for classrooms and its students. Categorized into Process (extracted feature and post processed results), Train (TensorBoard log events, saved model states, exported predictions) and Eval (results)
**src/**: Houses main scripts: catalogue.py (data-related), machine.py (model-related), teaching.py (teaching-related - training, validation and testing), environment.py (run-related) and learning.py (main script).

## Implementation and Tools
Tools Used: Python 3.10, Visual Studio Code, GitHub
Libraries: PyTorch, TorchVision, Scikit-Learn, Pandas, NumPy, Matplotlib, Seaborn, TensorBoard
Configuration Management: Argparse, YAML

## Features
- Simple to understand
- Easy to use for a surgeon
- Adaptable to a game-like GUI
## Backlog
## Bugs
