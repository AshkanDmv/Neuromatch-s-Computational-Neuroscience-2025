# A Look Back in Error: How Stimulus History and Adaptive Learning Shape Perceptual Decisions

**A Neuromatch Academy 2025 Project**

**Pod:** Playful Vishnu

**Team:** Disconnected Connectionists

**Mentors:** 
* [Gal Vishne](https://neurogal.github.io/)
* [Bryan Daniels](https://search.asu.edu/profile/2752849)

**TAs:**
* [Shirin Taghian](https://www.linkedin.com/in/shirin-taghian/)
* [Safa Mohammadi](https://www.linkedin.com/in/safa-mohammadi-70445b86/)

**Team Members:**
* [Afra Darvishi](https://www.linkedin.com/in/afra-darvishi/)
* Arash Rahimi
* Aylar Shadbakhsh
* Ashkan Damavandi
* [MohammadFazel Abdhaghighi](https://www.linkedin.com/in/mohammadfazel-abdhaghighi/)
* [Mohammad-Reza Salmani Jelodar](https://www.linkedin.com/in/msalmanijelodar/)

---

## 📖 Project Overview

This project models human perceptual decision-making under uncertainty, focusing on how people integrate sensory evidence with prior knowledge.  Using the [Laquitaine & Gardner (2017) dataset](https://doi.org/10.17632/nxkvtrj9ps.1), we analyzed how subjects' estimations of motion direction are influenced by their expectations and recent experiences. Our primary goals were to investigate perceptual biases, analyze the effect of past trials on current performance, and compare competing computational models to explain the observed behavior.

---

## 📊 The Dataset

**Title:** The Laquitaine & Gardner Dataset

**Description:** This dataset includes behavioral data from a motion direction estimation task performed by **12 human subjects** over **83,214 trials**. In the task, participants viewed a random dot kinetogram and reported the perceived direction of motion. The experimenters manipulated both the sensory evidence (motion coherence) and the prior knowledge (by drawing stimuli from different prior distributions) to study how these factors influence perception.

---

## 🧠  Research Questions & Findings

**1. How do past trials affect current motion estimation errors?**
* **Summary:** We investigated if the error in a current trial could be predicted by features from past trials. We trained Polynomial Ridge and Random Forest Regression models to predict the "signed bias" (the angular difference between the subject's estimate and the true stimulus direction) based on prior information.
* **Findings:** Both models showed moderate predictive power, achieving an R² of approximately 0.25. This indicates that while past trial information has some predictive value for current errors, a significant amount of variance remains unexplained by these features alone.

**2. Do subject errors indicate they experience perceptual illusions like the "waterfall" aftereffect or "cardinal biases"?**
* **Summary:** We analyzed trial-by-trial errors for two known perceptual biases:
    * **Waterfall Illusion:** A repulsive bias where a static stimulus appears to move in the opposite direction of a previously viewed motion. We analyzed this by comparing the current estimate's deviation from the stimulus relative to the mean of the previous three trials.
    * **Cardinal Bias:** An attractive bias where estimates are pulled toward cardinal directions.
* **Findings:** Evidence for the waterfall illusion was subject-dependent. For example, **Subject 5 showed evidence of the illusion**, particularly in low coherence and narrow prior conditions, while **Subject 2 showed no clear evidence** of this repulsive effect. We did find evidence for attractive biases, with subjects' estimates being pulled toward the mean of the prior distribution.

**3. What task variables drive subject learning, and which cognitive model best explains it?**
* **Summary:** We modeled subject learning by implementing and comparing two competing cognitive models: an **Online Bayesian Observer** and a **Switching Observer**. The Bayesian model optimally integrates sensory evidence and prior beliefs, while the Switching model uses a heuristic to report either the evidence or the prior on any given trial. We fit both models to the data for all 12 subjects and compared their performance using Mean Squared Error (MSE).
* **Findings:** The **Online Bayesian model provided a better fit** for the majority of subjects, showing a consistently lower MSE. This suggests that, in general, human subjects integrate information in a manner more consistent with Bayesian principles than with a simpler switching heuristic. However, we observed strong individual differences, indicating that perceptual strategies can be highly personalized.

---

## 🙏 Acknowledgements

We would like to thank our Neuromatch Academy mentors, TAs and the organizers for their guidance and support. We also acknowledge Laquitaine and Gardner for making their valuable dataset publicly available.
