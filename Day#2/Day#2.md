
 مفهوم (CLI)Command Line Interface

هي واجهة نصية تستخدم لتشغيل البرامج و إدارة ملفات الكمبيوتر و التفاعل مع الكمبيوتر.


أوامر CLI
أهم الأوامر المستخدمة في Command Line Interface
| وظيفة الأمر                                                                                      | Windows(command prompt) الأمر في نظام                  | Mac (terminal) الأمر في نظام         |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------ |
| عرض المسار الحالي                                                                                | cd                                                     | pwd                                  |
| الخروج من المجلدات                                                                               | cd ..                                                  | cd ..                                |
| إنشاء مجلد<br>ملاحظة: يمكنك استخدام علامة الاستفهام `?` إذا كان اسم الملف أو المجلد يحتوي مسافة. | mkdir folderName                                       | mkdir folderName                     |
| الدخول إلى المجلدات                                                                              | cd directoryName                                       | cd directoryName                     |
| إنشاء ملف نصي فارغ                                                                               | cd. > fileName.txt <br>OR <br>type nul >  fileName.txt | touch file.txt                       |
| عرض محتويات المجلد                                                                               | dir                                                    | ls                                   |
| عرض جميع محتويات المجلد بما فيها المحتويات المخفية                                               |                                                        | ls -a                                |
| الكتابة في ملف نصي                                                                               | echo My First File >> fileName.txt                     | echo "My First File” >> fileName.txt |
| عرض محتويات الملف النصي                                                                          | type fileName.txt                                      | cat fileName.txt                     |
| إزالة أي محتوى على نافذة الأوامر                                                                 | cls                                                    | clear                                |
| الدخول إلى مجلد المستخدم الحالي                                                                  |                                                        | cd ~                                 |
| فتح مجلد أو ملف                                                                                  | start                                                  | Open folderName/directoryName        |
| حذف ملف                                                                                          |                                                        | rm fileName                          |
| حذف مجلد                                                                                         |                                                        | rm -r directoryName                  |



مفهوم Version Control Systems


أنظمة التحكم بالنسخ 

أنظمة التحكم بالنسخ أو ماتسمى Version Control System هي أنظمة تقوم بإدارة وتتبّع مراحل تطوّر المشروع، بحيث يتم تسجيل أي تعديل سواء كان إضافة ملف جديد أو حذف أو تحديث ملف موجود مسبقًا في تاريخ المشروع منذ البداية. بعض أنواع أنظمة التحكم بالنسخ يساعدنا على تطوير المشاريع بشكل أسرع من خلال توفير الخدمات التي يحتاجها الفريق للعمل معًا. 


