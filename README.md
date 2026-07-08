<img width="1440" alt="Screenshot 2024-08-05 at 7 14 57 PM" src="https://github.com/user-attachments/assets/696a2309-d2aa-490e-9e06-df8f279ba2d9">
<img width="1440" alt="Screenshot 2024-08-05 at 7 12 56 PM" src="https://github.com/user-attachments/assets/bc7c6e28-c554-4ef1-b82d-0919f68da7e8">

# Steam Game Path Analysis Crawler

A web crawler that traces the shortest link path between two Steam game pages by following related-game links. It uses **MechanicalSoup** to navigate the Steam store, **Redis** to manage the crawl queue, and **MongoDB** to store crawled pages and links — then reconstructs and prints the hop-by-hop path once the target page is reached.

## 🔗 Developer
- [@Mitchell Cootauco](https://github.com/Mcootauc)

## 🛠️ Tech Stack
### Language
![Python](https://img.shields.io/badge/-Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
### Database & Queue
![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
### Libraries
- **MechanicalSoup** — headless browsing and HTML parsing
- **configparser** — configuration management

## ⚙️ How It Works
1. **Initialization** — Opens the MongoDB connection, sets up the Redis crawl queue, and starts a MechanicalSoup headless browser.
2. **Crawling** — Starts from a source page, downloads and parses each page for links, pushes valid links to the Redis queue, and stores them in
