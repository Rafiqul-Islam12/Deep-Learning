# ***Neuron vs Perceptron***
  
***`Perceptron` এবং `Biological Neuron`-এর মধ্যে একটি গভীর সম্পর্ক রয়েছে কারণ perceptron আসলে মানুষের nervous system থেকে অনুপ্রাণিত (inspired)।    
তবে এটি মনে রাখা জরুরি যে perceptron নিউরনের একটি "weakly inspired" রূপ মাত্র, এটি নিউরনের হুবহু কপি নয়।***   

<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img01.png" width="850">  

---
### ***Structural Similarities (গাঠনিক মিল):***   
***Perceptron-এর ডিজাইন অনেকটা biological neuron-এর বিভিন্ন অংশের মতো কাজ করে:***     

***`Dendrites vs Inputs`:    
Biological neuron-এ dendrites-এর মাধ্যমে input সংকেত আসে, যা perceptron-এর inputs (x1, x2) এবং তাদের weights (w1, w2)-এর সাথে তুলনীয়।***       

***`Nucleus vs Processing Block`:   
নিউরনের nucleus-এ সব ইন্টারনাল ক্যালকুলেশন হয়। Perceptron-এর ক্ষেত্রে এটি summation block (যেখানে dot product করা হয়) এবং activation function (যেমন step function)-এর সমান।***         

***`Axon vs Output`:     
নিউরনের axon দিয়ে যেভাবে output সংকেত বাইরে যায়, perceptron-এর final output ঠিক সেভাবেই কাজ করে।***    

---
### ***Key Differences (প্রধান পার্থক্য)***    
***`Complexity (জটিলতা):`       
একটি biological neuron অত্যন্ত জটিল একটি কোষ যা বিলিয়ন বিলিয়ন অন্য নিউরনের সাথে যুক্ত থাকে।     
অন্যদিকে, perceptron হলো একটি খুবই সাধারণ mathematical function বা model.***    

***`Processing Method:`   
নিউরনের nucleus-এর ভেতরে অত্যন্ত জটিল electro-chemical reactions ঘটে যা বিজ্ঞানীরা এখনো পুরোপুরি বুঝতে পারেননি।    
কিন্তু perceptron-এর প্রসেসিং খুবই সহজ; এটি শুধু একটি weighted sum বের করে এবং তাকে একটি নির্দিষ্ট ফাংশনের মধ্য দিয়ে পাস করে।***     

***`Neuroplasticity:`    
মানুষের নিউরনে neuroplasticity দেখা যায়, যার ফলে শেখার সাথে সাথে নিউরনের কানেকশনগুলো মোটা বা পাতলা হয় অথবা নতুন কানেকশন তৈরি হয়।        
কিন্তু একটি standard perceptron মডেলে এই কানেকশনগুলো একবার ডিফাইন করে দিলে তা আর নিজে থেকে পরিবর্তন হয় না (fixed connections)।***      

---
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img02.png" width="650">    

# ***Anatomy of the Architecture***    

***The design consists of several components:***   
- ***`Inputs (x1, x2)`: The features of your data.***
- ***`Weights (w1, w2)`: These determine the connection strength or feature importance.***
- ***`Bias (b)`: An additional parameter allowing the model to shift.***
- ***`Summation (Z)`: The linear combination of inputs and weights.***
- ***`Activation Function`: Used to bring the output into a specific range, such as -1 to 1 or 0 to 1. Examples include the Step function or ReLU.***   
   
***The mathematical equation for the weighted sum is: `Z = w1.x1 + w2.x2 + b`***   

***Initially, weights are assigned randomly. During training, the Perceptron Algorithm adjusts these weights to minimize the error between the predicted output and the actual output.***     
***If we look at the equation z = w1.x1 + w2.x2 + b, and set the boundary where z=0, we get the equation of a line:***    
***`Ax + By + C = 0`***

***This line divides the 2D plane into two regions:***   
- ***Positive Region: Where Ax + By + C ≥ 0.***  
- ***Negative Region: Where Ax + By + C < 0.***   

***We start with a random line and update it based on errors. This is often called the `Perceptron Trick`.***   

***The logic is simple:***
- ***`Case-1`:    
  If a point is positive (+ve) but falls in the negative region (misclassified), we add the point’s coordinates to the line’s coefficients.***
  <img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img03.png" width="250">   
- ***`Case-2`:   
  If a point is negative (-ve) but falls in the positive region (misclassified), we subtract the point’s coordinates.***   
  <img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img04.png" height="50" width="250">    

***Here, η represents the Learning Rate (e.g., 0.01).***
- ***The Simplified Update Rule   
  We can combine these conditions into a single elegant formula:***   
  <img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img05.png" height="100" width="250">  

***If the prediction is 0 (Correct classification), no update happens.   
If the prediction is wrong, the weights update automatically to shift the line.***   
***The goal of the Perceptron is to find the correct line (weights and bias) that separates the data classes perfectly.***    

---
# ***Example: Binary Classification with Neural Network***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img06.png" width="150">   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img07.png" width="600">  

***Trigger the training process with the Initial Random assumptions:***   
- ***Bias (b) = 0.25***   
- ***Weight 1 (w1) = 0.1***   
- ***Weight 2 (w2) = 0.2***   
- ***Learning rate (η eta) = 0.3***   
- ***Sigmoid Activation function = [1/(1+e^(−z))]***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img08.png" width="600">   

