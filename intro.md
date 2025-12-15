# MongoDB
- MongoDB is basically NoSQL.


| Feature        | SQL           | NoSQL (MongoDB)            |
| -------------- | ------------- | -------------------------- |
| Schema         | Fixed         | Flexible                   |
| Data Model     | Tables        | Documents                  |
| Relationships  | Foreign keys  | Embedded docs / references |
| Scalability    | Vertical      | Horizontal                 |
| Consistency    | Strong (ACID) | Eventual (configurable)    |
| Query Language | SQL           | JSON-style                 |
| Use Case       | Banking, ERP  | Web apps, APIs             |

- 🧠 **When to use MongoDB** (important)

- MongoDB is best when:

- Schema keeps changing

- Rapid development

- High read/write load

- JSON-based APIs

- Microservices

Examples:

- E-commerce catalog

- User profiles

- Logs

- Analytics

- Social media apps





<img width="994" height="1002" alt="image" src="https://github.com/user-attachments/assets/fed076ab-aca3-40f3-b6ac-9da2f82525be" />



<img width="952" height="538" alt="image" src="https://github.com/user-attachments/assets/44505233-8c30-4691-bda3-abbe0bdfe526" />



## Mongoose
<img width="910" height="912" alt="image" src="https://github.com/user-attachments/assets/665f1072-f15b-4c33-8424-f68ee82fbf10" />




```js
const DB = process.env.DATABASE.replace(
  "<PASSWORD>",
  process.env.DATABASE_PASSWORD
);
mongoose
  .connect(DB, {
    useNewUrlParser: true,
    useCreateIndex: true,
    useFindAndModify: false,
  })
  .then((con) => {
    console.log(con.connections);
    console.log("DB connection Successful!");
  });
const toursSchema = new mongoose.Schema({
  name: {
    type: String,
    required: true,
  },
  rating: Number,
  price: {
    type: Number,
    required: true,
  },
});
const Tour = mongoose.model("Tour", toursSchema);
```



- Firstly, we created a Database Connection using `DB`.
- Then, we used `connect()` method and then we handled that promise using `then()` .
- Then we created toursSchema , basically a schema we will use.
- Then lastly set up our model `Tour` using `model()` method.
