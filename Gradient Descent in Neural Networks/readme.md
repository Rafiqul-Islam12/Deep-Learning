# ***Gradient Descent***

***Neural network training-এ প্রথমে Forward Propagation দিয়ে prediction তৈরি হয়। এরপর Loss Function prediction ও actual-এর পার্থক্য থেকে cost বের করে। তারপর Backpropagation chain rule ব্যবহার করে প্রতিটি weight-এর gradient হিসাব করে, অর্থাৎ কোন weight কতটা error-এর জন্য দায়ী তা নির্ধারণ করে। সবশেষে Gradient Descent সেই gradient ও learning rate ব্যবহার করে weight update করে, যাতে পরবর্তী prediction আরও accurate হয়। এই পুরো process বারবার repeat হতে থাকে, যতক্ষণ না cost minimum-এর কাছাকাছি পৌঁছে।***   

***`Backpropagation gradient বের করে, Gradient Descent সেই gradient ব্যবহার করে weight update করে।`***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img1.svg" width=450>   

---
## ***কীভাবে Neural Network তার weight ধীরে ধীরে update করে minimum cost-এ পৌঁছায়?***
 
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img6.png" width=450>    

***এই ছবিটি একটি Cost Function Graph, যেখানে দেখানো হয়েছে কীভাবে Gradient Descent ধাপে ধাপে Cost কমিয়ে Minimum Cost-এ পৌঁছায়।***

***`১. Initial Weight`   
Training শুরুতে Model-এর Weight Random থাকে। এই অবস্থানে Cost অনেক বেশি থাকে, তাই এটিই Starting Point।***     

***`২. Cost (Y-axis)`   
Y-axis হলো Cost বা Loss, যা Prediction কতটা ভুল হয়েছে তা প্রকাশ করে। Cost যত কম হবে, Model তত ভালো কাজ করবে।***    

***`৩. Weight (X-axis)`    
X-axis হলো Weight বা Model Parameter। Gradient Descent এই Weight-ই পরিবর্তন করে Cost কমায়।***    
 
***`৪. Gradient`   
Gradient হলো Cost Curve-এর ঢাল (Slope)। এটি বলে দেয় কোন দিকে Weight পরিবর্তন করলে Cost কমবে।***    

***Gradient = dJ/dw   
Positive Gradient → Weight কমে   
Negative Gradient → Weight বাড়ে***   

***`৫. Incremental Step`     
Model একবারে Minimum-এ যায় না। ছোট ছোট Step নিয়ে Weight আপডেট করে।***    

***Weight Update:   
w(new) = w(old) − α × dJ/dw   
এখানে α হলো Learning Rate, যা প্রতিটি Step-এর আকার নির্ধারণ করে।***   

***Minimum Cost   
Curve-এর সর্বনিম্ন বিন্দুই Minimum Cost। এখানে Error সবচেয়ে কম এবং Gradient প্রায় শূন্য, তাই Model-এর Weight প্রায় Optimal হয়ে যায়।***   

---
# ***Types of Gradient Descent***

<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img9.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img10.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img11.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img12.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img13.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img14.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img15.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img16.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img17.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img18.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img19.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img20.png" width=900>    
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img21.png" width=900>    

 ---
 # ***Resources***
 - [***CampusX (YouTube)***](https://youtu.be/7z6yXpYk7sw?si=xNYpPfsUoAFuHhha)
 - [***Nice Explanation***](https://medium.com/data-science/batch-mini-batch-stochastic-gradient-descent-7a62ecba642a)

# ***Author***
***MD. RAFIQUL ISALM   
CSE,CoU***  


