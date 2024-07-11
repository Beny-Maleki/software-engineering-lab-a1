# software-engineering-lab-a1

<div dir='rtl'>

  

نکات مربوط به انجام آزمایش:

-
Github actions & pages:
برای استقرار فایل html استاتیک خود بر روی GitHub pages ابتدا فایل deploy.yml را به مسیر .github/workfloاضافه می‌کنیم. پس از آن فایل ما در آدرسی که در منوی settings->pages آمده است serve می‌شود

-
Making a ruleset:
برای اضافه کردن rule  مربوط به بستن کامیت مستقیم به main، از طریق settings وارد منوی rules می‌شویم و یک ruleset جدید برای default branch درست می‌کنیم و تیک‌های مربوط به بستن دسترسی‌ها به آن را می‌زنیم.

-
Merge conflicts:
برای ایجاد یک conflict تنها کافی است سعی کنیم برنچی را  به برنچ دیگر مرج کنیم که در برنچ دوم تغییرات روی خطوطی هستند که در برنچ اول هم وجود دارد. در واقع هنگامی که سعی کنیم این مرج را انجام دهیم، گیت تمام خطوطی که نتوانسته مرج را انجام دهد به ما نشان داده و در همان فایل قرار می‌دهد و در این حال  باید conflict ها را رفع کنیم که برای این کار معمولا از ابزارهایی مانند VSC استفاده می‌شود که merge conflict را راحت می‌کنند.
  
پرسش‌ها:

۱. پوشه .git جایی است که Git ابرداده (metadata) و پایگاه داده شیء (object storage) را برای پروژه شما ذخیره می کند. این مهمترین بخش Git است و وقتی یک مخزن را از کامپیوتر دیگری clone می کنید، کپی می شود.
این پوشه با دستور ```git init``` ایجاد می‌شود.

https://git-scm.com/book/en/v2/Getting-Started-What-is-Git

۲. کامیت اتمی، کامیتی است که شامل یک واحد کار  کامل و منسجم است. باید بتواند به تنهایی کار کند، یعنی بدون اینکه به کامیت‌های دیگر وابسته باشد یا بر آن تأثیر بگذارد اعمال شود. همچنین باید پیامی واضح و توصیفی داشته باشد که تغییرات ایجاد شده را خلاصه کند.

یک کامیت اتمی لزوماً به معنای کامیت کوچک نیست. این می تواند شامل چندین فایل یا خط کد باشد، به شرطی که به یک وظیفه یا ویژگی مرتبط باشند. نکته کلیدی این است که مطمئن شوید هر کامیت یک کار و فقط یک کار را انجام می دهد.

https://dev.to/this-is-learning/the-power-of-atomic-commits-in-git-how-and-why-to-do-it-54mn#

یک pull-request اتمی، شامل همه‌ی تغییرات مشابه هم است، در یک pull-request. مانند یک کامیت اتمی، یک pull-request اتمی هم باید تنها مربوط به یک ویژگی یا وظیفه باشد.

https://linearb.io/blog/pull-request-best-practices-our-tips

۳. تفاوت اصلی بین git fetch و pull در این است که git pull تغییرات را از یک مخزن remote مستقیما داخل working directory کپی می‌کند در حالی که fetch این کار را نمی‌کند. git fetch فقط تغییرات را داخل مخزن محلی کپی می‌کند. اما git pull هر دوی این کارها را انجام می‌دهد.

https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Git-pull-vs-fetch-Whats-the-difference#:~:text=Difference%20between%20Git%20fetch%20and,git%20pull%20command%20does%20both.

 عملیات rebase، کامیت‌ها را مجددا در بالای یک شاخه اعمال می‌کند، در حالی که merge، تاریخجه‌ی توسعه دو یا چند شاخه را با یکدیگر ادغام می‌کند. 
به بیان دیگر، تفاوت اصلی بین merge و rebase، ای است که merge تاریخچه را حفظ می‌کند و rebase آن را بازنویسی می‌کند.

https://blog.git-init.com/differences-between-git-merge-and-rebase-and-why-you-should-care/


عملیات Cherry-picking در Git به معنای انتخاب یک commit از یک شاخه و اعمال آن در شاخه دیگر است.
این در تضاد با روش‌های دیگری مانند merge و rebase است که معمولاً بسیاری از commit‌ها را در شاخه دیگری اعمال می‌کنند.

https://stackoverflow.com/questions/9339429/what-does-cherry-picking-a-commit-with-git-mean
  
  
۴. دستور git checkout برای وقتی استفاده می‌شود که می‌خواهیم تغییرات را در working directory 
دور بیاندازیم.

