# LUFFY Development Repository

&gt; 🚧 **Development Branch** - This is the main development repository for LUFFY (Learning to Reason Under Off‑Policy Guidance)

## About LUFFY

LUFFY is a reinforcement learning framework that bridges the gap between zero-RL and imitation learning by incorporating off-policy reasoning traces into the training process. This repository contains the core implementation and development work.

## 🔧 Development Status

This repository is under active development. Many features are currently being implemented or need refactoring.

## 🚀 Quick Start

⚠️ **Note**: This development version has incomplete implementations. Many features are marked as TODO and need to be completed before production use.

```bash
# Clone the repository
git clone &lt;repository-url&gt;
cd LUFFY

# Install dependencies
pip install -r luffy/requirements.txt

# Note: Some functionality is incomplete - check TODO list below for details
```

## 📁 Repository Structure

```
LUFFY/
├── luffy/                 # Core framework
│   ├── deepscaler/        # Scaling utilities (⚠️ API integration needed)
│   ├── verl/              # RL training components (⚠️ Some features incomplete)
│   └── ...
├── data/                  # Training data and scripts
├── eval_scripts/          # Evaluation utilities
├── exp_scripts/           # Experiment scripts
└── README.md              # This file
```

## ⚠️ Development Notes

- This is a **development version** with incomplete implementations
- Many functions contain TODO markers indicating pending work
- API integrations (OpenAI, Gemini) are currently placeholder implementations
- FSDP and distributed training features need completion


### 🔴 High Priority TODOs

- **API Integration**: OpenAI and Gemini API implementations need completion
- **Reward System**: Parallel processing and validation for reward computation  
- **FSDP Training**: Model loading and distributed training setup
- **Data Processing**: Batch dimension operations and tensor reshaping


### 📝 Complete TODO List

- [ ] **luffy/deepscaler/utils.py:40** - Add logging for API calls and errors
- [ ] **luffy/deepscaler/utils.py:41** - Support batch processing for multiple prompts
- [ ] **luffy/deepscaler/utils.py:42** - Add timeout configuration for API calls
- [ ] **luffy/deepscaler/utils.py:85** - Implement Vertex AI initialization and authentication
- [ ] **luffy/deepscaler/utils.py:86** - Configure safety settings for content generation
- [ ] **luffy/deepscaler/utils.py:87** - Set up GenerativeModel with proper system instructions
- [ ] **luffy/deepscaler/utils.py:88** - Implement retry logic with exponential backoff
- [ ] **luffy/deepscaler/utils.py:89** - Add comprehensive error handling for API access issues
- [ ] **luffy/deepscaler/utils.py:90** - Handle rate limiting and quota management
- [ ] **luffy/deepscaler/utils.py:91** - Implement response validation and text extraction
- [ ] **luffy/deepscaler/utils.py:92** - Add support for different generation configurations
- [ ] **luffy/verl/verl/protocol.py:159** - Optimize memory usage during tensor reshaping
- [ ] **luffy/verl/verl/protocol.py:160** - Add support for different tensor types and shapes
- [ ] **luffy/verl/verl/protocol.py:180** - Optimize tensor view operations for performance
- [ ] **luffy/verl/verl/protocol.py:181** - Add error handling for invalid batch dimensions
- [ ] **luffy/verl/verl/protocol.py:305** - we can actually lift this restriction if needed
- [ ] **luffy/verl/verl/protocol.py:575** - (zhangchi.usc1992) whether to copy

## 🤝 Contributing

1. Pick a TODO item from the list above
2. Implement the functionality
3. Test your implementation
4. Update this README when TODOs are completed