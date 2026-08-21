# ***Batch Normalization***

***Batch Normalization হলো একটা technique যেটা neural network-এর প্রতিটি layer-এর input/activation-এর values-কে normalize করে, যাতে সেগুলোর mean প্রায় 0 এবং variance প্রায় 1 এর কাছাকাছি থাকে। এর ফলে training-এর সময় data distribution বেশি stable থাকে, training faster হয়, learning সহজ হয়, gradient সমস্যা কমে, এবং model সাধারণত better perform করে। Batch Normalization সাধারণত activation function-এর আগে বা পরে ব্যবহার করা হয় এবং training-এর সময় batch-এর mean ও variance ব্যবহার করে normalization করে, তারপর learnable scale (γ) ও shift (β) দিয়ে network-কে প্রয়োজন অনুযায়ী values adjust করার সুযোগ দেয়।***   

---
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img1.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img2.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img3.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img4.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img5.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img6.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img7.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img8.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img9.png" width=750>   
<img src="https://github.com/Rafiqul-Islam12/Deep-Learning/blob/main/Batch%20Normalization/images/img10.png" width=750>   
