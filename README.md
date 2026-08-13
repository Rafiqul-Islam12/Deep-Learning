# Deep-Learning

---
## ***BASIC***
***Neural network training-এ প্রথমে Forward Propagation দিয়ে prediction তৈরি হয়। এরপর Loss Function prediction ও actual-এর পার্থক্য থেকে cost বের করে। তারপর Backpropagation chain rule ব্যবহার করে প্রতিটি weight-এর gradient হিসাব করে, অর্থাৎ কোন weight কতটা error-এর জন্য দায়ী তা নির্ধারণ করে। সবশেষে Gradient Descent সেই gradient ও learning rate ব্যবহার করে weight update করে, যাতে পরবর্তী prediction আরও accurate হয়। এই পুরো process বারবার repeat হতে থাকে, যতক্ষণ না cost minimum-এর কাছাকাছি পৌঁছে।***   

***`Backpropagation gradient বের করে, Gradient Descent সেই gradient ব্যবহার করে weight update করে।`***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img1.svg" width=450>

---
***`Step 1`: Forward Propagation***    
***প্রথমে input data network-এর ভিতরে যায়।   
ধরো তুমি student-এর CGPA, Skills, Experience দিলে network predict করল—    
Predicted = 0.80 (Job পাওয়ার probability)      
Actual = 1.00    
এখন prediction আর actual এক নয়।***    

***`Step 2`: Cost (Loss) Calculate   
এখানেই Cost Function আসে।   
Cost মানে model কতটা ভুল করেছে।***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img2.svg" width=450>  

***`Step 3`: Backpropagation  
এটাই সবচেয়ে important concept।   
ভাবো একটা network-এ ৩টা weight আছে।   
Backpropagation কোনো weight change করে না — শুধু gradient calculate করে।***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img3.svg" width=450>  

***`Step 4`: Gradient Descent — weight change  
Positive gradient → Weight কমাও   
Negative gradient → Weight বাড়াও***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img4.svg" width=450>  

***`Step 5`: আবার শুরু   
নতুন weight নিয়ে আবার prediction হবে।   
এবার prediction 0.80 থেকে 0.91 হলো।   
Cost কমে গেল।   
এই cycle চলে, যতক্ষণ না cost minimum-এর কাছাকাছি পৌঁছে।***   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/img5.svg" width=450>  

