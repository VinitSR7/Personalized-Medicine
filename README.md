# Personalized-Medicine
Classifying clinically actionable genetic mutations; NIPS-2017 Competition

<h2>  Description</h2>
<p> Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/ </p>
<p> Classify the given genetic variations/mutations based on evidence from text-based clinical literature. </p>

<h3>  Machine Learing Objectives  </h3>
<p> Objective: Predict the probability of each data-point belonging to each of the nine classes.
</p>
 
 
 <h2>  Data</h2>
 <h3>  Data Overview</h3>
 - Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
- We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that  human experts/pathologists use to classify the genetic mutations. 
- Both these data files are have a common column called ID
- <p> 
    Data file's information:
    <ul> 
        <li>
        training_variants (ID , Gene, Variations, Class)
        </li>
        <li>
        training_text (ID, Text)
        </li>
    </ul>
</p>

<h3>  Example Data Point</h3>
<hr>
ID,Gene,Variation,Class<br>
0,FAM58A,Truncating Mutations,1 <br>
1,CBL,W802*,2 <br>
2,CBL,Q249E,2 <br>
...

<h6> training_text</h6>
<hr>
ID,Text <br>
0||Cyclin-dependent kinases (CDKs) regulate a variety of fundamental cellular processes. CDK10 stands out as one of the last orphan CDKs for which no activating cyclin has been identified and no kinase activity revealed. Previous work has shown that CDK10 silencing increases ETS2 (v-ets erythroblastosis virus E26 oncogene homolog 2)-driven activation of the MAPK pathway, which confers tamoxifen resistance to breast cancer cells. The precise mechanisms by which CDK10 modulates ETS2 activity, and more generally the functions of CDK10, remain elusive. Here we demonstrate that CDK10 is a cyclin-dependent kinase by identifying cyclin M as an activating cyclin. Cyclin M, an orphan cyclin, is the product of FAM58A, whose mutations cause STAR syndrome, a human developmental anomaly whose features include toe syndactyly, telecanthus, and anogenital and renal malformations. We show that STAR syndrome-associated cyclin M mutants are unable to interact with CDK10. Cyclin M silencing phenocopies CDK10 silencing in increasing c-Raf and in conferring tamoxifen resistance to breast cancer cells. CDK10/cyclin M phosphorylates ETS2 in vitro, and in cells it positively controls ETS2 degradation by the proteasome. ETS2 protein levels are increased in cells derived from a STAR patient, and this increase is attributable to decreased cyclin M levels. Altogether, our results reveal an additional regulatory mechanism for ETS2, which plays key roles in cancer and development. They also shed light on the molecular mechanisms underlying STAR syndrome.Cyclin-dependent kinases (CDKs) play a pivotal role in the control of a number of fundamental cellular processes (1). The human genome contains 21 genes encoding proteins that can be considered as members of the CDK family owing to their sequence similarity with bona fide CDKs, those known to be activated by cyclins (2). Although discovered almost 20 y ago (3, 4), CDK10 remains one of the two CDKs without an identified cyclin partner. This knowledge gap has largely impeded the exploration of its biological functions. CDK10 can act as a positive cell cycle regulator in some cells (5, 6) or as a tumor suppressor in others (7, 8). CDK10 interacts with the ETS2 (v-ets erythroblastosis virus E26 oncogene homolog 2) transcription factor and inhibits its transcriptional activity through an unknown mechanism (9). CDK10 knockdown derepresses ETS2, which increases the expression of the c-Raf protein kinase, activates the MAPK pathway, and induces resistance of MCF7 cells to tamoxifen (6). ... 


<h3>Type of Machine Learning Problem</h3>
<p>
            There are nine different classes a genetic mutation can be classified into => Multi class classification problem
 
</p>

<h3> Performance Metric</h3>
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment#evaluation

Metric(s): 
* Multi class log-loss 
* Confusion matrix 

### Univarite Analysis done over Each Feature

- Gene
- Variation feature
- Text Feature

<h3> Result </h3>
* Gene feature is a stable feature, since it's it is equally distributed over the dataset.
* Variation Feature is not a stable feature, since only about 10% of the variation feature is present in the test data from train data.
* Text Feature is also a stable feature.

<h3> Data Preparation </h3> 
We will perform 2 types of encoding of the data<br>
 <ul> 
        <li>
        1. One Hot encoding
        </li>
        <li>
        Response Coding
        </li>
    </ul>

<h2> Models used </h2>
* Logistic Regression with class imbalancing
* Logistic Regression without class imbalancing
* K-Nearest Neighbors classifier
* Naive Bayes Classifier
* Linear SVM Classifier
* Random Forest Classifier
* Stacking Classifier
* Majority Voting Classifier (using mlxtend library)

