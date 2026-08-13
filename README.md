# Deep-Learning

---
## ***BASIC***
***Neural network training-এ প্রথমে Forward Propagation দিয়ে prediction তৈরি হয়। এরপর Loss Function prediction ও actual-এর পার্থক্য থেকে cost বের করে। তারপর Backpropagation chain rule ব্যবহার করে প্রতিটি weight-এর gradient হিসাব করে, অর্থাৎ কোন weight কতটা error-এর জন্য দায়ী তা নির্ধারণ করে। সবশেষে Gradient Descent সেই gradient ও learning rate ব্যবহার করে weight update করে, যাতে পরবর্তী prediction আরও accurate হয়। এই পুরো process বারবার repeat হতে থাকে, যতক্ষণ না cost minimum-এর কাছাকাছি পৌঁছে।***  

<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Gradient%20Descent%20in%20Neural%20Networks/images/a90ddaa1-d726-406f-9183-867e4746f41f.svg" width=400>     
