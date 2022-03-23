# iranian-news-agencies-crawler
a crawler to fetch last news from Iranian(Persian) news agencies.
# دریافت اخرین اخبار خبرگزاری های ایران
این کتابخانه ماانند یک API  برای دریافت اخرین اخبار از خبرگزاری های مهم  فارسی زبان داخلی و خارجی است به زبان node.js که خبرگزاری های زیر را پشتیبانی می‌کند:



| نام خبرگزاری     | کلید |  لوگو |
| ---            | ---             | ---       |
| [خبرگزاری فارس](https://www.farsnews.ir/) |      fars       | ---       |
| [خبرگزاری ایرنا](https://www.irna.ir/) |      irna       | ---       |
| [باشگاه خبرنگاران جوان](https://www.yjc.news/) |     yjc        | ---       |
| [خبرگزاری ایسنا](https://www.isna.ir/) |   isna          | ---       |
| [خبرگزاری تسنیم](https://www.tasnimnews.com/) |   tasnim         | ---       |
| [بی بی سی](https://www.bbc.com/persian) |      bbc       | ---       |
| [خبرگزاری مهر](https://www.mehrnews.com/) |    mehr         | ---       |
| [خبرگزاری ایلنا](https://www.ilna.news/) |   ilna          | ---       |
| [خبرگزاری موج ](https://www.mojnews.com/) |     moj        | ---       |
| [خبرگزاری تابناک](https://www.tabnak.ir/) |    tabnak         | ---       |
| [خبرآنلاین](https://www.khabaronline.ir/) |     khabaronline        | ---       |
| [خبرگزاری برنا](https://www.borna.news/) |    borna         | ---       |
| [خبرگزاری آنا](https://www.ana.press/) |     ana        | ---       |
| [الف](https://www.alef.ir/) |     alef        | ---       |
| [خبرگزاری صداسیما](https://www.iribnews.ir/) |     irib        | ---       |
| [خبرگزاری sputnik](https://ir.sputniknews.com/) |     sputnik        | ---       |
| [خبرگزاری independent](https://www.independentpersian.com/) |    independent         | ---       |
| [VOA فارسی](https://ir.voanews.com/) |     voa        | ---       |



## نصب
```sh
npm i iranian-news-agencies-crawler
```

## نحوه استفاده 
```javascript
import fetchNews from 'iranian-news-agencies-crawler';
...
// دریافت عنواوین خبر بدون متن اصلی 
// تاخیر زیر ۱ ثانیه
var lastNews = await fetchNews('isna', { includeNewsText: false });
...

// دریافت عنواوین خبر به همراه متن اصلی 
// تاخیر بسته به نوع خبرگزاری و سرعت اینترنت سرور بین ۲ تا ۶ ثانیه
var lastNews = await fetchNews('fars', { includeNewsText: true });
...

```  

- پارامتر اول نام خبرگزاری است که در جدول بالا و در ستون کلید هر خبرگزاری درج شده است.
- بدیهی است که برای دریافت خبر های  خبرگزاری های خارج از ایران مثل بی بی سی VOA و independent باید سرور خارج از کشور باشد و در محیط لوکال VPN متصل باشد.
- با توجه با تاخیر ذکر شده توصیه میشود این کد به صورت یک task  با بازه زمانی مشخص اجرا شود.

> این کتاب خونه بسیار سادست و خودتون هم می‌تونید توسعش بدید ولی با این حال خوشحال می‌شم نظرو یا باگ های احتمالیش رو همینجا از طریق
 [`'گیت هاب'`](http://github.com/hamid) 
 و یا 
 [`توییتر`](https://twitter.com/hamid_salimian)
 بهم بگید. 😊😊
