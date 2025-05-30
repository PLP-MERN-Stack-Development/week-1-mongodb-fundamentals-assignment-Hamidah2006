📚 PLP Bookstore MongoDB Setup

This project demonstrates a simple MongoDB database setup for a bookstore using Node.js. It includes inserting book records and preparing the database for CRUD operations and aggregation pipelines.


---

🛠️ Requirements

Node.js installed (https://nodejs.org)

MongoDB installed locally OR a MongoDB Atlas account

MongoDB Node.js Driver installed (mongodb)



---

📦 Installation & Setup

1. Clone this Repository or download the insert_books.js file.


2. Navigate to the Project Directory:

cd your-project-folder


3. Install MongoDB Driver:

npm install mongodb


4. Configure MongoDB URI
Open the insert_books.js file and replace the connection URI:

const uri = "mongodb://localhost:27017"; // Use Atlas URI if needed

For MongoDB Atlas, your URI will look like:

mongodb+srv://<username>:<password>@cluster.mongodb.net/?retryWrites=true&w=majority




---

▶️ Run the Script

node insert_books.js


---

✅ What the Script Does

Connects to a MongoDB database called plp_bookstore

Drops the books collection if it already exists

Inserts 10 pre-defined book documents into the books collection

Prints the inserted books to the console



---

📂 Project Structure

.
├── insert_books.js     # Script to insert book data into MongoDB
├── queries.js          # (Optional) File to store all your MongoDB queries
├── README.md           # Setup and usage guide


---

🧪 Sample Queries (to be used in queries.js or MongoDB Shell)

// Find all books in a specific genre
db.books.find({ genre: "Fiction" });

// Find books published after a certain year
db.books.find({ published_year: { $gt: 2000 } });

// Find books by a specific author
db.books.find({ author: "George Orwell" });

// Update the price of a specific book
db.books.updateOne({ title: "Moby Dick" }, { $set: { price: 14.99 } });

// Delete a book by its title
db.books.deleteOne({ title: "The Great Gatsby" });


---

📘 Notes

For MongoDB Atlas, ensure your IP is whitelisted and database access credentials are correct.

Use MongoDB Compass or mongosh to visually explore your data if preferred.
