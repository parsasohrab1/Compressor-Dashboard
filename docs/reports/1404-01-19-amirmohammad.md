###  گزارش کار روزانه پروژه

**تاریخ:** 1404/01/19   
**تهیه‌کننده:** امیر محمد شریفی

---

### ✅ خلاصه فعالیت‌های انجام‌شده:

1. **پیاده‌سازی الگوریتم ژنتیک برای بهینه‌سازی ویژگی‌های کلیدی کمپرسور**  
2. **استخراج مقادیر بهینه برای هر ویژگی و ذخیره‌سازی در فایل CSV**  
3. **ایجاد کلاس پیشنهاددهنده بلادرنگ برای اصلاح ورودی‌ها (RealTimeRecommender)**  
4. **طراحی و اجرای مکانیزم تست برای پیشنهاد خودکار اصلاح ورودی‌های فعلی**

---

### 🔧 شرح فنی اقدامات:

#### ۱. الگوریتم ژنتیک برای بهینه‌سازی ویژگی‌ها:
- استفاده از کتابخانه DEAP برای ساختاردهی الگوریتم ژنتیک
- تعریف توابع fitness برای اندازه‌گیری انحراف هر ویژگی از محدوده نرمال
- بهینه‌سازی جداگانه هر ویژگی با تنظیمات ژنتیک (selection، mutation، crossover)
- انتخاب بهترین نمونه به‌عنوان مقدار بهینه برای هر ویژگی

#### ۲. ذخیره مقادیر بهینه:
- مقادیر بهینه خروجی برای ۱۲ ویژگی مختلف مانند فشار ورودی، دمای ورودی، جریان، راندمان، مصرف برق و ...  
- ساخت یک DataFrame و ذخیره خروجی به صورت `optimal_values.csv`  
- این مقادیر به‌عنوان مرجع برای تشخیص انحراف در ورودی‌های آینده استفاده می‌شوند

#### ۳. پیاده‌سازی کلاس RealTimeRecommender:
- تعریف یک کلاس Python با هدف مقایسه ورودی فعلی با مقادیر بهینه  
- در صورت انحراف بیش از مقدار تعیین‌شده (`tolerance`) پیشنهاد اصلاح عددی ارائه می‌شود  
- خروجی‌های کلاس به زبان ساده و قابل فهم برای اپراتور طراحی شده‌اند

#### ۴. تست کلاس پیشنهاددهنده:
- اجرای تابع `report()` برای نمایش پیشنهاد اصلاح هر ویژگی  
- بررسی درستی مقایسه و محاسبه انحراف
- مشاهده پیام‌هایی مانند "در محدوده بهینه" یا "تغییر مقدار به..." بر اساس داده تست

---

### 📁 فایل‌های تولیدشده:
- `optimal_values.csv` شامل مقادیر بهینه نهایی هر ویژگی کمپرسور  
- کد کامل Python برای الگوریتم ژنتیک و کلاس پیشنهاددهی بلادرنگ

---

### 📌 نکات قابل توجه:
- الگوریتم ژنتیک عملکرد مناسبی در تطبیق با محدوده‌های تعریف‌شده از خود نشان داد  
- کلاس پیشنهاددهنده پتانسیل پیاده‌سازی در محیط صنعتی یا داشبورد نظارتی را دارد  
- می‌توان این کد را در آینده با داده‌های Real-time ادغام کرد و برای پایش لحظه‌ای استفاده نمود

---
