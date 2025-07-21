# Case-Study---Data-Cleaning-and-Data-Wrangling
A practical case study focused on data cleaning and data wrangling using pandas. This project provides tools to preprocess Excel files by removing duplicates, detecting outliers, formatting dates (including Jalali), and cleaning messy or irrelevant columns for better data quality.


# 📊 Case Study - Data Cleaning and Data Wrangling

این پروژه یک مطالعه موردی (Case Study) در زمینه **پاک‌سازی داده‌ها (Data Cleaning)** و **مرتب‌سازی/ساختاردهی داده‌ها (Data Wrangling)** است. هدف، فراهم کردن ابزارها و روش‌هایی برای پردازش داده‌های خام اکسل و تبدیل آن‌ها به داده‌هایی با کیفیت و قابل استفاده برای تحلیل‌های آماری و مدل‌سازی است.

---

## 📁 ساختار فایل‌ها

| نام فایل | توضیح |
|----------|-------|
| `All_Sheets_at_One_Glance.ipynb` | نوت‌بوک اصلی برای بارگذاری تمام شیت‌های یک فایل Excel، بررسی آن‌ها، و اعمال مراحل پاک‌سازی اولیه با استفاده از توابع فایل کمکی. |
| `helper.py` | فایل کمکی شامل مجموعه‌ای از توابع مهم برای پردازش، پاک‌سازی و گزارش‌گیری از داده‌ها. این توابع برای حذف داده‌های زائد، بررسی داده‌های پرت، تبدیل تاریخ، و ارائه گزارش ساختاری استفاده می‌شوند. |

---

## ✅ قابلیت‌های کلیدی

### در فایل نوت‌بوک (`All_Sheets_at_One_Glance.ipynb`)
- بارگذاری تمام شیت‌های یک فایل اکسل در یک نگاه
- بررسی اولیه داده‌ها: نمایش، سایز، ساختار، اطلاعات آماری
- استفاده از توابع ماژول `helper.py` برای:
  - حذف ستون‌های بدون ارزش
  - پاک‌سازی ردیف‌های تکراری
  - بررسی مقادیر خالی و محاسبه نسبت آن‌ها
  - تشخیص مقادیر پرت
  - تشخیص مقادیر با کاراکترهای ویژه

### در فایل `helper.py`:
- `strip_dataframe(df)`: حذف فاصله‌ها از سلول‌های متنی
- `drop_unvalued_columns(df)`: حذف ستون‌های کاملاً خالی، یا پر از فاصله یا با مقدار یکتا
- `drop_repeated_rows(df)`: حذف ردیف‌های تکراری
- `to_jalali_date(column, year_dir='L')`: تبدیل تاریخ میلادی به شمسی با پشتیبانی از فرمت‌های مختلف
- `empty_cells_info(df)`: گزارش تعداد سلول‌های خالی در هر ستون و در کل
- `count_distinct_values(df)`: بررسی تعداد مقادیر یکتا و نوع داده در هر ستون
- `detect_special_values(column)`: بررسی و شمارش مقادیر دارای کاراکترهای خاص (مثل @، !، فاصله و ...)
- `detect_outliers(df, column)`: شناسایی مقادیر پرت در ستون عددی بر اساس IQR

---

## 🧰 پیش‌نیازها

قبل از اجرای پروژه، کتابخانه‌های زیر باید نصب شده باشند:

```bash
pip install pandas numpy jdatetime jalali_pandas prettytable
```

# راهنمای استفاده از پروژه

🧪 **نحوه استفاده**

**اجرای نوت‌بوک:**
1. فایل نوت‌بوک را در Jupyter Notebook یا Google Colab باز کنید.
2. فایل Excel مورد نظر را آپلود کرده و آدرس آن را در کد مشخص کنید.
3. توابع مورد نیاز را از `helper.py` ایمپورت کرده و استفاده نمایید.

```python
from helper import (
    strip_dataframe,
    drop_unvalued_columns,
    drop_repeated_rows,
    to_jalali_date,
    empty_cells_info,
    count_distinct_values,
    detect_special_values,
    detect_outliers
)
```
📜 **مجوز (License)**
این پروژه تحت لایسنس MIT منتشر شده و استفاده‌ی شخصی، آموزشی و توسعه‌ای از آن آزاد است.


🧪 **ارتباط با من**
## Contact
For questions, bugs, or suggestions, please:

- Open an issue on GitHub.  
- Contact the author at [hadi.shirin@gmail.com](mailto:hadi.shirin@gmail.com)
   

