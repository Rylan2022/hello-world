Creating a library website using only simple HTML, CSS, and JavaScript involves the following steps:

1. **Plan the Website:**
   - Define the structure and features of your library website. For instance, you might need a homepage, a catalog page, a book details page, and a contact page.

2. **Set Up Your Project:**
   - Create a new project folder.
   - Inside this folder, create subfolders for `css`, `js`, and `images`.

3. **Create HTML Files:**
   - Create an `index.html` file for the homepage.
   - Create additional HTML files for other pages (e.g., `catalog.html`, `book-details.html`, `contact.html`).

4. **Design the Layout with CSS:**
   - Create a `style.css` file inside the `css` folder.
   - Link this CSS file in your HTML files using `<link rel="stylesheet" href="css/style.css">`.

5. **Add JavaScript for Interactivity:**
   - Create a `script.js` file inside the `js` folder.
   - Link this JavaScript file in your HTML files using `<script src="js/script.js"></script>`.

Here’s a basic example to get you started:

### 1. index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Library</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Welcome to the Library</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="catalog.html">Catalog</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <main>
        <h2>Featured Books</h2>
        <div id="featured-books"></div>
    </main>
    <script src="js/script.js"></script>
</body>
</html>
```

### 2. css/style.css
```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

nav a {
    color: #fff;
    margin: 0 15px;
    text-decoration: none;
}

main {
    padding: 20px;
    text-align: center;
}

#featured-books {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.book {
    background-color: #fff;
    border: 1px solid #ddd;
    margin: 10px;
    padding: 10px;
    width: 200px;
}
```

### 3. js/script.js
```js
document.addEventListener('DOMContentLoaded', () => {
    const featuredBooks = [
        { title: "Book 1", author: "Author 1" },
        { title: "Book 2", author: "Author 2" },
        { title: "Book 3", author: "Author 3" }
    ];

    const featuredBooksContainer = document.getElementById('featured-books');

    featuredBooks.forEach(book => {
        const bookDiv = document.createElement('div');
        bookDiv.classList.add('book');
        bookDiv.innerHTML = `<h3>${book.title}</h3><p>${book.author}</p>`;
        featuredBooksContainer.appendChild(bookDiv);
    });
});
```

### 4. Additional Pages
Repeat the process for creating the `catalog.html`, `book-details.html`, and `contact.html` files. For each page, make sure to include the same header and navigation structure, and adjust the content within the `<main>` section as needed.

### Basic Folder Structure:
```
project-folder/
│
├── css/
│   └── style.css
│
├── js/
│   └── script.js
│
├── index.html
├── catalog.html
├── book-details.html
└── contact.html
```

This setup provides a simple yet functional library website. You can expand it by adding more CSS styles, JavaScript functionality (like search and filter for books), and additional HTML pages as required.
