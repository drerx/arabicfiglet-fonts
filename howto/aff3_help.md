راهنمای طراحی قلم در قالب AFF3
---
در این سند قرار است یک راهنمایی برای گنجاندن قلم آراسته در قالب AFF3 (Araste Font File v3) آورده شود. سعی بر این خواهد بود که این راهنمایی در حد امکان به زبان ساده باشد.

# مراحل طراحی یک قلم
البته که طراحی یک قلم یک کار هنری است و همه چیز بستگی به خود شما دارد. اما اینجا یک پیشنهاد برای پرهیز از مشکلات فنی آورده می‌شود.

## تعیین ارتفاع نویسه‌ها

برای طراحی قلم بهتر است در مرحلهٔ اول ارتفاع نویسه‌ها را تعیین کنید. با توجه به این که ارتفاع همهٔ نویسه‌ها باید باهم برابر باشند پس بهتر است در همان آغاز کار یک ارتفاع مناسب در نظر بگیرید.

ارتفاع یعنی تعداد خطوطی که برای چاپ آن نویسه لازم است. برای مثال در نویسهٔ زیر که حرف «`ب`» فارسی در حالت مستقل (بدون این که به حرف دیگری بچسبد) را نمایش می‌دهد، ارتفاع نویسه برابر ۶ خط است.

دقت کنید که این ارتفاع شامل خط‌های خالی هم می‌شود.

```


\_________/

     *
    
```


### مشخص کردن ارتفاع گلیف‌ها

در قلم AFF3 ارتفاع گلیف‌ها در سرآیند قلم تعیین می‌شود. این مقدار را تنظیم کنید.


سرآیند قلم به شکل زیر است:
```
aff3 A B C D E F
```


اولین عدد در این سرآیند یعنی `A` ارتفاع گلیف‌ها را تعیین می‌کند.


## تعیین خط کرسی

مسئلهٔ مهم دیگر خط کرسی است. فرض کنید نویسه‌ها قرار است روی یک خط کرسی ترسیم شوند. اگر خط کرسی را رعایت نکنید ممکن است نویسه‌ها بالاتر یا پایین‌تر از خط ترسیم شوند.

برای مثال در نویسه‌های پایین، سومین خط نویسه روی خط کرسی قرار دارد.

این گلیف‌ها به‌ترتیب نویسه‌های «ـب» در حالت پایانی (حالتی که از سمت راست به نویسهٔ دیگری می‌چسبد  از سمت چپ به چیزی نمی‌چسبد) و «تـ» در حالت اولیه (حالتی که از سمت راست به چیزی نمی‌چسبد و از سمت چپ به نویسهٔ بعدی خود می‌چسبد) را نمایش می‌دهند.


```


\_________|

     *
    
```

```
   * *

_______/


    
```

با توجه به این که خط کرسی در هر دوی این‌ها در خط سوم قرار دارد، این نویسه‌ها به‌درستی به هم می‌چسبند و واژهٔ «تب» را مثل شکل زیر می‌سازند:

```
              * *
           
\_________|_______/
           
     *     
               
```

حالا ببینیم اگر خط کرسی را کمی تغییر دهیم چه می‌شود. مثلاً در مثال پایین خط کرسی را برای نویسهٔ «ب» روی خط ۱ آورده‌ایم.

```
\_________|

     *


    
```

حال واژهٔ «تب» به شکل زیر درمی‌آید:
```
\_________|   * *
           
     *     _______/
           
           
        
```

مشخص است که این نتیجه بسیار بد شده است! دلیل آن مشخص است. نویسهٔ «ب» بالاتر از جایی که باید به نمایش درآمده است.


خط کرسی هم مشابه ارتفاع گلیف‌ها باید در همان ابتدای طراحی قلم مشخص شود و در طول طراحی قلم ثابت ماندن آن رعایت شود.

### مشخص کردن خط کرسی

در قلم AFF3 ارتفاع گلیف‌ها در سرآیند قلم تعیین می‌شود. این مقدار را تنظیم کنید.


سرآیند قلم به شکل زیر است:
```
aff3 A B C D E F
```


دومین عدد در این سرآیند یعنی `B` ارتفاع گلیف‌ها را تعیین می‌کند.


