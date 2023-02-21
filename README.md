# tse_option


[![Downloads](https://static.pepy.tech/personalized-badge/tse-option?period=total&units=international_system&left_color=grey&right_color=red&left_text=TotalDownloads)](https://pepy.tech/project/tse-option)
[![Downloads](https://static.pepy.tech/personalized-badge/tse-option?period=month&units=international_system&left_color=grey&right_color=orange&left_text=Downloads/month)](https://pepy.tech/project/tse-option)
![Downloads](https://img.shields.io/badge/version-0.1.1.0-brightgreen)


این پکیج جهت بررسی و قیمت گذاری اوراق اختیار معامله موجود در بورس اوراق بهادار تهران و فرابورس ایران ایجاد شده است. لازم به یادآوری است که در این ماژول از مدل ارائه شده توسط بلک-شولز-مرتون در سال 1973 برای قیمت گذاری اختیار معامله استفاده شد است. سعی بر آن است که در نسخه های بعدی سایر مدل های قیمت گذاری نیز اضافه شوند.

برخی از توابع این پروژه،از ماژول های [finpy_tse](https://github.com/ARahimiQuant/finpy-tse) و [tsemodule5](https://github.com/python4financeacademy/tsemodule5) اقتباس شده اند.

----------------------------------------------

**توجه**: کلیه خروجی این ماژول از جمله قیمت گذاری و محاسبه تلاطم ضمنی و ... به جهت تسهیل در تصمیم گیری سرمایه گذاران است و هیچگونه پیشنهادی برای خرید یا فروش آن محسوب نمی شود. لذا تمامی عواقب سرمایه گذاری به عهده شخص سرمایه گذار است و توسعه دهندگان هیچ مسئولیتی در قبال زیان های احتمالی ندارند.

----------------------------------------------


**تغییرات نسخه جدید(0.1.1.0)**: 


1- امکان دانلود تاریخچه قیمت سهام و اوراق اختیار معامله


2- رفع برخی مشکلات


----------------------------------------------




### نصب
```python
pip install tse-option
```

### فراخوانی
```python
import tse_option as tso
```

-----------------------------------------------------------------


#### دریافت داده های مربوط به تمام اختیار معامله های موجود روی یک سهم خاص
```python
df = tso.pricing_based_on_stock(stock_name="خودرو", trading_days=100, IV=False, leverage=True, P_BSM=False, sort="Maturity")
```

**stock_name:**  نماد سهم مورد نظر


**trading_days:**  تعداد روزهای معاملاتی مورد نظر که تلاطم تاریخی براساس آن محاسبه می شود.


**IV:**  محاسبه تلاطم ضمنی یا Implied Volatility


**leverage:** نمایش مقدار اهرم اختیار معامله


**P_BSM:** نمایش نسبت قیمت بازار به قیمت تئوری بلک-شولز-مرتون


**sort:** نحوه مرتب شدن دیتافریم خروجی

(می توان از متغیرهایی چون زمان باقی مانده تا سررسید(Maturity)،قیمت اعمال(Strike Price) و موقعیت های باز(Open Interest) برای مرتب سازی استفاده کرد)


-----------------------------------------------------------------

#### دریافت داده های مربوط به یک اختیار معامله خاص
```python
df = tso.pricing_based_on_option(option_name="ضسپا1205", trading_days=100, IV=False, leverage=True, P_BSM=False, sort="Maturity")
```
**option_name:** نماد اختیار معامله مورد نظر


**IV:**  محاسبه تلاطم ضمنی یا Implied Volatility


**leverage:** نمایش مقدار اهرم اختیار معامله


**P_BSM:** نمایش نسبت قیمت بازار به قیمت تئوری بلک-شولز-مرتون


-----------------------------------------------------------------


برای مشاهده مثال های بیشتر [اینجا](https://github.com/sm-sokout/tse-option/blob/master/Example/Example.ipynb) کلیک کنید.

-----------------------------------------------------------------



This project on github [tse-option](https://github.com/sm-sokout/tse-option)
