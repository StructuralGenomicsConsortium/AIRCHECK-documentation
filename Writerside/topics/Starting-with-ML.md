# Starting with ML

For those new to using chemical fingerprints for machine learning and AI modeling, you might ask yourselves what to do with this type of high-dimensional data. Fortunately, the answer is simple: anything you could do with other numerical representations of data. You can treat this
the same as you would treat convert a grayscale image to a flatten vector of color values for instance. 

There is some uniqueness of DEL chemical fingerprint data that must be accounted for though: chemical fingerprints tend to be sparse (lots of zeros) and can be heavily correlated (in many fingerprints, having a non-zero value in one element requires that another element also be non-zero).

A common practice in the field is to use these as direct inputs into a Random Forest or SVM for instance, combined with feature selection or reduction. An early example of machine learning analysis of DEL data can be found [here](https://pubmed.ncbi.nlm.nih.gov/32525674/) (Preprint available [here](https://arxiv.org/abs/2002.02530)).
