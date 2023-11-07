# First place solution WIDS Datathon 2019
We would like to first thanks WiDS and all the sponsors and Kaggle for providing us with an interesting use case that might have a good inpact for our planet .

We are currently coworkers and just after participating to the Kaggle days in Paris we decided that we should team up one day, this challenge was obviously a good opportunity (never mind if we miss the xbox at the end).

## Solution:

we started with the public kernel https://www.kaggle.com/tcapelle/fastai-starter based on fast.ai , thanks @tcapelle for that one.
we then follow this check list of things to try :
• Stratify the cross validation on the target, eventually also on the score column
• Lower the % of validation, we ended up with a 7 and 11 fold cross validation
• Try different image size , we ended up using 256x256 image size
• Try different kind of pretrained model, SeResnext101 and Senet154 were those that gave the best results. You can used this repo to enrich your fast.ai experience with lot of models : https://github.com/Cadene/pretrained-models.pytorch
• Tune the number of epoc and LR
• Use the default data augmentation and TTA provided by fast.ai
• We finally bagged using the median of the results from all the fold of each models
• We did most of the processing thru kaggle kernel or google colab notebook.
What we have tried but didn't improve :

## data augmentation with SMOTE
- other kind of transformations for the fast.ai transform function
- overtuning the network
- pseudo labelling
the final kernel is still running we will publish it when it's done.

## references:
- https://github.com/Cadene/
- https://www.fast.ai/
- https://arxiv.org/pdf/1812.01187v2.pdf

voila/