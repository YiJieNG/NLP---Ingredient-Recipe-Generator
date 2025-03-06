# NLP---Ingredient-Recipe-Generator
## Overview
This project is simply a Sequence-to-Sequence modelling task, mapping ingredients to a recipe using RNN techniques. It consists of 4 custom RNN training models:
- Baseline 1: Sequence-to-sequence RNNBaseline model 1
- Baseline 2: Sequence-to-sequence RNN with attentionBaseline model 2
- Extension 1: Sequence-to-sequence RNN with attention and data-preprocessingExtension model 1
- Extension 2: Sequence-to-sequence RNN with attention, data-preprocessing, pretrained word2vec embedding and advanced RNN technique with reference to the paper of Ximing Lu, Peter West, Rowan Zellers, Ronan Le Bras, Chandra Bhagavatula, Yejin Choi. NeuroLogic Decoding: (Un)supervised Neural Text Generation with Predicate Logic Constraints. In Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics

## Challenges
This project showcases a self-built sequence-to-sequence RNN model, emphasizing technique comparison rather than perfect performance. The evaluation faced challenges due to limited resources in hardware, time, data quality, and completeness. Consequently, the primary goal was to compare methodologies, not to generate an ideal recipe from the provided ingredients.

## Data Preprocessing
For every model, I have removed any data having no value (either ingredients or recipe or both), then convert the cell value into string.

### For extension 1 and 2 model with data preprocessing:

#### 1. For Ingredients:
- Lower down every character and transform them from Unicode to ascii.
- Substitute the stopwords with space.
- Remove character other than a to z and space notation such as \t
- Separate the left valid ingredients (using \t).
- Remove the extra space.
- Make the repeated ingredients to a unique ingredient to avoid repeated ingredients
- Concatenate the unique ingredients into a long string.

### For extension 1 and 2 model with data preprocessing:

#### 2. For Recipe:
- The reason why ingredients have extra preprocessing step compared to recipe is because recipe is considered as ground truth label, and the expected output of model should be a valid and complete sentence of a recipe. However, we only need a certain information for ingredient thus more preprocessing step is introduced for ingredients compared to recipe.

## Evaluation
Find out more about the details and result at: https://www.ngyijie.com/projects/ingreRecipeGen 
