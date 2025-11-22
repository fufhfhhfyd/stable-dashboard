# AdGen Studio - AI-Powered Social Media Ads

## Project info

**URL**: https://lovable.dev/projects/99e68166-71ae-4c3a-8c66-a105a2ab328e

## 🚀 Setup Instructions

### 1. Supabase Storage Setup (Required)

Before using the ad creation feature, you **must** set up a Supabase Storage bucket:

1. Go to your Supabase project dashboard
2. Navigate to **SQL Editor**
3. Copy and run the SQL commands from `supabase-storage-setup.sql` in this repo

This creates the `ad-files` bucket with public read access for storing uploaded images and videos.

### 2. Configure App Settings

In the app's **Settings** page, configure:
- **Supabase URL**: Your Supabase project URL
- **Supabase Anon Key**: Your Supabase anonymous/public key  
- **n8n Generate Webhook**: Your n8n workflow webhook for ad generation
- **n8n Post Webhook**: Your n8n workflow webhook for posting to social media
- **Database Table Name**: Default is `social_media_videos`

### 3. Key Features & Fixes

✅ **Fixed Issues:**
- Auto-redirect after clicking "Generate" button - now stays on current page
- Button label corrected to "Update Image" for image uploads
- Form data persists in local storage when navigating between tabs
- File inputs properly separated (images only for "Update Product Image", images/videos for others)
- Webhook now receives file **URLs** instead of Base64 data (files uploaded to Supabase Storage first)

📋 **Features:**
- **Create Ads**: Generate AI-powered ads with image/video uploads
  - Update Product Image (images only)
  - Product Ads (images/videos)
  - UGC Ads (images/videos)
- **Post Management**: View, edit, and manage generated ads
- **Local Storage**: Form data persists across page navigation
- **File Upload**: Files uploaded to Supabase Storage, URLs sent to webhooks

## How can I edit this code?

There are several ways of editing your application.

**Use Lovable**

Simply visit the [Lovable Project](https://lovable.dev/projects/99e68166-71ae-4c3a-8c66-a105a2ab328e) and start prompting.

Changes made via Lovable will be committed automatically to this repo.

**Use your preferred IDE**

If you want to work locally using your own IDE, you can clone this repo and push changes. Pushed changes will also be reflected in Lovable.

The only requirement is having Node.js & npm installed - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)

Follow these steps:

```sh
# Step 1: Clone the repository using the project's Git URL.
git clone <YOUR_GIT_URL>

# Step 2: Navigate to the project directory.
cd <YOUR_PROJECT_NAME>

# Step 3: Install the necessary dependencies.
npm i

# Step 4: Start the development server with auto-reloading and an instant preview.
npm run dev
```

**Edit a file directly in GitHub**

- Navigate to the desired file(s).
- Click the "Edit" button (pencil icon) at the top right of the file view.
- Make your changes and commit the changes.

**Use GitHub Codespaces**

- Navigate to the main page of your repository.
- Click on the "Code" button (green button) near the top right.
- Select the "Codespaces" tab.
- Click on "New codespace" to launch a new Codespace environment.
- Edit files directly within the Codespace and commit and push your changes once you're done.

## What technologies are used for this project?

This project is built with:

- Vite
- TypeScript
- React
- shadcn-ui
- Tailwind CSS
- Supabase (Database & Storage)

## How can I deploy this project?

Simply open [Lovable](https://lovable.dev/projects/99e68166-71ae-4c3a-8c66-a105a2ab328e) and click on Share -> Publish.

## Can I connect a custom domain to my Lovable project?

Yes, you can!

To connect a domain, navigate to Project > Settings > Domains and click Connect Domain.

Read more here: [Setting up a custom domain](https://docs.lovable.dev/features/custom-domain#custom-domain)