## تنوع‌های یک گلیف
در دبیرهٔ فارسی هر حرف الفبا به چند شکل مختلف نوشته می‌شود. این شکل‌ها بسته به این که حرف در کجای یک واژه و در کنار چه حروف دیگری قرار دارد تعیین می‌شود. برای مثال حرف «ع» (عین) می‌تواند به چهار حالت «عــ»، «ــعــ»، «ــع» و «ع» نوشته شود. این‌ها اسم‌های متفاوتی دارند. گاهی به‌ترتیب این اسم‌ها را «اول»، «وسط»، «آخر چسبان» و «آخر تنها» می‌نامیم. گاهی هم آن‌ها را به‌ترتیب «شکل آغازین»، «شکل میانی»، «شکل پایانی» و «مستقل» می‌نامیم.

در قلم آراسته به هر یک از این تنوع‌ها یک عدد نسبت داده شده است که به ترتیب از 1 تا 4 هستند. یعنی این گونه:


| ترتیب | کد | اسم | اسم دیگر | مثال |
|---|---|---|---|---|
| ۱  | 1  | اول  | شکل آغازین  | عـــ  |
| ۲  |  2 |  وسط | شکل میانی  | ــعــ  |
| ۳  |  3 | آخر چسبان  |  شکل پایانی | ـــع  |
| ۴  |  4 |  آخر تنها |  شکل مستقل | ع  |

همچنین وقتی که تنوع یک نویسه مهم نباشد، مثلاً وقتی که یک نویسهٔ لاتین استفاده می‌کنید، می‌توانید کد تنوع را برابر 0 بگذارید. کد 0 یعنی این شکل از نویسه مستقل از محل آن در واژه یا نویسه‌های همسایهٔ آن است.


### نکته‌ای دربارهٔ استفادهٔ نرم‌افزار از تنوع‌ها

از نرم‌افزاری مثل «_آراسته_» که از قلم‌های AFF3 استفاده می‌کند انتظار می‌رود در استفاده از این تنوع‌ها اولویت مشخصی را رعایت کند. این اولویت چنین است:

1. در صورتی که برای یک نویسه با کد مشخص، گلیفی با همان کد تعریف شده است، باید همان گلیف استفاده شود.
2. در صورتی که برای یک نویسه با کد مشخص، گلیفی با همان کد تعریف نشده است، باید گلیفی استفاده شود که بیشترین شباهت از نظر تنوع به آن را دارد. بیشترین شباهت برای هر تنوع در زیر آمده است:
	1. برای کد 1 بیشترین شباهت‌ها حالت‌های 2 و 4 هستند.
	2. برای کد 2 بیشترین شباهت‌ها حالت‌های 1 و 3 هستند.
	3. برای کد 3 بیشترین شباهت‌ها حالت‌های 2 و 4 هستند.
	4. برای کد 4 بیشترین شباهت‌ها حالت‌های 1 و 3 هستند.
3. در صورتی که نه تنوع موردنظر گلیف موجود باشد و نه تنوع شبیه به آن، برنامه می‌تواند از تنوع با کد 0 (مستقل از تنوع) استفاده کند.


### مشخص کردن تنوع‌ها

ساختار فایل AFF3 از یک سرآیند، چند خط کامنت و تعدادی بلوک تشکیل شده است. هر بلوک هم به‌نوبهٔ خود از ۲ خط سرآیند و چند خط که اطلاعات گلیف را در خود دارد تشکیل می‌شود. ساختار یک بلوک مانند شکل زیر است:

```
A
B C
L1
L2
...
Ln
```

دو خط اول این فایل که پارامترهای `A`، `B` و `C` را در خود جای داده‌اند، سرآیندها هستند.

خط‌های بعدی ترسیم گلیف هستند.

پارامترهای سرآیندهای یک بلوک مشخص کنندهٔ نویسه، تنوع گلیف و سویهٔ نویسه هستند.

#### پارامتر نویسه

پارامتر `A` نویسه را در خود جای می‌دهد. برای مثال اگر این بلوک یک گلیف برای حرف «`م`» است، پارامتر `A` برابر با `م` خواهد بود. یعنی خط اول سرآیند به شکل زیر است:

```
م
```


#### پارامتر تنوع نویسه

پارامتر `B` تنوع نویسه را تعیین می‌کند. برای تعیین آن مقدار کد تنوع نویسه را در این پارامتر جایگذاری کنید. مثلاً اگر این نویسه در حالت مستقل است مقدار `B` را برابر `4` قرار دهید یا اگر این نویسه تنوع ندارد مقدار آن را برابر `0` بگذارید.