![](https://paper-attachments.dropbox.com/s_A62BAA18E072C17CB13B44953D7699BA7D20B7D65FF3A4EBD55A67B40379ED93_1659121313593_Screen+Shot+1443-12-30+at+10.01.22+PM.png)


أنظمة التحكم بالنسخ لها أنواع: 

- المركزيّة Centralized:

أنظمة التحكم بالنسخ المركزيّة وتعمل بالطريقة التالية:
توجد نسخة واحدة من المشروع مشتركة بين جميع أعضاء الفريق، لكن من سلبياتها أنها تحتوي على نقطة واحدة عند حصول الخطأ، أي أن نتيجة انقطاع الاتصال من الخادم الذي تم رفع المشروع عليه تعني انقطاع الاتصال لدى جميع أعضاء الفريق، بالتالي لايمكن لأي عضو الوصول للمشروع وتطويره خلال فترة الانقطاع.

![](https://paper-attachments.dropbox.com/s_A62BAA18E072C17CB13B44953D7699BA7D20B7D65FF3A4EBD55A67B40379ED93_1659121525078_Screen+Shot+1443-12-30+at+10.02.59+PM.png)



- الموزّعة Distributed: 

أنظمة التحكم بالنسخ الموزّعة وتعمل بالطريقة التالية:
توجد نسخة مشتركة بين جميع أعضاء الفريق مع وجود نسخة خاصة لكل عضو، بحيث يقوم كل عضو بإضافة تعديلاته على النسخة المحلية ومن ثم رفعها إلى النسخة المشتركة بحيث تصل التحديثات إلى جميع أعضاء الفريق.

![](https://paper-attachments.dropbox.com/s_A62BAA18E072C17CB13B44953D7699BA7D20B7D65FF3A4EBD55A67B40379ED93_1659121536393_Screen+Shot+1443-12-30+at+10.04.54+PM.png)




التعرف على نظام Git
ما هو Git؟

هو عبارة عن نظام ينتمي إلى أنظمة التحكم بالنسخ الموزّعة، أي أنه يقوم بتتبع وتسجيل التغييرات التي أجريت على الملفات، وطريقته في تتبع الملفات تكون عبر أخذ نسخ “snapshot” (تسمى أيضًا commits) من المشروع يحددها المستخدم فيقوم هذا النظام بحفظ التغييرات خطوة بخطوة مع التسلسل الزمني ويرفق وصفًا لكل خطوة من هذهِ التغييرات حتى يتمكن المستخدم من تتبعها والرجوع إليها بسهولة، وجميع التغييرات التي تحصل على المشروع يتم تخزينها في Repository أي مخزن أو مستودع.


تثبيت Git - أجهزة Windows

قبل أن نستطيع التعامل مع Git يجب علينا أولًا أن نقوم بتثبيته على أجهزتنا، لذلك قم بالدخول على موقع Git الرسمي من خلال هذا الرابط (https://git-scm.com/) والضغط على Download كما هو موضح في الصورة المرفقة:

![](https://paper-attachments.dropbox.com/s_83AF89E1934F15C9A9BAEE1A6EE76D5250AF8EAA839CEC4256BB4E08F52B1BEF_1627472481826_Screen+Shot+1442-12-18+at+2.40.26+PM.png)

تثبيت Git - أجهزة MacOS

يعتبر Git موجود مسبقًا على أجهزة MacOS بالتالي كل ما عليك عمله هو التحقق من وجوده من خلال استخدام الأمر  `git` `--``version`   في Terminal كالتالي:

![](https://paper-attachments.dropbox.com/s_83AF89E1934F15C9A9BAEE1A6EE76D5250AF8EAA839CEC4256BB4E08F52B1BEF_1627472609882_Screen+Shot+1442-12-18+at+2.43.27+PM.png)


في حالة ظهور النسخة، هذا يعني أن Git موجود لديك، وإن لم يكن موجود سيقوم Terminal بارشادك إلى ما يجب عمله لتنزيله. 




مفاهيم و أوامر Git

يوجد في Git العديد من المفاهيم والأوامر سنقوم في هذا الدرس بتغطية أكثر هذهِ المفاهيم شيوعًا.


الأمر `git init`

في Git جميع التعديلات يتم تخزينها في Repository لذلك إن أردنا تتبع مشروع ما باستخدام Git يجب علينا أولًا إنشاء هذا المخزن لتسجيل جميع التعديلات بداخله، وبمعنى آخر أي فريق يريد استخدام Git لتتبع المشروع الذي يتم العمل على تطويره يحتاج المخزن لتسجيل جميع التعديلات التي حدثت خلال رحلة تطوير المشروع.

خطوات إنشاء Repository: 

- فتح terminal أو command prompt.
- الوصول إلى المسار الذي يحتوي على المشروع الذي تريد تتبعه وإدارته.
- الدخول على المشروع. 
- استخدام الأمر  `git init`  الذي يقوم بإنشاء Repository جديد. 

الأمر المستخدم لإنشاء Repository هو: 

    git init

هذا الأمر سيقوم بإنشاء مجلد `git.` والذي يحتوي على جميع الملفات والمجلدات التي يحتاجها Git لتتبع المشروع. 


مفهوم Git Stages 

خلال العمل على المشروع والتطوير عليه، لابد من إنشاء ملفات، أو حذفها، أو التعديل عليها ولحفظ هذهِ التعديلات لابد من إعلام Git بأنه تم التعديل عليها وأنك تريد حفظها لأن Git لن يقوم بشكل تلقائي بحفظ هذهِ التعديلات على تاريخ المشروع، وقد تحتاج للتراجع عن التعديل لذلك وجد مفهوم Git Stages والذي ينص على أن الملفات في Git تمر بمراحل أو Stages كالتالي:

المرحلة الأولى Untracked

- تعني أن Git لا يقوم بتتبع الملفات إلى الآن ولم يخزنها في Repository.

المرحلة الثانية Staged وتسمى أيضًا tracked

- تعني أن Git يعلم بالتغييرات الحاصلة على الملف ويقوم بتتبعها لكن لم يقم بحفظها إلى الآن في Repository.

المرحلة الثالثة Committed 

- وتعني أن الملفات تم التعديل عليها وحفظها في تاريخ المشروع Repository.

يمكنك التفكير بالمراحل كمتجر الكعك، فعندما تريد أن تطلب كعكة يجب عليك أولًا اختيارها وتحديد ماتريد فتشابه هنا مرحلة untracked، بمعنى أنك لم تقم إلى الآن باختيار طلبك بالفعل، وبعد اختيارك يقوم الموظف بتغليفها مثل مرحلة staged لكن لن يقوم بتسليمها لك إلّا بعد تسجيل الفاتورة والدفع، وهذهِ تشابه مرحلة committed بحيث أنه تم تسجيل شرائك في قاعدة البيانات لديهم ويستطيعون العودة لتاريخ الشراء ومالذي قمت بشرائه في أي وقت.


أمر `git status` 

يساعدنا الأمر `git status` على معرفة حالة المشروع، فيزودنا بعدد من المعلومات مثل أسماء الملفات المتواجدة في مرحلة untracked ومرحلة staged. 

مثال:
قبل تطبيق أي أمر من أوامر Git على أحد المشاريع يجب أن يكون لدينا مجلد `git.` والذي يتم إنشاؤه من خلال الأمر `git init`، دعونا أولًا ننشئ مجلد جديد في `Desktop` كالتالي:


    > pwd
    /Users/user/Desktop

 
 بعد التأكد من تواجدنا في `Desktop` سنقوم بإنشاء المجلد الجديد وليكن بالاسم `git-test`:

    > git-test  

لنقم الآن بالدخول إليه واستخدام الأمر `ls` و  `ls -a` لعرض الملفات والمجلدات سواء كانت مخفيّة أم لا:

    > cd git-test
    > ls
    > ls -a

نلاحظ أن المجلد فارغ تمامًا، بمعنى أننا لم نقم بإنشاء Repository باستخدام الأمر `git init` بعد، لنقم باستخدام أمر  `git status`  للتحقق من أنه سيعمل دون تواجد Repository أم لا:

    > git status
    fatal: not a git repository (or any of the parent directories): .git

نتج عن الأمر رسالة خطأ كرد، والسبب هو عدم استخدامنا للأمر `git init` قبل استخدام الأمر، لذلك سنقوم باستخدامه الآن:

    > git init
    Initialized empty Git repository in /Users/user/Desktop/git-test/.git/

بعد إنشاء Repository نستطيع استخدام أوامر Git، لنقم باستخدام أمر `git status` مرة أخرى:

    > git status
    On branch master
    
    No commits yet
    
    nothing to commit (create/copy files and use "git add" to track)

بهذا الشكل يقوم الأمر `git status` بعرض حالة المشروع لنا. 


الأوامر المستخدمة: 

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627478352004_Screen+Shot+1442-12-18+at+4.19.07+PM.png)

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627478527138_Screen+Shot+1442-12-18+at+4.22.01+PM.png)

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627478506094_Screen+Shot+1442-12-18+at+4.21.42+PM.png)




أمر `git add` 

كما ذكرنا سابقًا، يوجد مراحل تمر فيها الملفات في Git، أحد هذهِ المراحل هي Untracked وتعني أن الملف لا يتم تتبعه، مثال بمجرّد إنشائك لملف جديد يعتبر الملف Untracked، لذلك إذا أردت أن يقوم Git بتتبعه يجب عليك نقله إلى المرحلة التالية وهي Staged، ويتم ذلك من خلال استخدام الأمر `git add` مع إرسال اسم الملف الذي تريد نقله، بالتالي نستخلص مما ذكر بأن الأمر `git add` يقوم بنقل الملفات من مرحلة Untracked إلى Staged.

مثال:

> ملاحظة: الأوامر في هذا المثال تابعة للأوامر المتواجدة أعلاه. 

لرؤية المراحل التي يمر بها الملف لنقم بإنشاء ملف جديد باستخدام الأمر `touch` كالتالي:

    > pwd
    /Users/user/Desktop/git-test
    > touch file.txt
    > ls
    file.txt

الآن بعدما تأكدنا من أنه تمّ إنشاء الملف بنجاح، لنقم بالاستعلام عن حالة المشروع من خلال استخدام الأمر `git status`:

    > git status
    On branch master
    
    No commits yet
    
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    file.txt
    
    nothing added to commit but untracked files present (use "git add" to track)

نلاحظ أنه قام بوضع الملف الجديد في مرحلة Untracked، وكما ذكرنا لتتبعه نستخدم الأمر `git add` كالتالي:


    > git add file.txt
    > git status
    On branch master
    
    No commits yet
    
    Changes to be committed:
      (use "git rm --cached <file>..." to unstage)
    new file:   file.txt

 بهذا الشكل قمنا بنقل الملف إلى المرحلة الأخرى وهي Staged/Tracked.


الأوامر المستخدمة:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627479217767_Screen+Shot+1442-12-18+at+4.33.35+PM.png)



نلاحظ الرسالة أعلاه، بأنه في حال أردت التراجع عن تتبع الملف يمكنك استخدام الأمر `git rm`، سنقوم باستخدامه ونرى ما سيحصل: 

    > git rm --cached file.txt
    rm 'file.txt'
    > git status
    On branch master
    
    No commits yet
    
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    file.txt
    
    nothing added to commit but untracked files present (use "git add" to track)

بهذا الشكل قمنا بإعادة الملف إلى مرحلة Untracked. 

الأوامر المستخدمة:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627479376321_Screen+Shot+1442-12-18+at+4.36.13+PM.png)



الأمر `git commit` 

يقوم هذا الأمر بنقل الملفات من مرحلة Staged إلى Committed.

مثال:
سنقوم أولًا بنقل الملف من مرحلة untracked إلى staged مرة أخرى كالتالي:

    > git add file.txt
    > git status
    On branch master
    
    No commits yet
    
    Changes to be committed:
      (use "git rm --cached <file>..." to unstage)
    new file:   file.txt

والآن سنقوم باستخدام الأمر `git commit` لنقل الملفات إلى مرحلة Committed، هذهِ العمليّة تسمى commit لكن يجب الأخذ بعين الاعتبار أننا نحتاج إلى رسالة commit، بحيث نصف فيها ما قمنا بالتعديل عليه كالتالي:


    > git commit -m "new file added"
    [master (root-commit) e4f436b] new file added
     1 file changed, 0 insertions(+), 0 deletions(-)
     create mode 100644 file.txt

الآن تم تخزين التعديلات التي قمنا بها (إنشاء ملف جديد) في Repository، وللتحقق من أنه لا يوجد تعديل آخر جديد سنقوم باستخدام الأمر `git status`.


    > git status
    On branch master
    nothing to commit, working tree clean


الأوامر المستخدمة:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627481607349_Screen+Shot+1442-12-18+at+5.13.24+PM.png)





