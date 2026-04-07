---
description: Workflow tự động deploy (đưa website lên sóng) bằng Cloudflare Pages
---
// turbo-all

Bước 1: Chạy lệnh Wrangler CLI để đẩy source code lên Cloudflare Pages Production.
Hệ thống đã login bằng `npx wrangler login` trước đó.
Domain: lambiamavang.com (DNS CNAME qua Netlify → biamavang.pages.dev)

Thực thi lệnh sau tại thư mục dự án:
```powershell
npx wrangler pages deploy . --project-name=biamavang --branch=production
```

Bước 2: (Tuỳ chọn) Kiểm tra deployment đã lên chưa.
```powershell
Invoke-WebRequest -Uri "https://biamavang.pages.dev" -Method Head -UseBasicParsing | Select-Object StatusCode, StatusDescription
```