## ***Epoch-1***
***`1. First Sample (1, 2, 0)`***  
***Weighted sum: z = 0.25 + (0.1 * 1) + (0.2 * 2) = 0.25 + 0.1 + 0.4 = 0.75***  
***Sigmoid activation output: output = 1 / (1 + e^(−0.75)) ≈ 0.6792***  
***Error: error = 0 − 0.6792 = −0.6792***   

***Updated Weights and bias after First Sample:    
w1 = 0.1 + (0.3 * (−0.6792) * 1) = −0.10376  
w2 = 0.2 + (0.3 * (−0.6792) * 2) = −0.20752      
b = 0.25 + (0.3 * (−0.6792)) = 0.04624***  

***`2. Second Sample (2, 1, 0)`***   
***Weighted sum: z = 0.04624 + (−0.10376 * 2) + (−0.20752 * 1) = −0.3688   
Sigmoid activation output: output = 1 / (1 + e^(0.3688)) ≈ 0.4087   
Error: error = 0 − 0.4087 = −0.4087***      

***Updated Weights after Second Sample:    
w1 = −0.10376 + (0.3 * (−0.4087) * 2) = −0.34898    
w2 = −0.20752 + (0.3 * (−0.4087) * 1) = −0.33013    
b = 0.04624 + (0.3 * (−0.4087)) = −0.07637***    

***`3. Third Sample (2, 3, 0)`***    
***Weighted sum: z = −0.07637 + (−0.34898 * 2) + (−0.33013 * 3) = −1.76472    
Sigmoid activation output: output = 1 / (1 + e^(1.76472)) ≈ 0.1462   
Error: error = 0 − 0.1462 = −0.1462***   

***Updated Weights and bias after Third Sample:   
w1 = −0.34898 + (0.3 * (−0.1462) * 2) = −0.43670   
w2 = −0.33013 + (0.3 * (−0.1462) * 3) = −0.46171   
b = −0.07637 + (0.3 * (−0.1462)) = −0.12023***  

***`4. Fourth Sample (3, 3, 1)`     
Weighted sum: z = −0.12023 + (−0.43670 * 3) + (−0.46171 * 3) = −2.81546   
Sigmoid activation output: output = 1 / (1 + e^(2.81546)) ≈ 0.0565   
Error: error = 1 − 0.0565 = 0.9435***

***Updated Weights and bias after Fourth Sample:   
w1 = −0.43670 + (0.3 * 0.9435 * 3) = 0.41245   
w2 = −0.46171 + (0.3 * 0.9435 * 3) = 0.38744   
b = −0.12023 + (0.3 * 0.9435) = 0.16282***   

***`5. Fifth Sample (3, 4, 1)`  
Weighted sum: z = 0.16282 + (0.41245 * 3) + (0.38744 * 4) = 2.94993   
Sigmoid activation output: output = 1 / (1 + e^(−2.94993)) ≈ 0.9503   
Error: error = 1 − 0.9503 = 0.0497***   

***Updated Weights and bias after Fifth Sample:   
w1 = 0.41245 + (0.3 * 0.0497 * 3) = 0.45718    
w2 = 0.38744 + (0.3 * 0.0497 * 4) = 0.44708   
b = 0.16282 + (0.3 * 0.0497) = 0.17773***   

***`6. Sixth Sample (4, 3, 1)`   
Weighted sum: z = 0.17773 + (0.45718 * 4) + (0.44708 * 3) = 3.34769   
Sigmoid activation output: output = 1 / (1 + e^(−3.34769)) ≈ 0.9660   
Error: error = 1 − 0.9660 = 0.0340***   

***Updated Weights and bias after Sixth Sample:   
w1 = 0.45718 + (0.3 * 0.0340 * 4) = 0.49798   
w2 = 0.44708 + (0.3 * 0.0340 * 3) = 0.47768   
b = 0.17773 + (0.3 * 0.0340) = 0.18793***   

***`Final Weights after First Epoch`     
Bias (b) = 0.18793  
Weight 1 (w1) = 0.49798   
Weight 2 (w2) = 0.47768***    

<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img09.png" width="600">   

## ***Epoch-2***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img10.png" width="600">   

## ***Epoch-3***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img11.png" width="600">   

---
# ***Why the Perceptron Fails at XOR***
***The Core Problem is Not Linearly Separable.***  
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Perceptron/images/img12.png" width="650">  
***A perceptron computes: output = f(w1×x1 + w2×x2 + bias)  
This is a LINEAR equation.  
It can only draw:***  
- ***a LINE    in 2D***  
- ***a PLANE   in 3D***   
- ***a HYPERPLANE in higher dimensions***   

***XOR needs a BENT/CURVED boundary → impossible with one straight line.***  

- ***AND Gate: Linearly separable → Perceptron ✓***   
- ***OR Gate: Linearly separable → Perceptron ✓***   
- ***XOR Gate: NOT linearly separable → Perceptron ✗***   
- ***Fix for XOR: Stack layers → MLP → Deep Learning born***  

---
# ***Resources***
- [***The Math Behind Perceptron***](https://www.linkedin.com/pulse/math-behind-perceptron-step-by-step-guide-neural-sharat-manikonda-lpp5c/)
- [***Perceptron (ANN)***](https://medium.com/data-science-in-your-pocket/deep-learning-series-01-perceptron-ann-00eefdbbe3d0)   
- [***The Intuition Behind Perceptron***](https://ninamaamary.medium.com/the-intuition-behind-perceptrons-a58a03b1b874)  
- [***How Perceptrons Learn***](https://aa-nadim.medium.com/how-perceptrons-learn-intuition-and-edge-cases-24239c13af92)   

---
## ***Author***  
***Md. Rafiqul Islam***  
***CSE, CoU***   

