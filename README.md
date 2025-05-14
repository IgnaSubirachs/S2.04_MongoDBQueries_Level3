# 📄 Description – Exercise Statement

In this exercise, we worked with a MongoDB collection of **Restaurants** in New York City and wrote over **25 different queries**—ranging from simple `find()` operations to more advanced filters involving projections, array indexing, comparison operators, regular expressions, sorting, pagination, and type checks. By correctly constructing and running each of these queries against the provided `restaurants.json` dataset, we achieved **Level 3** mastery of MongoDB querying.

---

# 💻 Technologies Used

* **MongoDB** (Community Edition or Atlas)
* **MongoDB Shell** (`mongosh`)
* **MongoDB Compass** (GUI for building and testing queries)
* **JSON** (for the `restaurants.json` dataset)
* **JavaScript** (query syntax in the shell)

---

# 📋 Requirements

* **MongoDB Server** (v4.0+) installed locally or accessible via Atlas
* **MongoDB Shell** (`mongosh`) or **MongoDB Compass**
* **Node.js** (optional, if you want to script the imports)
* The `restaurants.json` data file (provided in this repo or exercise bundle)
* Basic familiarity with JSON and command-line tools

---

# 🛠️ Installation

1. **Clone or download** this exercise bundle, which includes `restaurants.json`.
2. **Import the dataset** into your MongoDB instance:

   ```bash
   mongoimport \
     --db ITAcademy \
     --collection Restaurants \
     --file ./restaurants.json \
     --jsonArray
   ```
3. **Verify** that the `Restaurants` collection now contains documents:

   ```bash
   mongosh
   > use ITAcademy
   > db.Restaurants.count()
   ```

---

# ▶️ Execution

You can run the queries either in **mongosh** or with **MongoDB Compass**:

### 1. In `mongosh`

```js

// Example: find all documents, project only name and cuisine, exclude _id
db.Restaurants.find(
  {},
  { name: 1, cuisine: 1, _id: 0 }
).limit(10)
```

* Paste any of the prepared queries into the shell and press **Enter**.

### 2. In MongoDB Compass

1. Select the **ITAcademy** database and **Restaurants** collection.
2. Click **Documents**, then the `{}` icon next to **Find** to open the panels.
3. Fill in:

   * **Filter**: your query criteria (e.g. `{ borough: "Bronx" }`)
   * **Project**: fields to include or exclude (e.g. `{ name: 1, _id: 0 }`)
   * **Skip**, **Limit**, **Sort** as needed
4. Click **Find** to view results.

---

By following these instructions, you can reproduce each of the 25+ queries that demonstrate advanced MongoDB querying techniques and confirm you’ve achieved Level 3 proficiency!
