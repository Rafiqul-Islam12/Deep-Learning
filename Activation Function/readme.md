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

## 1. ReLu




