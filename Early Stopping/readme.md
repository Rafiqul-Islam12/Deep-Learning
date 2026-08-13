# Early Stopping in Neural Network

## Early Stopping কী?

**Early Stopping** হলো Neural Network-এর একটি **Regularization Technique**, যা Training-এর সময় **Overfitting প্রতিরোধ করার জন্য** Training আগে থেকেই বন্ধ করে দেয়।

---

## কেন Early Stopping ব্যবহার করা হয়?

Training চলার সময় দুই ধরনের Loss দেখা হয়—

- **Training Loss** → Training Data-তে Error
- **Validation Loss** → নতুন (Unseen) Data-তে Error

প্রথমে দুটোই কমে, কিন্তু একসময় Validation Loss আবার বাড়তে শুরু করে। তখন Model Overfitting করছে।

> **Early Stopping সেই মুহূর্তেই Training বন্ধ করে দেয়।**

---

## কীভাবে কাজ করে?

1. Model প্রতিটি Epoch শেষে Training ও Validation Loss গণনা করে।
2. Validation Loss পর্যবেক্ষণ করা হয়।
3. যদি কয়েকটি Epoch ধরে Validation Loss উন্নতি না করে, তাহলে Training Stop হয়।
4. Best Validation Performance-এর Weight সংরক্ষণ করা হয়।

---

## গুরুত্বপূর্ণ টার্ম

- **Epoch:** পুরো Dataset একবার Training হওয়া।
- **Training Loss:** Training Data-এর Error।
- **Validation Loss:** Unseen Data-এর Error।
- **Patience:** কতগুলো Epoch অপেক্ষা করবে উন্নতি না হলেও।

---
## Early Stopping in Keras
- [Early Stopping](https://keras.io/api/callbacks/early_stopping/)
