# 📰 NewsPulse

> A lightweight, responsive news aggregation website that fetches and displays the latest articles using the NewsAPI.

**NewsPulse** is a front-end news reader built with HTML, CSS, and vanilla JavaScript. Users can browse news by category or search for a topic and open the original article directly from a news card.

## ✨ Features

* 📰 Fetches live news articles using **NewsAPI**
* 🔎 Search for news by keyword
* 🏏 Quick category navigation for IPL, Finance, Politics, and Technology
* 🖼️ Displays article images, titles, descriptions, sources, and publication dates
* 🔗 Click any news card to open the original article
* 📱 Responsive card-based layout
* 🎨 Clean and minimal user interface
* ⚡ Built entirely with vanilla JavaScript

## 🛠️ Tech Stack

* **HTML5**
* **CSS3**
* **JavaScript (ES6+)**
* **NewsAPI**

## 📂 Project Structure

```text
NewsPulse/
├── index.html
├── styles.css
├── index.js
├── logo.png
└── README.md
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/NewsPulse.git
cd NewsPulse
```

### 2. Get a NewsAPI key

Create an account on NewsAPI and generate an API key.

### 3. Configure the API key

In `index.js`:

```javascript
const apikey = "YOUR_NEWS_API_KEY";
```

> ⚠️ Never commit a real API key to a public GitHub repository. The API key included in the original code should be rotated/revoked before publishing.

### 4. Run the project

You can use VS Code's **Live Server** extension, or:

```bash
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## 🔍 How It Works

When the page loads, NewsPulse requests news for India. The application then retrieves articles from NewsAPI, dynamically generates news cards, and displays them on the page.

Users can also:

* Search for any topic
* Select IPL, Finance, Politics, or Technology
* Click an article to open the original source

## 🎨 Customization

You can modify `index.html` to change the categories and page content.

Use `styles.css` to customize colors, typography, spacing, cards, navigation, and hover effects.

Use `index.js` to modify API requests, search behavior, article rendering, and navigation.

## 🚀 Future Improvements

* Pagination or infinite scrolling
* Loading indicators
* Error handling
* Dark mode
* Country and language filters
* Article bookmarks
* Better mobile navigation
* "No articles found" messages
* Backend API proxy for secure API-key handling

## 🔐 Security

**Do not publish your NewsAPI key on GitHub.**

If the key in your original source code has already been pushed to a public repository, rotate/revoke it before publishing the project.

For a production version, the API key should be kept on a backend server rather than exposed in browser JavaScript.

## 📄 License

This project is available for educational and personal portfolio use. Add an open-source license such as MIT if you want others to freely reuse and modify the project.

---

### 👨‍💻 Author

**Shyam Ande**

Built with HTML, CSS, JavaScript, and NewsAPI.

⭐ If you found this project useful, consider giving the repository a star!
::: 
