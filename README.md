# software-engineering-lab-a1

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