#### پارامتر سویهٔ نویسه

همان‌طور که می‌دانید قلم‌های آراسته امکان ذخیرهٔ گلیف‌ها و نویسه‌ها از سویه‌های مختلف را به‌شکل هم‌زمان دارند. یعنی می‌توان در آن‌ها هم نویسه‌های راست‌به‌چپ مربوط به دبیره عربی را جای داد و هم نویسه‌های چپ‌به‌راست دبیرهٔ انگلیسی را.

سویهٔ نویسه با یک کد عددی از 0 تا 2 مشخص می‌شود که به شرح زیر است:

| ردیف | کد | اسم | مثال |
|---|---|---|---|
| ۱ | 0 | بدون سویه.| برای نویسه‌هایی مانند فاصله یا علایم نگارشی مثل نقطه که باید مستقل از سویه باشند. |
| ۲ | 1 | راست‌به‌چپ | برای نویسه‌های دبیرهٔ عربی. مثل همهٔ نویسه‌های فارسی. در همهٔ تنوع‌ها. هم‌چنین علایم نگارشی جهت‌دار مثل علامت سؤال فارسی |
| ۳ | 2 | چپ‌به‌راست | برای نویسه‌های دبیرهٔ لاتین. مثل همهٔ نویسه‌های انگلیسی. |

#### مشخص کردن سرآیند یک گلیف

می‌توانیم یک مثال را بررسی کنیم. در مثال پیشین که مربوط به نویسهٔ `م` در تنوع مستقل است سرآیند را مشخص می‌کنیم. دقت کنید که سویهٔ این نویسه راست‌به‌چپ است. سرآیند به شکل زیر خواهد بود:

```
م
4 1
```


## نکته‌های طراحی یک گلیف

حال که همهٔ بخش‌های سرآیند مشخص شده‌اند می‌توانیم یک گلیف را طراحی کنیم. هر گلیف از تعداد ثابتی خط تشکیل شده است که یکی از آن‌ها خط کرسی است.

برای ترسیم، محتوای هر خط را در آن خط جایگذاری کنید. انتهای خط لازم نیست چیز خاصی بگذارید. فقط enter بزنید و به خط بعدی بروید.

تنها نکتهٔ مهم در اینجا خط کرسی است. انتظار می‌رود نرم‌افزارهایی مثل _آراسته_ که از قلم AFF3 استفاده می‌کنند، طول یک نویسه را بر حسب خط کرسی تعیین کنند. یعنی مثلاً اگر در خط کرسی ۶ نویسه وجود داشته باشد، نرم‌افزار باید طول این گلیف را هم ۶ در نظر بگیرد.

این نکته هنگامی اهمّیّت می‌یابد که بخشی از گلیف شما قرار است عقب‌تر از محل آغاز گلیف برود و در بالا یا پایین گلیف قبلی خود قرار بگیرد. به عنوان مثال گلیف زیر که برای حرف «`ک`» با تنوع 1 (در حالت آغازین) است را ببینید:

```
..........████████
.......███
....███
.......██
........██
█████████
.
.
```


فرض کنید که خط کرسی روی خط ۶ قرار دارد.

حال اگر این نویسه قرار باشد پس از گلیف دیگری بیاید، بخش بالایی آن یعنی سرکش حرف ک به گلیف قبلی خود خواهد چسبید چرا که از ابتدای خط کرسی عقب‌تر رفته است. برای برطرف کردن این مسئله باید در بخش خط کرسی به تعداد لازم نویسهٔ خالی (مثل نویسهٔ فاصله (` `) در بیشتر قلم‌ها یا در این مثال نویسهٔ نقطه (`.`) اضافه کنید. یعنی مثل این:

```
..........████████
.......███
....███
.......██
........██
█████████.........
.
.
```

در این صورت نرم‌افزار طول آن نویسه را جوری در نظر می‌گیرد که این گلیف به گلیف قبلی خود نچسبد.

# طراحی‌های پیشرفته‌تر

حال که طراحی یک قلم را یاد گرفته‌اید می‌توانید قلم‌های پیشرفته‌تری را طراحی کنید.

## طراحی قلم دوسویه

## طراحی قلم‌های متغیر

## طراحی علایم نگارشی