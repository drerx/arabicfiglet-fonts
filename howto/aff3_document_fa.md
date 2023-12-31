# مستند AFF3
مستند نگارش ۳ قلم آراسته.

## این مستند چیست
برای پشتیبانی بهتر از متن دوسویه، لازم است قلم یک سویهٔ پیشفرض داشته باشد و هم‌چنین گلیف‌ها بتوانند سویهٔ خنثی داشته باشند. حالت سویهٔ خنثی یا بدون سویه برای نویسه‌هایی مثل فاصله یا علایم نگارشی کاربرد دارد.

برای این کار لازم است نگارش جدیدی از قلم آراسته ساخته شود. این نگارش، به دلیل تغییر در سرآیند قلم و سرآیند هر گلیف، با نگارش پیشین سازگاری ندارد.

## ویژگی‌های AFF نگارش ۳ و تفاوت‌ها با نگارش پیشین
دو چیز اصلی به این نگارش اضافه شده است:
- امکان تعیین سویهٔ پیشفرض برای قلم.
- امکان تعیین سویهٔ خنثی یا حالت بدون سویه برای هر نویسه.

### تفاوت‌های فنی با نگارش پیشین
این قلم ۲ تفاوت اصلی دارد.
1. در سرآیند قلم، یک پارامتر در انتهای قبلی‌ها اضافه شده است که سویهٔ پیشفرض قلم را تعیین می‌کند.
2. برای تعیین سویه (چه در گلیف‌ها و چه در سرآیند قلم) برای قلم‌های چپ‌به‌راست از این پس لازم است از عدد 2 استفاده شود. عدد 0 برای نویسه‌های بدون سویه استفاده خواهد شد.

## ساختار فایل
این یک فایل متنی است. شامل یک سرآیند که کلیات قلم را توصیف می‌کند و تعدادی بلوک که هر کدام یکی از گلیف‌های قلم را توصیف می‌کنند.

خط اول این فایل متنی سربرگ است که شامل موارد زیر است:


```
aff3 A B C D E F
```

این سرآیند از ۶ بخش تشکیل شده است. بخش اول آن aff3 است که نمایانگر فرمت فایل می‌باشد.  
۵ مورد بعدی عدد هستند که توضیحات آن‌ها در زیر آمده است.
1. ارتفاع نویسه‌ها که باید عددی ثابت باشد.
2. خط کرسی. شمارهٔ خط کرسی نویسه‌ها از بالا. شماره‌گذاری خطوط از ۱ آغاز می‌شود.
3. تعداد خط‌های کامنت (توضیحات) که بعد از سرآیند می‌آید.
4. بیشینهٔ طول بلوک. طول بزرگ‌ترین بلوک (اندازهٔ طولانی‌ترین خط در بین همهٔ بلوک‌ها).
5. تعداد بلوک‌های موجود در قلم
6. سویهٔ پیشفرض قلم. برای چپ‌به‌راست عدد 2 و برای راست‌به‌چپ عدد 1 استفاده می‌شود. عدد 0 یعنی قلم سویهٔ پیشفرض ندارد.

**نکته**: بهتر است برای قلم‌های فارسی که اغلب قلم‌های آراسته چنین هستند، سویهٔ پیشفرض برابر 1 قرار داده شود.



چند خط بعدی توضیحات هستند. مواردی مانند اسم طراح قلم، پروانهٔ قلم یا تاریخ انتشار را می‌توانید در این‌جا ذکر کنید. تعداد خطوط توضیحات باید در سربرگ مشخص شود.

بعد از سربرگ و توضیحات، نوبت تعریف هر گلیف می‌رسد. به هر یک از آن‌ها یک بلوک می‌گوییم.


### بلوک‌ها

هر بلوک از یک سربرگ و سپس نویسه‌های خود بلوک تشکیل می‌شود. ارتفاع همهٔ بلوک‌ها باید باهم یکسان باشد.

سربرگ بلوک از ۲ خط تشکیل شده است. مانند زیر و شامل موارد زیر است.
```
A
B C
```

