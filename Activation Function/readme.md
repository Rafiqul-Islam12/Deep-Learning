# ***Activation Function***

***Neural Network এর প্রতিটি node (neuron) এ input আসার পর একটা weighted sum হিসাব করা হয় (যেমন: w1x1 + w2x2 + ... + b)। এই সংখ্যাটাকে একটা নির্দিষ্ট output এ রূপান্তর করার জন্য যে function ব্যবহার করা হয়, সেটাই হলো Activation Function।***    
   
---
***Activation Function না থাকলে:***  
- ***পুরো Neural Network Linear Model হয়ে যাবে।***  
- ***Deep Neural Network অনেক layer থাকলেও complex relationship শিখতে পারবে না।***  
- ***Image, speech, face recognition-এর মতো complex problem solve করতে পারবে না।***

---
### ***কেন দরকার?***
- ***Non-linearity যোগ করা***   
  ***এটাই সবচেয়ে বড় কারণ। যদি Activation Function না থাকতো, তাহলে পুরো Neural Network শুধুমাত্র একটা Linear Regression এর মতো কাজ করতো — যতই layer বাড়ানো হোক না কেন, সবগুলো মিলে একটা single linear equation এ পরিণত হয়ে যেত। কারণ linear function এর সাথে linear function যোগ করলে সেটা linear-ই থাকে।***   
  ***বাস্তব জগতের সমস্যা (image recognition, language, ইত্যাদি) বেশিরভাগ ক্ষেত্রেই complex এবং non-linear। তাই Model কে জটিল pattern শেখানোর জন্য non-linearity অপরিহার্য।***  
- ***Output কে নির্দিষ্ট range এ আনা***   
  ***কিছু Activation Function output কে 0-1 বা -1 থেকে 1 এর মধ্যে বেঁধে রাখে, যা probability বা normalized value হিসেবে কাজে লাগে।***    
- ***কোন neuron "fire" (activate) হবে সেটা ঠিক করা***   
  ***Human brain এর neuron এর মতোই, একটা নির্দিষ্ট threshold পার হলেই neuron টা "active" হয় এবং পরের layer এ signal পাঠায়।***

---
## ***Example: Cat vs Dog Classification***    
***ধরো, CNN একটি Cat-এর ছবি input হিসেবে পেল।***    
***`Input Image (Cat)`***   
`        ↓         `   
***`Convolution Layer`***     

***Convolution Layer image থেকে feature বের করল।    
Output (Feature Map):***    
***`-3   2   5`***   
***` 4  -2   1`***   
***`-6   3   7`***    

***এখানে,   
Positive value = Strong feature     
Negative value = Weak বা unnecessary feature***     
    
***কিন্তু Convolution Layer জানে না কোনটা গুরুত্বপূর্ণ, কোনটা নয়। তাই সব value-ই output হিসেবে দেয়।   
যদি Activation Function না থাকে পরের layer-এ সব values চলে যাবে।***   
   
### ***Problem***     
- ***Negative value-গুলোও process হবে।***    
- ***অনেক unnecessary information নিয়ে computation হবে।***     
- ***Network complex feature ভালোভাবে শিখতে পারবে না।***   
  
### ***যদি ReLU Activation ব্যবহার করি***     
***ReLU-এর Formula:***   
***`               f(x)=max(0,x)                `***  

***অর্থাৎ,   
যদি value < 0 → 0  
যদি value > 0 → একই থাকবে***    
   
***Before ReLU***   
***`-3   2   5`***     
***` 4  -2   1`***   
***`-6   3   7`***  

***After ReLU***   
***`0   2   5`***   
***`4   0   1`***   
***`0   3   7`***     
   
***এখন CNN শুধুমাত্র strong features নিয়ে কাজ করছে।***  

---
# ***Tyepes of Activation Function***

## ***1. ReLU (Rectified Linear Unit)***   
***এটি positive input হলে input-কে যেমন আছে তেমনই return করে, আর negative input হলে 0 return করে।***   
***ReLU-এর Formula:***   
***`               f(x)=max(0,x)                `***    
***অর্থাৎ,   
যদি value < 0 → 0  
যদি value > 0 → একই থাকবে***    
   
