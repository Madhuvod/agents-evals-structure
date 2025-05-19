# Agents-Evals Repository Structure

This document provides a comprehensive overview of the `agents-evals` repository owned by Madhuvod. The repository is designed for agent evaluation frameworks and results, with a primary focus on audio processing and evaluation.

## Repository Overview

The repository is organized into the following main directories:
- `/src`: Contains the source code for the library
- `/tests`: Contains test files for the codebase

### Root Directory Files

- **README.md**: Repository documentation and usage instructions
- **requirements.txt**: Dependency information (librosa, soundfile, numpy)

## Detailed Directory Structure

### /src Directory

The source code directory contains the core functionality of the library:

#### 1. audio_processing.py
- Main file for audio processing functionality
- Contains functions for splitting audio files into segments
- Handles VBR (Variable Bit Rate) audio files correctly
- Example usage is provided in the README

#### 2. /src/cli Directory
- Contains command-line interface tools
- **__init__.py**: Package initialization file
- **audio_eval_cli.py**: CLI tool for audio evaluation tasks

#### 3. /src/data Directory
- Data handling and loading functionality
- **__init__.py**: Package initialization with data utilities
- **audio_dataset_loader.py**: Functions for loading and processing audio datasets

#### 4. /src/evaluators Directory
- Contains evaluation frameworks and utilities
- **audio_evaluator.py**: Framework for evaluating audio processing tasks

### /tests Directory

- **test_audio_splitting.py**: Tests for the audio splitting functionality

## Key Features

Based on the repository structure and README:

1. **Audio Processing**
   - Splits audio files into 10-minute segments
   - Handles Variable Bit Rate (VBR) audio files
   - Frame-based processing for accurate audio handling

2. **Evaluation Framework**
   - Tools for evaluating agent performance on audio tasks
   - CLI interfaces for easy testing and evaluation

3. **Dataset Management**
   - Utilities for loading and processing audio datasets
   - Standardized interfaces for working with different audio formats

## Installation & Usage

### Installation
```bash
pip install -r requirements.txt
```

### Basic Usage
```python
from src.audio_processing import split_audio_file

output_files = split_audio_file(
    input_file="audio.mp3",
    output_dir="output_directory"
)
```

### CLI Usage
The repository provides command-line tools for evaluation:
```bash
python -m src.cli.audio_eval_cli [options]
```

## Dependencies

The project relies on the following Python libraries:
- librosa (>=0.10.1): Audio analysis library
- soundfile (>=0.12.1): Audio file reading/writing
- numpy (>=1.24.0): Numerical processing

---

This documentation provides a clear overview of the repository structure and its main components.