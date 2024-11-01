### English Version

# Sublink Worker

Sublink Worker is a lightweight subscription conversion tool that can be deployed on Cloudflare Worker. It converts various proxy protocol URLs into subscription links compatible with different clients. Additionally, it offers flexible customization rules and API support.

## Features

- Supported protocols: ShadowSocks, VMess, VLESS, Hysteria2, Trojan, TUIC
- Supports importing Base64-encoded http/https subscription links
- One-click deployment with Vanilla JS + Cloudflare Worker, no backend required
- Supported clients:
  - Sing-Box
  - Clash
  - Xray/V2Ray
- Generates fixed/random short links (based on KV)
- Light/Dark theme toggle
- Flexible API with scripting support
- User-friendly web interface with customizable rules
  - Offers multiple predefined rule sets
  - Allows custom geo-site, geo-ip, ip-cidr, and domain-suffix policy groups

## Deployment

### Quick Deployment
[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/mohammadham/sublink-worker)

### Manual Deployment
- Clone the repository: `git clone https://github.com/mohammadham/sublink-worker.git`
- Install dependencies: `npm install`
- Configure Cloudflare account credentials
- Deploy using Wrangler: `wrangler deploy`

## API Documentation

Detailed API documentation is available in [API-doc.md](/doc/API-doc.md).

Key endpoints include:

- `/singbox`: Generates Sing-Box configuration
- `/clash`: Generates Clash configuration
- `/xray`: Generates Xray configuration
- `/shorten`: Generates shortened links

## Recent Updates

- 2024-10-3
  - Now supports saving and managing custom shortened links

[View Changelog](/doc/update-log.md)

## Project Structure

```
.
├── index.js                 # Main server logic, handles request routing
├── BaseConfigBuilder.js     # Builds base configuration
├── SingboxConfigBuilder.js  # Builds Sing-Box configuration
├── ClashConfigBuilder.js    # Builds Clash configuration
├── ProxyParsers.js          # Parses various proxy protocol URLs
├── utils.js                 # Provides utility functions
├── htmlBuilder.js           # Generates HTML for the web interface
└── config.js                # Stores configuration information
```

## Contributing

Feel free to submit Issues and Pull Requests to improve this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This project is for educational and research purposes only. Do not use it for illegal purposes. The developer is not responsible for any consequences resulting from the use of this project.

---

### نسخه فارسی

# Sublink Worker

Sublink Worker یک ابزار کوچک و کارآمد برای تبدیل لینک‌های اشتراک‌گذاری پروکسی است که بر روی Cloudflare Worker قابل استقرار است. این ابزار می‌تواند لینک‌های اشتراک انواع پروتکل‌های پروکسی را به لینک‌هایی تبدیل کند که با کلاینت‌های مختلف سازگار هستند. همچنین از قوانین سفارشی و API انعطاف‌پذیر پشتیبانی می‌کند.

## ویژگی‌ها

- پروتکل‌های پشتیبانی‌شده: ShadowSocks، VMess، VLESS، Hysteria2، Trojan، TUIC
- پشتیبانی از وارد کردن لینک‌های اشتراک‌گذاری رمزگذاری شده با Base64
- استقرار با یک کلیک، بدون نیاز به بک‌اند با استفاده از Vanilla JS و Cloudflare Worker
- کلاینت‌های پشتیبانی‌شده:
  - Sing-Box
  - Clash
  - Xray/V2Ray
- ایجاد لینک‌های کوتاه ثابت یا تصادفی (بر اساس KV)
- امکان تغییر تم به روشن/تاریک
- API انعطاف‌پذیر با پشتیبانی از عملیات اسکریپتی
- رابط کاربری ساده و کاربرپسند با قابلیت سفارشی‌سازی قوانین
  - شامل چندین مجموعه قانون از پیش تعریف‌شده
  - امکان تعریف گروه‌های سیاستی سفارشی برای geo-site، geo-ip، ip-cidr، و domain-suffix

## استقرار

### استقرار سریع
[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/mohammadham/sublink-worker)

### استقرار دستی
- کلون کردن مخزن پروژه: `git clone https://github.com/mohammadham/sublink-worker.git`
- نصب وابستگی‌ها: `npm install`
- تنظیم مدارک حساب Cloudflare
- استقرار با Wrangler: `wrangler deploy`

## مستندات API

مستندات کامل API در [API-doc.md](/doc/API-doc.md) موجود است.

مهم‌ترین نقاط انتهایی شامل موارد زیر است:

- `/singbox`: تولید تنظیمات Sing-Box
- `/clash`: تولید تنظیمات Clash
- `/xray`: تولید تنظیمات Xray
- `/shorten`: تولید لینک‌های کوتاه

## به‌روزرسانی‌های اخیر

- 2024-10-3
  - اکنون امکان ذخیره و مدیریت لینک‌های کوتاه سفارشی فراهم است

[مشاهده تاریخچه تغییرات](/doc/update-log.md)

## ساختار پروژه

```
.
├── index.js                 # منطق اصلی سرور، مدیریت مسیرها
├── BaseConfigBuilder.js     # ساخت تنظیمات پایه
├── SingboxConfigBuilder.js  # ساخت تنظیمات Sing-Box
├── ClashConfigBuilder.js    # ساخت تنظیمات Clash
├── ProxyParsers.js          # تجزیه لینک‌های پروکسی مختلف
├── utils.js                 # توابع کاربردی
├── htmlBuilder.js           # ایجاد HTML برای رابط کاربری وب
└── config.js                # ذخیره تنظیمات
```

## مشارکت

با ارسال Issues و Pull Requests می‌توانید در بهبود این پروژه مشارکت کنید.

## مجوز

این پروژه تحت مجوز MIT است. برای اطلاعات بیشتر به فایل [LICENSE](LICENSE) مراجعه کنید.

## سلب مسئولیت

این پروژه صرفاً برای اهداف آموزشی و تحقیقاتی است. از آن برای مقاصد غیرقانونی استفاده نکنید. توسعه‌دهنده هیچ‌گونه مسئولیتی در قبال عواقب استفاده از این پروژه ندارد.
