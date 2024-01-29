# DNA Encoded Libraries

A DNA-encoded library (DEL), is a recent technology enabling fast screening of large libraries of chemical compounds against a 
protein target (or system) of interest. The basics of a DEL discovery campaign from motivations to experimental output are provided below.

## Motivation
A foundational goal in pharmaceutical sciences is the discovery of chemical matter that can bind or interact with a 
desired protein target. This can be a costly challenge, as it often requires experimentally testing thousands of chemical compounds
to see if they have the desired activity. Multiple methods have been developed to make this process both
faster and cheaper. DEL is one such approach, where a DEL screening campaign aims to discover chemical matter that
interacts with a desired target.

## DEL Screening
Specifically, DEL is a small molecule screening approach for finding compounds that **bind** the target of interest. 
This means that, unlike other screening methods, DEL can only determine if compounds bind a protein and **CANNOT**
determine if the overall function of the target is affected by the compound. Further, unlike other methods used to screen for binding, DEL 
cannot determine actual coefficients of binding (like Kd or Ki), and will only be able to determine how "enriched" a given chemical was at binding over other chemicals that were not enriched (did not show any binding).

The main advantage of the DEL approach lies in its high-throughput, enabling the screening a billions of compounds in a time and cost-effective manner. This process allows for the collection of large volumes of structured data for downstream analysis.

## How DEL Works
DEL can yield massive throughput by taking advantage of DNA and next-generation sequencing. It works by tagging each 
unique compound in library with a unique DNA code. Multiple copies of each compound are made (with the same tag) and included in the library solution. The result is a solution that contain multiple copies of billions of chemicals, all tagged with DNA: a DNA-encoded library. More details about the DEL technology can be found [here](https://en.wikipedia.org/wiki/DNA-encoded_chemical_library).

This DEL solution is used for screening. After the screening step, only the portion of the library that bound to the 
target remains. The DNA of those compounds can then be sequenced with high-throughput sequencing to determine how many copies of a given compound were.
This allows for the collection of 'sequence counts' or 'enrichment values'. While a vast majority of compounds will not be
detected post screening, a fraction will have been found to bind, and have counts/enrichment that range from as low to high. While the
value of the enrichment generally corresponds with how tight of a binder a chemical is, it should be noted that due to noise and other factors,
enrichment levels should not be taken as quantitative measurements of binding strength, like Ki or Kd. For example, if one DEL compound
is twice as enriched as another, it does not mean that the real coefficient of binding is twice as large.

## DEL Compound Makeup
DELs do not contain just any random chemical, but a specific set that follows some general rules. This is because DEL 
takes advantage of something known as combinatorial synthesis. This is an approach where chemical compounds are assembled from small sets of 
chemical fragments (called building blocks or BBs) that can all undergo the same reaction. This allows the generation of large
libraries (billions) of chemicals from relatively small sets (~6,000) of building blocks (BBs).

As an example: Say we have chemical reactions X and Y. We also have three sets of BBs, set A (4,000 compounds), set B (3,000) and set C (2,000). 
Everything in set A and set B can undergo reaction X, thus after one mixes these two sets one gets 12,000,000 compounds. 
Moreover, everything in set B can react with set C via creation Y. Since all of 12 million compounds from the last reaction have a set B in them, that can undergo reaction Y. 
Thus after mixing in set C, we have 12,000,000 * 2,000 = **24,000,000,000** (24 billion) compounds in the library. Each of these
24 billion compounds is then made up of 3 building blocks (each from a different set, sometimes called cycle), and 1 reaction scheme. 

## Disynthons and Monosynthons
Since DELs are made up of 2 or more (generally 3) building blocks assembled in a combinatorial approach, there is a lot
of repetition in the chemical library. Thus, we sometimes break DEL compounds down into subcomponents to better understand the data and chemistry trends.

We call these Disynthons (set of 2 building blocks) or Monosynthons (set of 1 building block). There are 3 mono and 3 disynthons for each DEL (if it used 3 sets/cycles). For example, A234 might be a single BB in the A set of the library example above.
That means 12,000,000 compound have A234. When analyzing the data, one might want to look at how many of the enriched compounds share this "monosynthon". This is even more powerful when looking
at disynthons. Only 2,000 compounds share A234 and B567, thus if one observes that disynthon 60 times in the enriched compound list, one might be more confident that there is one of multiple chemical substructures defined by that disynthon that bind the target. Likewise, one can use this to help clear up noise or find outliers: if a DEL compound has monosythons and disynthons that show up nowhere else
in the enriched list of compounds, then we might suspect this is the result of noise or the presence of an outlier point.

If a library is made of only two sets/cycles then it has only 1 disynthon and 2 monosynthons. 1 set/cycle DEL libraries cannot exist, and 4 set/cycle libraries are rare, and not used in 
by AIRCHECK