الأمر `git log`  

يقوم هذا الأمر بعرض تاريخ التعديلات commit التي قمنا بها سابقًا.

مثال:

    > git log
    commit e4f436b662be5e7183351e1636a4d15faf6c274f (HEAD -> master)
    Author: dev <dev@test.com>
    Date:   Wed Jul 28 17:10:58 2021 +0300
    
        new file added

نلاحظ وجود عدد من المعلومات مع commit الذي قمنا به سابقًا، منها التاريخ والوقت، الرسالة الخاصة في commit، معلومات الشخص الذي قام بحفظ التعديلات مثل اسمه dev والايميل الخاص به، كما أنه أيضًا قام بإنشاء رقم hash لتحديد commit بحيث يدل كل hash على commit معيّن ولا مجال لتداخلهم. 


> ملاحظة: يستفيد Git من رقم hash لتحديد ما إذا تم التعديل على الملف أم لا، فأي تغيير على رقم hash هو دليل على تغيير محتوى الملف.



الأوامر المستخدمة:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627481670344_Screen+Shot+1442-12-18+at+5.14.27+PM.png)


لتغيير محتوى الرسالة يمكنك كتابة 

    > git commit --amend -m "last update"


الأمر `git log` `--``oneline` 

يقوم هذا الأمر بعرض تاريخ التعديلات commit التي قمنا بها سابقًا بشكل مختصر (في سطر واحد).

