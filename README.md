# ADMET-AI: Advanced ADMET Prediction and Optimization

A Flask-based web application for predicting ADMET (Absorption, Distribution, Metabolism, Excretion, and Toxicity) properties of chemical compounds, with built-in AI-powered optimization capabilities.

## Features

- **ADMET Prediction**:
  - Machine learning models trained on chemical data
  - Rule-based physicochemical property analysis
  - Detailed molecular descriptor calculations
- **AI Optimization**:
  - Ant Colony Optimization (ACO) for molecular improvements
  - Google Gemini integration for AI-driven suggestions
- **Advanced Analytics**:
  - Drug-likeness evaluation (Lipinski, Ghose, Veber rules)
  - Toxicity risk assessment (PAINS filters)
  - Pharmacokinetic property predictions
- **Interactive Features**:
  - Chat interface with Gemini AI
  - Molecular radar visualization
  - Batch processing capabilities

## Installation

### Prerequisites
- Python 3.8+
- pip package manager
- Google Gemini API key

### Setup

1. Clone the repository:
```bash
git clone https://github.com/Gencoders-Team/ADMET.git
cd ADMET
```

2. Create and activate virtual environment:
python -m venv venv
source venv/bin/activate  # Linux/MacOS
venv\Scripts\activate  # Windows

3. Install dependencies:
   pip install -r requirements_final_v2.txt

4. Set up environment variables:
   echo "GEMINI_API_KEY=your_api_key_here" > .env

Configuration
Required Files

    Create adme_training_data.csv with your dataset or use sample data

Environment Variables

    GEMINI_API_KEY: 
    PORT: Server port (default: 5009)

Optimization Algorithms
Ant Colony Optimization (ACO)

    Modifies molecular structure using reaction rules

    Evaluates QED, LogP, and toxicity for fitness

    50 iterations with 20 virtual ants by default

Gemini AI Optimization

    Uses Google's Gemini model for structural suggestions

    Focuses on improving drug-likeness metrics

    Maintains chemical validity through SMILES validation

Troubleshooting

Common Issues:

    Invalid SMILES:

        Verify input using RDKit's MolFromSmiles

        Use the /chat endpoint for SMILES validation help

    Missing Dependencies:

        Ensure all requirements are installed

        Check for CUDA drivers if using GPU acceleration

    API Key Errors:

        Verify .env file contains valid GEMINI_API_KEY

        Ensure no trailing spaces in the key

Logs:

    Check app.log for detailed error information

    Enable debug mode by removing debug=False in app.run()

License

MIT License - See LICENSE for details
Disclaimer

This project is intended for research purposes only. Predictions should be validated with experimental data. The authors are not responsible for any decisions made based on this software.
