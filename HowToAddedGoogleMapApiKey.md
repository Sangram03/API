
## 🌍 **How to Create a Google Maps API Key (Updated Guide)**

![Image](https://cdnblog.webkul.com/blog/wp-content/uploads/2019/12/Home-%E2%80%93-My-First-Project-%E2%80%93-Google-Cloud-Platform-1200x597.png?utm_source=chatgpt.com)

![Image](https://docs.shipperhq.com/hubfs/Knowledge%20Base%20Import/Screen_Shot_2020-04-06_at_2_04_46_PM-Jun-25-2025-10-39-21-6147-AM.png?utm_source=chatgpt.com)

![Image](https://cdnblog.webkul.com/blog/wp-content/uploads/2019/12/Credentials-Dummy-Project-Google-Cloud-Platform-1200x597.png?utm_source=chatgpt.com)

---

## ✅ **Step 1: Go to Google Cloud Console**

Open this link:
👉 **[https://console.cloud.google.com/](https://console.cloud.google.com/)**

Login with your Google account.

---

## ✅ **Step 2: Create a New Project**

1. On the top navigation bar, click **Project dropdown**.
2. Click **New Project**.
3. Give a project name (example: *My Maps Project*).
4. Click **Create**.

---

## ✅ **Step 3: Enable Maps API**

1. Inside your project, go to **Navigation Menu → APIs & Services → Library**
2. Search these APIs depending on your need:

   * **Maps JavaScript API** (for showing maps on website)
   * **Places API** (places autocomplete, search)
   * **Geocoding API** (convert address ↔ coordinates)
   * **Directions API** (routes)
3. Open each API → click **Enable**.

---

## ✅ **Step 4: Create Credentials (API Key)**

1. Go to **APIs & Services → Credentials**
2. Click **Create Credentials**
3. Choose **API Key**

Your API key will be generated instantly.

---

## 🛡️ **Step 5: (Very Important) Secure Your API Key**

Click on the created key → **Restrict Key**.

### Add restrictions:

### 🔒 **1. API Restrictions**

Select only the APIs you use (Maps JavaScript API, Places API, etc.)

### 🌐 **2. Website Restriction (if using on frontend)**

Add:

```
https://yourwebsite.com/*
http://localhost:3000/*
```

### 💻 **3. IP Restriction (if using on backend)**

Add server IPs.

### 📱 **4. Android/iOS restriction**

If using in mobile apps.

---

## 🚀 **Final Step: Use Your API Key**

Example (HTML + JS):

```html
<script async
    src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap">
</script>
```