دستور git reset وقتی استفاده می‌شود که می‌خواهیم یک فایل را unstage کنیم و تغییراتمان را به working directory برگردانیم.
این دستور می‌تواند به قصد حذف کردن commitها از مخن محلی نیز به کار رود.

دستور git revert  موقعی استفاده می‌شود که می‌خواهیم commitها را از مخن remote  حذف کنیم. 
که این کار را با ساخت یک کامیت دیگر که تغییرات یک کامیت دیگر را undo می‌کند انجام می‌دهیم.


دستور git restore در واقع فایل‌هایی که در working tree هستند را از یک index یا یک commit دیگر بازیابی می‌کند. این دستور شاخه را آپدیت نمی‌کند. 


https://www.geeksforgeeks.org/git-difference-between-git-revert-checkout-and-reset/

https://blog.git-init.com/how-to-undo-changes-in-git-using-reset-revert-and-restore/


۵. استیج کردن به معنای نهایی کردن بخشی از/تمام تغییرات انجام‌شده بر روی پروژه نسبت به آخرین کامیت برنچ فعال است. در اصل فرضاً ممکن است که یک فایلی را به گیت  اضافه کنیم ولی صرفاً قسمتی از آن تغییرات کامل باشد و بخواهیم فقط همان را کامیت کنیم.

https://softwareengineering.stackexchange.com/questions/119782/what-does-stage-mean-in-git


اغلب، زمانی که روی بخشی از پروژه خود کار می کنیم، همه چیز به‌هم‌ریخته است. و گاهی می‌خواهیم برای مدتی شاخه خود راعوض کنیم تا روی چیز دیگری کار کنیم. مشکل این است که ما نمی‌خواهیم یک کار نیمه تمام را کامیت کنیم تا بتوانیم بعداً به این نقطه بازگردیم. برای این منظور می‌توانیم از دستور git stash استفاده کنیم.

دستور Stash حالت به‌هم‌ریخته working directory ما را می گیرد؛ یعنی فایل‌های ردیابی‌شونده اصلاح شده و تغییرات stage شده، را می‌گیرد و  آن‌ها را در پشته ای از‌ تغییرات ناتمام ذخیره می‌کند که می توانید هر زمان که بخواهید مجدداً اعمال کنید (حتی در یک شاخه دیگر).

https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning


۶. در مخازن گیت ساختاری که فایل‌ها ذحیره می‌شوند به این صورت است که برای هر فایل یک 
blob object
نگهداری می‌کند که محتوای فایل اصلی را در خود دارد. هنگامی که در ویرایشگر یک فایل را تغییر می‌دهیم گیت متوجه این تغییر در 
blob 
مربوطه می‌شود و آن را دنبال می‌کند. از طرفی ساختار پوشه‌ها به کمک 
tree
ساخته می‌شود. به این صورت که هر 
tree
نشان‌دهنده‌ی یک پوشه است و به تعدادی 
tree
یا
blob 
اشاره می‌کند. 
treeهایی
که یک 
tree
پدر به آن اشاره می‌کند، در عمل زیرپوشه‌ی آن پوشه‌ی پدر هستند.
در نهایت هر 
commit
یک تصویر از وضعیت 
object model
کل 
working directory
ما است. به این معنا که نشان می‌دهد وضعیت هر کدام از 
treeها
و
blobهای 
ما در آن لحظه از زمان که این تصویر گرفته شده به چه صورت بوده است.

![Alt text](https://github.blog/wp-content/uploads/2020/12/commit.png?resize=399%2C268?w=399)

در عکس بالا مثلث‌ها 
tree
مربع‌ها 
blob
و
دایره‌ها
commitها 
هستند که در عمل 
snapshotهایی
از وضعیت کل 
object model
در یک لحظه هستند.


https://github.blog/2020-12-17-commits-are-snapshots-not-diffs/


۷. 
در گیت به طور کلی دو مدل مخزن دارد:
- مخزن remote: که روی یک سرور میزبانی می‌شود (که می‌تواند از طریق اینترنت یاشبکه داخلی در دسترس باشد) و بین اعضای مختلف تیم به اشتراک گذاشته می‌شود.
- مخزن local: که روی کامپیوتر شخصی هر نفر از اعضای تیم میزبانی می‌شود و برای استفاده همان نفر است.

https://nulab.com/learn/software-development/git-tutorial/git-basics/repositories/remote-repositories-vs-local-repositories/
