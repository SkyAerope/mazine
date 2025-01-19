# Mazine

[English](readme.md) · [简体中文](/MDs/Mazine_zh.md)

Mazine is a **Serverless modern image hosting application** built on **Next.js 14** and object storage services, with the following features:

- **No database management**: No longer worry about database failures causing image hosting to go down.
- **Code Hosting**: The project code is hosted on **GitHub** and deployed to **Vercel**.
- **Environment Variable Management**: Passwords and related environment variables must be manually added to Vercel to ensure the security of sensitive information.

### CDN Security and Recommended Configuration

Due to the high risk of password leaks when handling CDN through open-source code, this project does not include any CDN conversion code. It is recommended to manage the CDN using the following methods:

1. **R2 Custom Subdomain**: Secure access by configuring a dedicated R2 subdomain.
2. **Cloudflare Worker**: Use Cloudflare Worker for efficient CDN acceleration and processing.
3. **Alist S3 CDN Functionality**: Leverage Alist integration for easy CDN implementation.

## Features

- 🚀 Based on Next.js 14 App Router
- 📦 Supports multiple object storage services (S3, Alist, etc.)
- 🎨 Responsive design + dark mode
- 🔒 Simple password protection
- 📋 One-click copy in multiple formats (URL, Markdown, BBCode)
- 💾 Image compression and WebP conversion
- 🖼️ Supports grid view and timeline view, card-style management and preview
- ❤️ Image favorites functionality
- 🔍 Image search feature

## [✈️Take a look in YouTube](https://youtu.be/SAv8wK-1I6s?si=fii0mtWhbZO6IM5T)

![home_1.webp](/MDs/home_1.webp)

![manage_1.webp](/MDs/manage_1.webp)

![manage_2.webp](/MDs/manage_2.webp)

---

### [Q&A☑️](/MDs/Declaration.md) — [中文✅](/MDs/Declaration_zh.md)

---

## Deployment

### 1.Fork this repository

### 2.Using R2

This project is developed and tested using Cloudflare R2 as the storage bucket, and other S3 buckets have not been tested.  
If using R2 as the storage backend, the configuration example is:

[✡️R2-setting-guide, click here!!!!!](/MDs/R2-setting.md)

```env
S3_REGION=APAC
S3_ACCESS_KEY=your-access-key
S3_SECRET_KEY=your-secret-key
S3_BUCKET_NAME=your-bucket
S3_ENDPOINT=http://localhost:9000
ACCESS_PASSWORD=ur-password
NEXT_PUBLIC_CDN=xxx.r2.dev or Custom Domain
NEXT_PUBLIC_LANGUAGE=EN
```

### 3.Vercel Deployment

#### import the respsitory to vercel

![vercel_2.webp](/MDs/vercel_2.webp)

![vercel_3.webp](/MDs/vercel_3.webp)

#### setup your Environment Varicables

![vercel_1.png](/MDs/vercel_1.png)

#### deploy and spend 1 min on your drink!

#### enjoy!!



## To-Do Features

- Alist S3 integration
- Other S3 integrations
- Mobile upload functionality (only the upload page, preserving image favorites feature, excluding management and favorites pages)
- Docker deployment
- Cloudflare Worker version (more complete, but subject to worker policy; waiting for updates)

### Tech Stack

- Next.js 14
- TypeScript
- Tailwind CSS
- AWS SDK for JavaScript v3

------

### **Commercial Use Restriction**

The code and resources in this project are for personal or non-commercial use only. Commercial use in any form is strictly prohibited. Without explicit written permission from the copyright holder, this code cannot be used for any profit-making or commercial activities, including but not limited to product development, service provision, or commercial promotion.

------

### **Prohibited Distribution Without Permission**

The source code, documentation, and all related resources of this project must not be publicly disclosed, released, distributed, or shared by any third-party institution or company without permission from the copyright holder. Specifically, **this project is prohibited from being published on MSDN or any similar platform**, whether it's the full code or parts of it.

------

## License Statement

This project is licensed under the Apache License 2.0. You are free to use, modify, and distribute the project as long as you retain the copyright notice of the original author.

------

## Disclaimer

This project does not actively collect user privacy data. Image storage is fully managed by the user's object storage service, and the developer is not responsible for its privacy.

This project is open-source software, and the developer is not responsible for any direct or indirect loss caused by the use of this software. Users must ensure that their use complies with relevant laws and regulations in their country or region.

This project is strictly prohibited from being used for any illegal activities or infringing on third-party copyrights. Users bear the legal responsibility for improper use.

The services provided by this project are not guaranteed to be error-free. Users must assume the risks associated with using this project. The author is not responsible for any losses or damages caused by using this project.
