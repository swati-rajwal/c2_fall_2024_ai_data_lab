<h1 align="center">The Carter Center for AI.DataLab</a></h1>
<h5 align="center"> If you like our project, please give us a star ⭐ on GitHub for the latest update.</h5>
<h5 align="center">

<p align="center">
  <img src="output/Picture1.png" width="45%" alt="Image 1">
  <img src="output/A_follower_distributions.png" width="45.9999%" alt="Image 2">
</p>
<p align="center"><b>Figure 1: (a) News outlets considered in this study; (b) Number of followers of various news outlets across multiple social media.</b></p>

# 👩‍💻Human Annotations and Agreements
To make it uniform, an annotation guideline was first prepared, and all human annotators followed it. You can read it [here](https://github.com/swati-rajwal/c2_fall_2024_ai_data_lab/blob/main/docs/Annotator%20Guidelines%20for%20Labeling%20Political%20Tweets%20and%20Articles.pdf).
<p align="center">
  <img src="output/D_iaa.png" width="651" alt="agreement level across annotating columns">
</p>
<p align="center"><b>Figure 2: Agreement level across annotating columns.</b></p>

# 🎯Training RoBERTa
<p align="center">
  <img src="output/B_roberta_results.svg" width="651" alt="Experimental Task Design">
</p>
<p align="center"><b>Figure 3: RoBERTa results on gold standard for tweets (blue) and extracted articles (yellow).</b></p>

## Training Parameters

- **output_dir**: `./results/post_body` - Directory to save the model and checkpoints.
- **eval_strategy**: `epoch` - Evaluates the model at the end of each epoch.
- **learning_rate**: `1e-5` - Learning rate for the optimizer.
- **per_device_train_batch_size**: `16` - Batch size per device (e.g., GPU) for training.
- **num_train_epochs**: `15` - Total number of training epochs.
- **weight_decay**: `0.01` - Weight decay to prevent overfitting.
- **save_strategy**: `epoch` - Saves checkpoints at the end of each epoch.
- **logging_dir**: `./logs/post_body` - Directory for logs.
- **logging_steps**: `10` - Logs every 10 steps during training.
- **save_total_limit**: `1` - Retains only the most recent checkpoint.
- **load_best_model_at_end**: `True` - Loads the best model at the end of training.

# Results
<p align="center">
  <img src="output/C_Pro_anti_stances.png" width="651" alt="Experimental Task Design">
</p>
<p align="center"><b>Figure 4: Top 10 Outlets by Pro- and Anti- Stance (Log Scale).</b></p>
