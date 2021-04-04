NOTE :
The values in the Excel sheet were for my run. As such due to Monte-Carlo
averaging over all the iterations, change in values from run to run should
be extremely miniscule


Comparisons based on the Excel Sheet Values

As can be seen, we did get, Supervised > Semi-Supervised > Unsupervised

For our entire dataset, Supervised performs the best. Then Semi-Supervised
and finally Unsupervised (going by, majorly, the test errors)

A few additional comparisons :

Between Unsupervised KMeans on Raw and Normalized dataset, the results with
the Normalized dataset were much better

Additionally in Unsupervised Learning, between KMeans and Spectral Clustering,
KMeans performed better than Spectral Clustering (if dataset is Normalized)

KMeans here worked with raw data as well, however Spectral Clustering with raw
data gave rather weird results, as a result of which, Spectral Clustering was
performed only for Normalized dataset.

The results of Supervised and Semi-Supervised learning were quite close, as
can be seen. The test scores of Supervised, overall, are better, while the train
scores of Semi-Supervised seem to be better. Obviously the relevant scores are
the test scores in order to compare two learning methods. Thus Supervised wins
over Semi-Supervised by a very small margin, as Supervised has a smaller test
error than Semi-Supervised learning

Additionally, one major issue with Unsupervised learning is the Recall, both
for Train and Test, for all Unsupervised Learning techniques.

Recall is around 60-70 % (train and test) (all Unsupervised Methods)

This symbolizes that for Unsupervised Learning, quite a few members of the
positive class have been incorrectly classified in the negative class. Thus
Positive class was Malignant and Negative class was benign. Thus if a patient
who is Malignant is incorrectly told he is Benign, this creates a pretty relevant
problem.

Thus for Unsupervised Classifiers, Recall is an issue, and for this dataset
it is relevant that recall be as high as possible as diagnosing incorrectly
a Malignant cancer as Benign cancer can lead to pretty major issues and is
pretty significant (Recall relevant for Medical datasets)

Additionally for Unsupervised methods, both the Train and Test precision is 
excruciatingly high (95-99%). Thus if the Unsupervised classifier says that
someone has Malignant Cancer, we can trust the classifiers decision directly, due
to such a high precision.

Precision and Recall is pretty high (>90%)(both) for Supervised and Semi-Supervised
learning techniques


Thus


Supervised > Semi-Supervised > Unsupervised (KMeans)(Normalized) > Unsupervised
(Spectral Clustering)(Normalized) > Unsupervised (KMeans)(Raw)

This above result obtained corresponds with what we did expect for 
Supervised, Semi-Supervised and Unsupervised learning

Thus, use Supervised if all labels available
If some are and some aren't use Semi-Supervised
Finally, if no label available use Unsupervised, however, with unsupervised
one has to be wary about the Recall issues. Precision for Unsupervised, however,
rather good.