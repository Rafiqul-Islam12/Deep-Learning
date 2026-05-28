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