- ***Range: [0, ∞)***  
       
***Before ReLU***   
***`-3   2   5`***     
***` 4  -2   1`***   
***`-6   3   7`***  

***After ReLU***   
***`0   2   5`***   
***`4   0   1`***   
***`0   3   7`***     

***কোথায় ব্যবহার হয়?***
- ***CNN-এর Hidden Layer***   
- ***Deep Neural Network-এর Hidden Layer***  

***Advantages***  
- ***Computationally Efficient***   
  ***খুব সহজ function, তাই training দ্রুত হয়।***   
- ***Non-Saturating Gradient***   
  ***Vanishing Gradient problem অনেক কম হয়, তাই Deep Network সহজে train করা যায়।***   
- ***Sparse Activation***   
  ***Negative output 0 হয়ে যায়, ফলে অনেক neuron inactive থাকে। এতে computation কমে এবং model efficient হয়।***   

***Disadvantages***  
- ***Dying ReLU Problem***  
  ***যদি কোনো neuron বারবার negative input পায়, তাহলে তার output সবসময় 0 হবে। তখন সেই neuron আর শেখে না (update হয় না), অর্থাৎ "dead" হয়ে যায়।***

---
## ***2. Sigmoid***    
***Sigmoid হলো একটি Activation Function, যা input value-কে 0 থেকে 1 এর মধ্যে convert করে। তাই এটি probability হিসেবে output দেয় এবং Binary Classification-এ বেশি ব্যবহৃত হয়।   
Formula:***   
***`       σ(x)= 1 / 1 + e^−x       `***   
   
***Example   
Input:***   
***`        -5    0    5       `***   
***Output:***    
***`    0.006   0.5   0.993       `***    

***অর্থাৎ,***       
***বড় Negative → 0-এর কাছাকাছি***   
***0 → 0.5***   
***বড় Positive → 1-এর কাছাকাছি***   

- ***Range: (0, 1)***   

***কোথায় ব্যবহার হয়?***    
- ***Binary Classification***   
- ***Output Layer-এ Probability বের করার জন্য***   

***Disadvantages***    
- ***Vanishing Gradient Problem***  
  ***যদি input খুব বড় positive বা বড় negative হয়, তাহলে output 1 বা 0-এর খুব কাছাকাছি চলে যায়। তখন gradient প্রায় 0 হয়ে যায়, ফলে weight update খুব কম হয় এবং model ধীরে শেখে।***  

---
## ***3. Softmax***  
***Softmax হলো একটি Activation Function, যা Multi-class Classification-এ ব্যবহার করা হয়। এটি model-এর raw output (scores)-কে probability-তে convert করে।      
সব class-এর probability-এর যোগফল (Sum) = 1 হয়।***       

***Example***       
***ধরো CNN একটি image দেখে ৩টি class-এর score দিল:***       
***`Cat   = 2.0`***        
***`Dog   = 5.0`***               
***`Lion  = 1.0`***      

***Softmax apply করার পর:***   
***`Cat   = 0.05`***   
***`Dog   = 0.90`***   
***`Lion  = 0.05`***    

***এখানে,   
সব probability-এর যোগফল = 1    
সবচেয়ে বেশি probability Dog (0.90), তাই prediction হবে Dog।***    

- ***Range: [0, 1]***     

***কোথায় ব্যবহার হয়?***    
- ***Output Layer***    
- ***Multi-class Classification***    

***Disadvantages***   
- ***Hidden Layer-এ ব্যবহার করা হয় না।***   
- ***এটি computationally expensive, কারণ সব class-এর probability একসাথে calculate করতে হয়।***   
- ***Outlier বা খুব বড় score-এর প্রতি sensitive হতে পারে, ফলে একটি class-এর probability অনেক বেশি হয়ে যেতে পারে।***   

---
# ***Resources***   
- [***Activation Functions***](https://medium.com/@vishnuam/activation-functions-in-convolutional-neural-networks-cnn-b1114a1b9b4d)     

---
## ***Author***
***MD RAFIQUL ISLAM   
CSE, CoU***   