مثال:

    > git log --oneline
    e4f436b (HEAD -> master) new file added


الأوامر المستخدمة:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627482043279_Screen+Shot+1442-12-18+at+5.20.39+PM.png)




مفهوم branches

تعتبر الفروع أو Branches مسارات لتطوير المشروع، لنفترض أننا نريد التعديل على المشروع من خلال إضافة خاصية جديدة لكن لسنا متأكدين من فعاليتها أو إمكانيّة تطبيقها، بالتالي لا نريد أن نخاطر بالتعديل على المشروع الفعلي، من هنا أتت خاصية الفروع، بحيث نستطيع أخذ نسخة من المشروع للتجربة وإضافة الخصائص الجديدة من خلال إنشاء فرع جديد (مسار جديد للمشروع).



الأمر  `git branch`  

يستخدم هذا الأمر لعرض الفروع المتواجدة في المشروع.

مثال:

    > git branch
    * master

من المخرجات نلاحظ وجود فرع واحد يسمى master وهو الفرع التلقائي/ الرئيسي الخاص بالمشروع، كما نلاحظ وجود `*` وتعني أننا حاليًا متواجدين في master وأي تعديل أو إضافة حاصلة الآن ستكون في الفرع master. 



الأمر `<git branch <branchName`

هذا الأمر يقوم بإنشاء فرع جديد. 