1. یک نویسه یا یک رشته از نویسه‌ها. این در یک خط مستقل می‌آید.
2. تنوع این نویسه. اگر تنوع مهم نیست یا می‌خواهید همه‌جا قابل‌استفاده باشد، از عدد 0 استفاده کنید. اعداد 1 تا 4 هم به‌ترتیب برای تنوع‌های اول، وسط، آخر، تنها هستند.
3. سویهٔ نویسه. برای قلم‌های راست‌به‌چپ این عدد 1 است و برای قلم‌های چپ‌به‌راست این عدد 2 است. برای نویسه‌های بدون سویه یا با سویهٔ خنثی مثل فاصله یا علایم نگارشی، این عدد 0 است.

بعد از دو خط سربرگ، خود حروف گلیف در تعدادی خط می‌آیند. مشابه شکل زیر:

```
ب
1 1
            
            
            
          ██
  ██████████
            
      ██    
            
```

## نحوهٔ استفاده از این قلم
نرم‌افزارهای هنر اسکی مانند آراسته، ابتدا باتوجه‌به سربرگ قلم و سربرگ‌های نویسه‌ها، آن‌ها را می‌خواند و نگاشتی از رشته‌ها به گلیف‌ها ایجاد می‌کند.

هنگامی که می‌خواهد یک نوشته را رندر کند تا هنراسکی آن را بسازد، ابتدا دنبال بلندترین زیررشته‌ای از آن می‌گردد که در فهرستش موجود باشد.

سپس به تنوع محل قرارگیری آن رشته در فهرست نگاه می‌کند. اگر مطابق با زیررشتهٔ موجود در متن باشد، از آن برای رندر استفاده می‌کند. اگر مطابق نباشد، سراغ موردی که عدد تنوع آن صفر است می‌رود و از آن استفاده می‌کند. اگر تنوع صفر هم موجود نباشد، سراغ زیررشته‌های با طول کوتاه‌تر می‌رود.

بعد با توجه به راست‌به‌چپ یا چپ‌به‌راست بودن، این گلیف‌ها را پشت سر هم می‌چیند.

برای پشتیبانی از متن دوسویه، نرم‌افزاری مثل آراسته لازم است ابتدا زیررشته‌های راست‌به‌چپ و چپ‌به‌راست را در متن جدا کند و هر یک را جداگانه در جهت خودش رندر کند و سپس به هم بچسباند.

البته الگوریتم مورداستفاده برای این کار بستگی به خود نرم‌افزار دارد اما انتظار می‌رود گلیف‌های یک نوشتهٔ لاتین از چپ به راست و گلیف‌های یک نوشتهٔ عربی از راست به چپ پشت سر هم چیده شوند.

## راهنما برای طراحی قلم
می‌توانید همهٔ نویسه‌ها را مثل یک قلم flf یا aff1 طراحی کنید. فقط باید به سربرگ‌ها توجه کنید و آن‌ها را با استاندارد جدید تطبیق دهید. همچنین دقت کنید که در استاندارد aff3 در انتهای خطوط نویسهٔ «@» وجود ندارد.

سپس برای نویسه‌هایی مثل سریا، لازم است رشته‌هایی با طول بیشتر از یک نویسه تعریف کنید. مثلاً برای سریا ممکن است چنین بلوکی ایجاد کنید:

```
هٔ
3 1

  _
 (_
___)
  __
 /  |
 \__|
    \____



```

خط اول بلوک بالا نشان می‌دهد که این بلوک برای رشتهٔ سریا که از کنارهم‌چیده‌شدن دو نویسهٔ «ه» و «ٔ» تشکیل شده، طراحی شده است.

عدد اول در خط دوم نشان می‌دهد که این برای تنوع سوم سریا است. یعنی وقتی که از سمت راست به حرف دیگری بچسبد ولی از سمت چپ به حرف دیگری نچسبد.

عدد دوم در خط دوم نشان می‌دهد که این مربوط به یک قلم راست‌به‌چپ است که خانوادهٔ عربی از این نوع هستند.

چند خط بعدی شکل گلیف سریا (ـهٔ) را با نویسه‌های اسکی ترسیم کرده است که به شکل یک «ـه» در تنوع سوم آن به همراه یک «ی» کوچک در بالای آن است.

همچنین تعداد خط‌ها در این بلوک مهم است. فرض شده که ارتفاع هر بلوک در سربرگ این قلم برابر ۱۱ خط تعریف شده است و خط شمارهٔ ۸ به‌عنوان خط کرسی مشخص شده است. 