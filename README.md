# mongo-assignment-2-easy

1. List All Products in the "Electronics" Category

   Code: db.products.aggregate([
  {
    $match: { category: "Electronics" }
  }
])

   <img width="664" alt="image" src="https://github.com/user-attachments/assets/a124c9e9-a4dd-4064-a26c-efcd4e5ae957" />
   
   ![image](https://github.com/user-attachments/assets/f3400dfa-7c2c-4440-b16a-6296164fff5e)


2. Count Products per Category

    Code: db.products.aggregate([
  {
    $group: {
      _id: "$category",
      count: { $sum: 1 }
    }
  }
])

![image](https://github.com/user-attachments/assets/0a535e3c-e391-4f28-84bd-64d2cce51267)


3. Product Names and Prices, Sorted by Price (Descending)

 Code: db.products.aggregate([
  {
    $project: {
      _id: 0,
      name: 1,
      price: 1
    }
  },
  {
    $sort: { price: -1 }
  }
])

![image](https://github.com/user-attachments/assets/f7c0175b-2b61-42bd-a96b-cbd05d698291)

![image](https://github.com/user-attachments/assets/53f88195-99dd-4251-bd34-1b80046e7dd3)