مثال:

    > git branch test 
    > git branch
    * master
      test

نلاحظ أعلاه بأنه فعلًا تم إنشاء فرع جديد بالاسم test. 


الأمر  `git checkout`  
يقوم هذا الأمر بالانتقال إلى فرع آخر. 

مثال: 

    > git branch
    * master
      test

نلاحظ هنا أننا مازلنا على نفس الفرع وأي تعديل سيكون في master، بالتالي إن أردنا التعديل على الفرع الجديد يجب الانتقال له باستخدام الأمر `git checkout` كالتالي: 


    > git checkout test
    Switched to branch 'test'

بهذا الشكل أي تعديل يحصل الآن سيكون في فرع test، وللتأكد أكثر سنستخدم الأمر `git branch`  مرة أخرى.


    > git branch
      master
    * test

الأوامر المستخدمة:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627542795584_Screen+Shot+1442-12-19+at+10.13.11+AM.png)



مفهوم Merge

تطرقنا سابقًا إلى مفهوم الفروع، وذكرنا أنه يمكننا أخذ فرع من المسار الخاص بالمشروع والتعديل عليه كما نريد، لكن ماذا سنفعل عند نجاح الخاصية الجديدة؟ عند نجاح الخاصية سنقوم بدمجها مع المسار/الفرع الرئيسي للمشروع. 



الأمر `git merge`  

يستخدم الأمر `git merge`  لدمج الفروع مع بعضها. 
عند دمج مسار بآخر سينقسم الدمج إلى حالتين: 

