## Checkpoint 1 Feedback:
**Module 0 (EDA) + Module 1 (Clustering):**
-	[ ] Fix the textual explanation issue in Preprocessing
-	[x?] Incorporate richer experiments
    - We expanded the hypothesis [is this enough to cover the action items?]
-	[ ] Go beyond method comparison and develop deeper, insight-driven analysis

## Checkpoint 2 Feedback:
**Module 2 (Graph mining):**
-	[x] Justify k and σ in graph construction with a brief sensitivity check
    - Added section to justify both (ended up selecting a different k)
-	[x] Add graph diagnostics
    - Added just before the graph plot (the graph diagnotics provides better insight, the plot is totally overplottet)
-	[ ] Run Node2Vec with at least 2–3 different settings and compare.
-	[ ] Quantify cross-method agreement between Louvain, Spectral, and DBSCAN partitions.
-	[ ] Try to explore some more interesting findings 
    - **understanding**: do sub-experiment [similar to those in Module 4] such that the insight cannot be derived with simple EDA
        - **response to**: "Surpriseness: Not really. The discovered regimes (workingday × season × weather) are already visible from the correlation heatmap. The graph view confirms but doesn't reveal anything that the vector view couldn't. Consider one analysis the vector view can't easily do could be more interesting."

## Final Project 3:
**Module 4 (Graph mining):**


## Additional Points:
### 1. Feedback for Dataset and Task Selection
- Should the task description + hypothesis perhaps be better aligned with findings not directly observeable in the EDA (heatmatp, etc.)? e.g., H1 only applies to graphs - then we cannot really use for other than Module 3....

### 2. Feedback for Checkpoint 1: Clustering
- add a conclusion + more methods
- 3rd experiment + conclusion is missing?

### 3. Feedback for Checkpoint 2 - Graph mining
- add quantitative cross-method comparison: Compute ARI / NMI between the three partitions to support the claim that "all three methods found similar regimes".



## All checkpoint feedback

### Feedback for Dataset and Task Selection
#### Overall Feedback
The dataset choice is appropriate and offers rich possibilities for analysis.

I think five different tasks may be somewhat too ambitious at this stage. It might be more effective to select one or two of them and develop those in greater depth. 

I think another issue is that somewhat abrupt from the raw dataset to the clustering tasks. An important question is how you intend to preprocess and transform the original data in order to make it suitable for clustering. Providing more details about data preparation and feature construction would make your plan clearer.

### Feedback for Checkpoint 1: Clustering
#### 1. Problem & Dataset
“Apply clustering to discover structure in bike-sharing demand patterns” is too broad. A good project should have a more specific and clearly defined objective, along with some concrete hypotheses.
#### 2. Preprocessing & Data Understanding
The data analysis lacks sufficient textual explanation. You need to clearly state what insights are obtained from the analysis, rather than simply presenting the results.
#### 3. Analysis Quality (Module 1)
You do not provide any conclusions, which is the main issue. I cannot understand what problem you are analyzing or what the clustering results actually mean. No meaningful insights are drawn from the data. The analysis should go beyond merely comparing different methods and be developed in greater depth.
The hyperparameter discussion is quite good and detailed, but having only two methods may be not very sufficient. You could consider adding one or more baselines to strengthen your conclusions.
#### 4. Action Items (must address in the final report)
- [ ] Fix the textual explanation issue in Preprocessing
- [ ] Incorporate richer experiments
- [ ] Go beyond method comparison and develop deeper, insight-driven analysis

### Feedback for Checkpoint 2 - Graph mining
#### Transition to Graph Representation
Clean motivation and a good separation. k = 10 in the kNN graph and σ = mean(distances) in the Gaussian kernel are stated but not justified: a brief sensitivity check would help.

#### Preprocessing & Graph Construction
Some graph diagnostics are reported (nodes, edges, components, average degree, weight range) — good. Could explore: degree distribution plot and clustering coefficient.

#### Analysis Quality (Graph Methods)
- Soundness: Three complementary lenses is a strong and clear design. Hypothesises are good.
- Depth:
    - Node2Vec is run with a single hyperparameter setting (p=1.0, q=1.0, dim=16). Could explore more hyperparameter settings.
    - The three methods have no quantitative cross-method comparison. Compute ARI / NMI between the three partitions to support the claim that "all three methods found similar regimes".
- Surpriseness: Not really. The discovered regimes (workingday × season × weather) are already visible from the correlation heatmap. The graph view confirms but doesn't reveal anything that the vector view couldn't. Consider one analysis the vector view can't easily do could be more interesting.

#### Readiness for Final Submission
Solid foundation, well-organized, hypothesis tracking is clear. It could be better if there is some findings are more surprising.

#### Action Items
- [ ] Justify k and σ in graph construction with a brief sensitivity check.
- [ ] Add graph diagnostics.
- [ ] Run Node2Vec with at least 2–3 different settings and compare.
- [ ] Quantify cross-method agreement between Louvain, Spectral, and DBSCAN partitions.
- [ ] Try to explore some more interesting findings