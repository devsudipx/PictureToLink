# 📸 PictureToLink — Supabase Image Uploader

A lightweight, high-performance single-page web application that uploads images directly to **Supabase Storage** and generates instant, public direct links (`https://...`). Built with pure HTML5, CSS3, and Vanilla JavaScript—no backend server, build steps, or external build tools required.

Live Repository: [github.com/devsudipx/PictureToLink](https://github.com/devsudipx/PictureToLink)

---

## 🚀 Features

* **⚡ Fast & Lightweight:** Single-page application with zero framework overhead.
* **🔒 Direct-to-Cloud Upload:** Uses the official Supabase JS Client SDK directly inside the browser.
* **🔑 Local Credential Storage:** Saves your Supabase URL and Anon Key inside browser `localStorage` (never sent to third-party servers).
* **🌐 Public CDN Direct Links:** Instant URLs ready for embedding in apps, Markdown, HTML, or direct sharing.
* **📋 One-Click Copy:** Instant clipboard copy for direct URLs and Markdown image tags.
* **🎨 Modern Drag & Drop UI:** Interactive visual dropzone with responsive progress feedback.

---

## 🛠️ Supabase Prerequisites & Setup

1. Create a free account at [supabase.com](https://supabase.com).
2. Create a new project.
3. Go to **Storage** -> Click **New Bucket**.
4. Name the bucket `images` and make sure **Public Bucket** is toggled **ON**.
5. Retrieve your project credentials from **Project Settings** -> **API**:
   * **Project URL**
   * **`anon` / public key**

---

## ⚡ Step-by-Step SQL Policy Setup (Fix RLS Upload Error)

If you get `Error: new row violates row-level security policy`, you need to grant public insert permissions to your storage bucket using either method below:

### Method 1: SQL Editor (Recommended & Quickest)
1. Open your Supabase Dashboard and click on **SQL Editor** from the left sidebar.
2. Click **New Query**, paste the SQL snippet below, and click **Run**:

```sql
-- Allow public uploads to the 'images' storage bucket
CREATE POLICY "Allow public uploads" 
ON storage.objects 
FOR INSERT 
TO public 
WITH CHECK (bucket_id = 'images');