- دمج fast forward: وهو الدمج الحاصل عندما تتم إضافة الخصائص في الفرع الجديد مع الفرع الرئيسي فقط.
- دمج مع conflict أو ما يسمى true merge، وهو ما يحدث عند ظهور تعارض conflict بسبب اختلاف نسخ المشروع، فعندما يقوم شخص بالتطوير على المسار الرئيسي وأنت لازلت تعمل على إضافة الخاصية في الفرع الخاص بك ومن ثم حاولت الدمج، سيظهر اختلاف بين النسختين وسيطالبك Git بحل هذا الاختلاف/التعارض.

مثال:
لنقم بالتعديل على الفرع test من خلال إنشاء ملف جديد فيه كالتالي: 

    > git branch
      master
    * test
    > touch new-file.txt

الآن بعد إنشاء الملف يجب أن يكون هذا الملف في مرحلة untracked ولنتحقق من ذلك سنقوم باستخدام الأمر `git status` كالتالي:

    > git status
    On branch test
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    new-file.txt
    
    nothing added to commit but untracked files present (use "git add" to track)

لنقم الآن بنقل الملف إلى مرحلة staged من ثم committed بحيث يزيد بعدد commit واحد عن الفرع الرئيسي(master):

    > git add new-file.txt
    > git commit -m "new-file.txt added to test branch"
    [test 52fa698] new-file.txt added to test branch
     1 file changed, 0 insertions(+), 0 deletions(-)
     create mode 100644 new-file.txt
    > ls
    file.txt new-file.txt

نلاحظ الآن أنه أصبح لدينا ملفان في فرع test وبعد أن قمنا بحفظ التعديلات سننتقل لفرع master ونرى عدد الملفات هناك كالتالي:

    > git branch
      master
    * test
    > git checkout master                              
    Switched to branch 'master'
    > ls
    file.txt

نلاحظ أنه في الفرع master يوجد ملف واحد فقط، والسبب أن الملف الثاني تم إنشاؤه في الفرع test، بالتالي سنقوم بدمج الفرع test مع master لجلب التحديثات الخاصة بالفرع test في المسار الرئيسي باستخدام `git merge` :

    > git merge test
    Updating e4f436b..52fa698
    Fast-forward
     new-file.txt | 0
     1 file changed, 0 insertions(+), 0 deletions(-)
     create mode 100644 new-file.txt

الآن لنتحقق من عدد الملفات باستخدام الأمر ls:

    > ls
    file.txt new-file.txt

بالتالي نلاحظ أنه بالفعل تم دمج الفرع test مع master.

الأوامر المستخدمة:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627546385805_Screen+Shot+1442-12-19+at+11.13.02+AM.png)

----------


التعريف بمنصة GitHub 

تعرفنا سابقًا على برنامج git وعلى أهميته في حفظ نسخ المشاريع وتتبعها والوصول إليها بكل سهولة، لكن ماذا لو أننا فقدنا جهازنا الشخصي أو احتجنا للوصول إلى `Repository` المشروع في وقت لم يكن جهازنا برفقتنا، كيف سنقوم بذلك؟ هنا يأتي دور منصة GitHub وغيرها من المنصات المشابهة والتي تقوم بحفظ نسخة من `Repository` المشروع على الإنترنت حتى تستطيع الوصول لها من أي جهاز أو مكان متصل بالإنترنت. 

تسجيل حساب في gitHub

لإنشاء حساب على منصة GitHub من الرابط التالي:  https://github.com/join  

ملاحظة: GitHub هي المنصة الأشهر لحفظ ومشاركة المشاريع أما بالنسبة git فهو النظام الذي يقوم بالتحكم بالنسخ.


إنشاء Repository على GitHub

بعد أن أتممنا عملية التسجيل في موقع gitHub وقمنا بتسجيل الدخول، سنقوم بإنشاء مستودع repository جديد
لإنشاء مشروع جديد نقوم  بالنقر على علامة الزائد الموجودة على في الجزء العلوي من الصفحة، ثم نقوم باختيار New repository.


