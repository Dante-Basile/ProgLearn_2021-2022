# Decision Forests for Computer Vision and Medical Image Analysis [Textbook](https://link.springer.com/book/10.1007/978-1-4471-4929-3) - Notes

## Ch 3 Intro: The Abstract Forest Model

### Some machine learing categories with examples:
- **Classification** task: recognizing type of a scene captured in a photo, desired output is a discrete, categorical label
- **Regression** problem: predicting price of a house as a function of its distance from a good school, output is a *continuous variable*
- **Density** function: dtecting abnormalities in a medical scan can be achieved by evaluating the image under a probability *density* function learned from scans of healthy indivs
- **Manifold learning**: correlation size + shape of some key brain structions in images with patient's age + health can be cast as this 
- **Semi-supervised** problem: interactive image segmentation, user's brush strokes define labeled data and the rest of image pixels provide *already available* unlabled data
- **Active learning** problem: learning gen rule for detecting tumors in images using min amount of manual annotations

- Decision forests popularity rise due to recent success in *classification* tasks
- Decision trees higher accuracy on prev unseen data, *generalization*, achieved by ensembles of slightly different trees

### General Tree Structure
![image](https://user-images.githubusercontent.com/89429238/132411238-6e585224-4d6c-44ce-ae24-8d75c4c52137.png)
- In a decision tree, each node is associated with one question (ie. is the top portion of the picture blue?)

### A decision tree
![image](https://user-images.githubusercontent.com/89429238/132412270-b234179c-0e9e-43d8-8504-a4abac4ef1db.png)
- The image is injected at the root node, and a test is applied to it 

### Key to good functioning of a decision tree is to establish:
1. Tests associated with each internal node
2. Decision-making predictors associated with each leaf

- Decision tree can be thought of as splitting complex problems into a set of simpler ones: **hierarchical piece-wise** model 

- **Split function, test function, weak learner** are used interchangeably in this book 

### Test function at a split node j as a function with binary output:
![image](https://user-images.githubusercontent.com/89429238/132415312-d3711a36-0146-4138-8194-fa4a4c25e601.png)

### Training points and sets
- **Training Point**: data point for which the attriibutes we are seeking for may be known and used to computer tree params
- **Training Set**: ie. set of photos associated with "indoor" or "outdoor" labels. Denoted S0, is a collection of different training data points
![image](https://user-images.githubusercontent.com/89429238/132419183-b1c0ac08-9cc4-4c79-bd2e-c5289896c109.png)

