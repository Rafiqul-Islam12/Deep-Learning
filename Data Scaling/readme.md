# Data Scaling in Neural Network

## Data Scaling কেন দরকার?  
**Data Scaling is used to normalize input features into a similar range, helping Gradient Descent converge faster and improving the stability and performance of the neural network.**  
**Data Scaling** হলো Input Feature-গুলোকে একই Range-এ আনার প্রক্রিয়া, যাতে Neural Network দ্রুত ও স্থিতিশীলভাবে শিখতে পারে।    

### কেন ব্যবহার করা হয়?

- বড় ও ছোট মানের Feature-এর প্রভাব সমান রাখতে।
- Gradient Descent দ্রুত Converge করতে।
- Training আরও Stable ও Efficient করতে।
- কোনো একটি Feature যেন অতিরিক্ত Dominant না হয়।

### উদাহরণ

ধরুন একটি Dataset-এ—

- Age = 22
- Income = 80,000

এখানে Income-এর মান অনেক বড়, তাই Scaling না করলে Model Income-কে বেশি গুরুত্ব দিতে পারে। Scaling করলে উভয় Feature একই Range-এ আসে
