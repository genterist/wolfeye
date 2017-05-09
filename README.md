# Project Wolf Eye

**NOTE: THE BELOW STEPS ARE JUST BASIC DEMONSTRATION OF ATTACKING CONCEPTS. FURTHER WORKS WILL BE DONE AND THIS REPO WILL BE UPDATED ACCORDINGLY**

## Step 1: Train the original model and then probe it with some special data (A2)
The below video will demonstrate basic steps on how to train an IBM Watson visual recognition model <br/>
[![](https://i.ytimg.com/vi/NyJgpM4SPlA/hqdefault.jpg?custom=true&w=196&h=110&stc=true&jpg444=true&jpgq=90&sp=68&sigh=z7sZw45N4F4UgkeV0wikLPS7_Pw)](https://www.youtube.com/watch?v=NyJgpM4SPlA)
<br/>
Note the values got input into the spreadsheet on the bottom right. Model was able to identify which picture is "cat", which picture is "lion" with just 10 samples for each training category. However, as the number of samples increases, there is not much improvement. When the number gets to 70 samples for each category, the model even fails to categorize picture named "c3". I plan to do >1000 samples of cat and around 100 samples of lion in the next experiment
<br/>
## Step 2: Pick the best sample to attack the model
The below video will demonstrate the steps <br/>
[![](https://i.ytimg.com/vi/a46BMhjhiaw/hqdefault.jpg?custom=true&w=196&h=110&stc=true&jpg444=true&jpgq=90&sp=68&sigh=Gj0Quzt4_5Xby9uXIESBoKHx-TE)](https://www.youtube.com/watch?v=a46BMhjhiaw)<br/>
The idea is using another model to select among the attack possibilities (A3), which possibility is closest to "cat" and predict the confidence score assigned to that possibility (picture) when classified by the target model.<br/>
Unfortunately that by design, IBM model does not display confidence score lower than 50% and that fails the illustration purpose. I was, however, able to find "jaguar" the best sample to attack the original model (easiest to be misclassified as "cat" if it got fed to the model).
<br/>
