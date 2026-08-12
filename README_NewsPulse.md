# 📰 NewsPulse

> A lightweight, responsive news aggregation website that fetches and displays the latest articles using the NewsAPI.

**NewsPulse** is a front-end news reader built with HTML, CSS, and vanilla JavaScript. Users can browse news by category or search for a topic and open the original article directly from a news card.

## ✨ Features

- 📰 Fetches live news articles using **NewsAPI**
- 🔎 Search for news by keyword
- 🏏 Quick category navigation for:
  - IPL
  - Finance
  - Politics
  - Technology
- 🖼️ Displays article images, titles, descriptions, sources, and publication dates
- 🔗 Click any news card to open the original article
- 📱 Responsive card-based layout
- 🎨 Clean and minimal user interface
- ⚡ Built entirely with vanilla JavaScript — no framework required

## 🛠️ Tech Stack

- **HTML5** — Page structure
- **CSS3** — Styling and responsive layout
- **JavaScript (ES6+)** — API requests, search, navigation, and dynamic rendering
- **NewsAPI** — News data source

## 📂 Project Structure

```text
NewsPulse/
│
├── index.html        # Main webpage
├── styles.css        # Website styling
├── index.js          # API calls and application logic
├── logo.png          # Website logo
└── README.md         # Project documentation
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/NewsPulse.git
cd NewsPulse
```

### 2. Get a NewsAPI API key

Create an account on [NewsAPI](https://newsapi.org/) and generate an API key.

### 3. Add your API key

In `index.js`, configure your API key:

```javascript
const apikey = "YOUR_NEWS_API_KEY";
```

> **Important:** Never commit a real API key to a public GitHub repository. The API key shown in the original project should be revoked/rotated and replaced with a new key. For a production application, keep secrets on a backend/server rather than exposing them in browser JavaScript.

### 4. Run the project

Because this is a static front-end project, you can run it using a local development server.

For example, with VS Code, use the **Live Server** extension and open `index.html`.

You can also use Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## 🔍 How It Works

When the page loads, the application requests news for India:

```javascript
window.addEventListener('load', () => fetchNews("India"));
```

The application then:

1. Sends a request to the NewsAPI.
2. Receives a list of articles.
3. Filters out articles without images.
4. Clones the news-card HTML template.
5. Inserts the article data into the card.
6. Adds the card to the page.
7. Opens the original article when the card is clicked.

### Search

Users can enter a keyword into the search box. For example:

```text
science
```

The application fetches matching articles and replaces the currently displayed news.

### Category Navigation

The navigation buttons call:

```javascript
onNavItemClick('technology');
```

which fetches news related to the selected category.

## 🎨 UI Overview

The application consists of three main areas:

### Navigation Bar

Contains:

- Project logo
- IPL category
- Finance category
- Politics category
- Technology category
- Search input and button

### News Cards

Each article is displayed as a card containing:

- Article image
- Title
- Source
- Publication date
- Description

Clicking a card opens the article in a new browser tab.

### Responsive Layout

The cards use a flexible layout that allows multiple articles to appear across the page and wrap onto additional rows.

## 🔧 Customization

### Change the default news query

In `index.js`:

```javascript
window.addEventListener('load', () => fetchNews("India"));
```

Change `"India"` to another search term.

### Add another category

Add a navigation item in `index.html`:

```html
<li
    class="hover-link nav-item"
    id="science"
    onclick="onNavItemClick('science')"
>
    SCIENCE
</li>
```

The existing JavaScript function can then fetch articles for that category.

### Customize the design

Modify `styles.css` to change:

- Colors
- Card dimensions
- Typography
- Navigation spacing
- Search-bar styling
- Hover effects
- Responsive behavior

## 📸 Suggested Improvements

Future versions of NewsPulse could include:

- Pagination or infinite scrolling
- Loading indicators
- Error handling for failed API requests
- "No articles found" messages
- Dark mode
- Country and language filters
- Article category filters
- Bookmark/favorite functionality
- Better mobile navigation
- Backend API proxy for securely handling the API key

## ⚠️ Known Limitations

- The NewsAPI key is required to retrieve articles.
- The current implementation exposes the API request in client-side JavaScript.
- The contact/backend functionality is not applicable because this project is a front-end news reader.
- API availability and request limits depend on the NewsAPI plan being used.
- Some articles may not contain an image or description.

## 🔐 Security Note

**Do not publish your actual NewsAPI key in GitHub.**

If a real API key has already been pushed to a public repository:

1. Revoke or rotate the exposed key.
2. Remove it from the source code.
3. Remove it from Git history if necessary.
4. Use a backend/server-side proxy for production applications.

For local experimentation, replace the placeholder with your own development key.

## 📄 License

This project is available for educational and personal portfolio use. Add a specific open-source license such as MIT if you want others to freely reuse and modify the project.

---

### 👨‍💻 Author

**Shyam Ande**

Built with HTML, CSS, JavaScript, and NewsAPI.

⭐ If you found this project useful, consider giving the repository a star!
