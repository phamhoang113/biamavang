---
description: Workflow tự động deploy (đưa website lên sóng)
---
// turbo-all

Bước 1: Chạy lệnh Netlify CLI để đẩy source code lên Production.
```powershell
npx netlify deploy --prod --dir=. --site=9a07713b-bb26-414b-9bb5-b0fb9a4fa6d4
```

Bước 2: Kiểm tra deployment đã lên sóng chưa.
```powershell
Invoke-WebRequest -Uri "https://lambiamavang.com" -Method Head -UseBasicParsing | Select-Object StatusCode, StatusDescription
```

