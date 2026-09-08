---
description: Workflow tự động deploy (đưa website lên sóng) bằng Cloudflare Pages
---
// turbo-all

Bước 1: Chạy lệnh Wrangler CLI để đẩy source code lên Cloudflare Pages Production.
(Lưu ý: Nếu token hết hạn, cần gõ `npx wrangler login` ở Terminal trước một lần).
```powershell
npx wrangler pages deploy . --project-name=biamavang --branch=production
```

Bước 2: Kiểm tra deployment đã lên sóng chưa.
```powershell
powershell -Command "(Invoke-WebRequest -Uri 'https://lambiamavang.com' -UseBasicParsing).Content.Contains('real_luanvan_cntt_dh_quocte.jpg')"
```


