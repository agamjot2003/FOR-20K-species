# FOR-20K-species


High-Accuracy Classification: Achieved a competitive test accuracy of ~78% on the For-20K species dataset, classifying trees across 33 distinct species labels.

ResNet-Based Architecture: Implemented a custom Residual Network (ResNet) architecture with 5 stages, utilizing bottleneck blocks to capture complex morphological features from multi-view inputs.

Adaptive Feature Extraction: Utilized AdaptiveAvgPool2d and Flatten layers to consolidate spatial information, followed by a Dropout layer to mitigate overfitting during training.

Multi-View Processing: Engineered the model to process four unique perspectives—Facade, Nadir, Profile, and Rear—fusing spatial data from multiple angles into a single classification head.

Advanced Augmentation (TrivialAugment): Integrated TrivialAugmentWide, a state-of-the-art automatic augmentation policy that applies various transformations to increase model robustness.

Regularization with Random Erasing: Employed RandErase (Random Erasing) as a regularization technique, which masks random patches of images to force the model to focus on various parts of the tree structure.

Normalized Preprocessing: Applied meticulous data normalization using calculated dataset means and standard deviations, alongside RandomCrop and HorizontalFlip for spatial variety.

Optimization Pipeline: Leveraged a batch size of 64 and a specialized collate function to handle the multi-view image tensors efficiently across 33 species.

## Results
Achieved a final test accuracy of 78% and 2nd position on the Codabench leaderboard for the For-20K Species Competition.
