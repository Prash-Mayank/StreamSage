# StreamSage

> **Stream, Rate & Download** Movies in HD, Full HD & 4K Ultra Quality

[![Live Demo](https://img.shields.io/badge/Live%20Demo-streamsage.netlify.app-4ecdc4?style=for-the-badge&logo=netlify)](https://streamsage.netlify.app)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TMDB](https://img.shields.io/badge/TMDB%20API-01D277?style=for-the-badge&logo=themoviedatabase&logoColor=white)](https://www.themoviedb.org/documentation/api)

![StreamSage Banner](./streamsage.png)

StreamSage is a feature-rich, client-side movie discovery platform that lets users browse trending films, watch trailers, manage a wishlist, and simulate downloads — all powered by the TMDB API.

---

## Features

### Movie Discovery
- **10 browsable categories** — Trending, Popular, Top Rated, Now Playing, Upcoming, Action, Comedy, Horror, Romance, Sci-Fi
- **Real-time search** with debounced input (triggers after 2+ characters)
- **Pagination** with Previous / Next controls
- **Infinite scroll / Auto-load** mode (toggleable)

### Movie Detail Modal
- Full backdrop image with blurred overlay
- Embedded YouTube trailer (auto-fetched)
- Rating, release year, and vote count
- Overview / synopsis
- Download section with quality selection

### Download Manager
- Simulated downloads with live progress bars
- Quality options: **720p HD (1.2 GB)**, **1080p FHD (2.8 GB)**, **4K UHD (8.5 GB)**
- Pause, Resume, and Remove individual downloads
- Pause All / Resume All / Remove All controls
- Download speed indicator
- Status badges on movie cards (Downloading / Downloaded)
- Persistent download panel (slide-in from right)

### Wishlist
- Bookmark any movie with a single click
- Persistent wishlist panel (slide-in from left)
- Remove individual items
- Wishlist icons update live across all visible cards

### Notifications Panel
- Onboarding notification with all keyboard shortcuts
- Toggle panel with badge count

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + D` | Open Download Panel |
| `Ctrl + L` | Open Wishlist Panel |
| `Ctrl + O` | Open Notification Panel |
| `Ctrl + P` | Pause All Downloads |
| `Ctrl + R` | Resume All Downloads |
| `Ctrl + M` | Scroll to Top |
| `Ctrl + I` | Toggle Auto-Load (Infinite Scroll) |
| `Esc` | Close any Panel or Modal |
| `>` / `<` | Next / Previous Page |
| `Alt + 1-0` | Switch between 10 categories |

---

## Project Structure

```
streamsage/
├── index.html       # All HTML, CSS, and JavaScript in a single file
└── logo.png         # App logo (favicon + header)
```

StreamSage is a **single-file application** — all styles and scripts are embedded directly in `index.html`.

---

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- An active internet connection (for TMDB API calls)
- No build tools, frameworks, or installations required

### Running Locally

```bash
# 1. Clone the repository
git clone https://github.com/dhruv865/StreamSage.git

# 2. Navigate into the project folder
cd streamsage

# 3. Open index.html in your browser
open index.html
# or just double-click index.html
```

For best results, serve via a local server to avoid any CORS quirks:

```bash
# Using Python
python -m http.server 8080

# Using Node.js (npx)
npx serve .
```

Then open `http://localhost:8080` in your browser.

---

## API Reference

StreamSage uses the [TMDB (The Movie Database) API](https://www.themoviedb.org/documentation/api).

| Endpoint | Purpose |
|----------|---------|
| `/trending/movie/week` | Trending movies |
| `/movie/popular` | Popular movies |
| `/movie/top_rated` | Top-rated movies |
| `/movie/now_playing` | Currently in theatres |
| `/movie/upcoming` | Upcoming releases |
| `/discover/movie?with_genres=` | Genre-filtered movies |
| `/search/movie?query=` | Search movies by title |
| `/movie/{id}/videos` | Fetch YouTube trailer key |

**Base URL:** `https://api.themoviedb.org/3`  
**Image CDN:** `https://image.tmdb.org/t/p/w500` (posters) and `https://image.tmdb.org/t/p/w1280` (backdrops)

> Note: The API key is embedded in the source for demo purposes. For production use, proxy API calls through a backend to keep the key secret.

---

## Tech Stack

| Technology | Usage |
|------------|-------|
| HTML5 | Semantic structure |
| CSS3 | Animations, glassmorphism, responsive grid |
| Vanilla JavaScript (ES6+) | All logic, state, and API calls |
| TMDB API | Movie data and trailers |
| Font Awesome 6 | Icons |
| Google Fonts (Inter) | Typography |
| Animate.css | Entry animations |
| AOS (Animate on Scroll) | Scroll-based reveal |

---

## Responsive Design

StreamSage is fully responsive across all screen sizes:

- **Desktop (1400px+)** — Full multi-column grid, all panels and toggles visible
- **Tablet (768px)** — Adjusted grid, stacked search, condensed categories
- **Mobile (480px)** — Single-column grid, full-width panels, touch-friendly buttons

---

## Planned Features

- [ ] User authentication and cloud-synced wishlist
- [ ] Dark / Light theme toggle
- [ ] TV Shows support
- [ ] Movie ratings and user reviews
- [ ] Advanced filters (year, language, sort order)
- [ ] PWA support for offline browsing

---

## Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## License

This project is open source and available under the [MIT License](LICENSE).

---

## Author

**Dhruv Tripathi**

- Website: [streamsage.netlify.app](https://streamsage.netlify.app)
- GitHub: [github.com/dhruv865](https://github.com/dhruv865)
- LinkedIn: [linkedin.com/in/dhruvtripathi865](https://www.linkedin.com/in/dhruvtripathi865/)

---

<p align="center">Crafted with love for movie lovers by <strong>Dhruv Tripathi</strong></p>
<p align="center">© 2024 StreamSage. All rights reserved.</p>
