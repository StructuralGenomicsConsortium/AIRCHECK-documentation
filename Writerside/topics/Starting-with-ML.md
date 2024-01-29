# Starting with ML

For those new to using chemical fingerprints for machine learning, there is a question of what to do with them. 
Luckily, the answer is simple: anything you could do with other numerical representations of data. You can treat this
not different from converting a grayscale image to a flatten vector of color values. 

There is some uniqueness to account for: chemical fingerprints tend to be sparse (lots of zeros) and can be heavily 
correlated (in many fingerprints, having a non-zero value in one element requires that another element also be non-zero).

Common place in the field is to use these as direct inputs into a Random Forest or SVM. Feature selection or reduction is
also common place. 