![](https://paper-attachments.dropbox.com/s_98A95AE7D23EFA3A27E978536B3E2F3AEDFF6B38471F57E7EF9893D54AF9EC3E_1587990282429_1.jpg)


ثم سننتقل للصفحة التالية وهي الصفحة الخاصة بإنشاء المستودع repository:

![](https://paper-attachments.dropbox.com/s_98A95AE7D23EFA3A27E978536B3E2F3AEDFF6B38471F57E7EF9893D54AF9EC3E_1588503119416_Screen+Shot+1441-09-10+at+1.50.21+PM.png)


والآن يمكننا إدخال اسم مشروع من اختيارنا في الخانة Repository name، قمنا باختيار الاسم `my-app`
لهذا المشروع وقمنا باختيار Public لجعل مشروعنا عام، وأخيرًا سنقوم بالنقر على زر Create repository لإتمام عملية الإنشاء، ستظهر لنا ثلاث خيارات أو مسارات يمكننا اتباعها لربط المستودع remote repository بالملف local file:

![](https://paper-attachments.dropbox.com/s_98A95AE7D23EFA3A27E978536B3E2F3AEDFF6B38471F57E7EF9893D54AF9EC3E_1588503154615_Screen+Shot+1441-09-10+at+1.48.17+PM.png)




الأمر  `git remote`  

يسمح لك هذا الأمر باستعراض remote المتواجد في المشروع الخاص بك، ويستخدم لتحديد موقع Repository الخاص بك في Github أو أي منصة أخرى. 

مثال:

    git remote


> ملاحظة: من الممكن أن يشير remote إلى موقع مشروع آخر في الجهاز ولا يشترط أن يؤشر على موقع Repository في أحد المنصّات.



الأمر  `git remote add`  

يسمح لك هذا الأمر بإنشاء remote بحيث يقوم برفع المشروع المحلّي الخاص بك إلى المشروع الموجود على internet.


مثال:
لإنشاء repository محلي ومن ثم رفعه على Github باستخدام الأمر `git remote add` :

    git remote add origin https://github.com/Mohammad-Ahmed/my-app.git






الأمر  `git push`  

يقوم هذا الأمر بإرسال التغييرات التي أجريت ورفعها إلى Repository محدد.


    git push <remote name> <branch name>

حيث تمثل `<``remote` `name``>`  الاسم أو المؤشر المعطى للمستودع الموجود على الإنترنت ويمثل  `<``branch name``>`  اسم الفرع الخاص به.


الأمر  `git pull`  

يجلب هذا الأمر ويدمج التغييرات من Repository المطلوب.


    git pull <variable name> <branch name>

حيث تمثل `<``remote` `name``>`  الاسم أو المؤشر المعطى للمستودع الموجود على الإنترنت ويمثل  `<``branch name``>`  اسم الفرع الخاص به.

تنبيه: عملية pull تقوم بدمج ملفات المستودع الموجودة على الإنترنت بالمستودع المحلي فيجب أن نقوم بعملية commit للتغييرات التي قمنا بها أولًا، ثم بعد ذلك نقوم  بعملية السحب pull حتى لا تتأثر التغييرات التي قمنا بها على النسخة المحلية.


الأمر  `git clone`  

يمكننا هذا الأمر من نسخ مشروع  Repository متواجد مثلًا على Github.

مثال:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627547420939_Screen+Shot+1442-12-19+at+11.30.17+AM.png)


لدينا أعلاه مشروع متواجد على Github، لنفرض أننا نريد استنساخ المشروع والعمل عليه، لذلك سنستخدم الأمر `git clone`  من خلال نسخ الرابط كالتالي:

![](https://paper-attachments.dropbox.com/s_50BAA5CA6C0DF0F94B919A672F50C5AB4C5272A84198C5100FA61C5B393E43CC_1627547559332_Screen+Shot+1442-12-19+at+11.31.52+AM.png)


بعد نسخ الرابط سنقوم بالذهاب إلى terminal والذهاب إلى المسار الذي نريد وضع المشروع به، من ثم استخدام الأمر `git clone`  كالتالي:


    git clone https://github.com/nodejs/node.git

بهذا الشكل أصبح لدينا مشروع. 



