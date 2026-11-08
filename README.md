# 📸 Supabase Image Uploader & Direct Link Generator

A lightweight, modern, and fast single-file web application to upload images directly to **Supabase Storage** and generate instant public direct links. Built with pure HTML5, CSS3, and JavaScript—no heavy frameworks or backend required!

---

## 🚀 Features

* **⚡ Ultra Fast & Lightweight:** Single-page app with zero bundle overhead.
* **🔒 Direct Browser-to-Cloud Upload:** Uses Supabase JS Client SDK directly in the browser.
* **🔑 Secure Local Storage:** API Credentials (Project URL & Anon Key) are saved safely in your browser's `localStorage`—never sent to any middleman server.
* **📁 Public CDN Links:** Instant direct image URLs (`https://.../storage/v1/object/public/...`) ready for sharing or embedding.
* **📋 One-Click Copy:** Easily copy image markdown or direct links with visual status notifications.
* **🎨 Drag & Drop Support:** Modern, interactive UI with seamless file drop support.

---

## 🛠️ Prerequisites

Before using this app, you need a free **Supabase** account:
1. Sign up at [supabase.com](https://supabase.com).
2. Create a new project.
3. Go to **Storage** -> Click **New Bucket**.
4. Name the bucket `images` and make sure to toggle **Public Bucket** to **ON**.
5. Go to **Project Settings** -> **API** to grab your:
   * **Project URL**
   * **`anon` / public key**

---

## 🏁 Quick Start

1. Clone or download this repository:
   ```bash
   git clone [https://github.com/devsudipx/PictureToLink.git](https://github.com/devsudipx/PictureToLink.git)
