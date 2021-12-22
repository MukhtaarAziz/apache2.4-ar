# apache2.4-ar
Translate The Apache Server Documentation To the Arabic Language

## TOC
### 1- المقدمة
#### 1-1 العملاء، الخدم، الروابط 



## 1- المقدمة
ان كنت جديد على استخدام خادم الويب **apache** ، او حتى لو كنت تمتلك
موقع الكتروني، لربما لا تعرف اين تبدا او ماهي الاسئلة التي تسألها. لذا في هذه الصفحات
سوف تتعلم الاساسيات.

### 1-1 العملاء، الخدم، الروابط 
العناوين في عالم **الويب** تعبر بواسطة الروابط **URLs** 
وهي مختصر لـ **Uniform Resource Locators** 
والتي من خلالها يتم تحديد نوع البروتوكل (Protocol)
 (**http**) 
 واسم الخادم - servername (www.apache.org)
مسار-الرابط - URL-path __(كمثال: docs/current/getting-started.html)__
وكذلك نص-الاستعلام (**Query String**) مثلا 
(?arg=value)
والتي تستخدم لتمرير المزيد من البيانات (المعلومات) الى الخادم.

**العميل (Client)**:
قد يكون متصفح الويب يتصل باخادم وليكن خادم HTTP اباتشي
وباستخدام البرتوكول HTTP 
ينشئ طلب لمصدر (resource) 
باستخدام مسار-الرابط.

مسار-الرابط URL-path : 
لربما يمثل مجموعة من الاشياء الموجودة على الخادم، قد يكون
ملف HTML مثلا getting-started.html 


### 3-1 ملفات الاعدادات و التوجيهات
يستخدم الخادم-اباتشي ملفات نصية لتخزين الاعدادات، توجد هذه الملفات في مواقع مختلفة حسب طريقة
تنصيب الخادم. الاماكن الشائعة لهذه ملفات-الاعدادات يمكن الاطلاع عليها من خلال الموقع
[http://wiki.apache.org/httpd/DistrosDefaultLayout] (httpd wiki).
اذا قمت بتنصيب الخادم من الكود-المصدري فيكون الموقع الافتراضي لملفات الاعدادات هو 
/usr/local/apache2/conf . 
اسم ملف الاعدادات الرئيسي عادة يكون 
httpd.conf .
وهذا ايضا قد يتغير بالاعتماد على الجهة الموزعة  للخادم-اباتشي.

عادة مايتم تقسم ملف الاعدادات الى عدة ملفات  اصغر، لتسهيل عملية ادارة الاعدادات، 
ويتم تحميل هذه الملفات بواسطة التوجيه Include.
اسماء ومواقع هذه الملفات تتغير ايضا حسب الجهة الموزعة للخادم او طريقة التنصيب
تستطيع انت ايضا التعديل على اسماء ومواقع هذه الملفات بالطريقة التي تريدها.

 يتم اعداد الخادم من خلال وضع التوجيهات الاعادادت **Configuration Directives**
 داخل ملفات الاعدادات. 
 وتوجيه الاعداد: هو عبارة عن كلمة-مفتاحية **keyword** 
 متبوعة معامل واحد او اكثر **argument** 
 التي تحدد قيمة التوجيه.

 السوال يكون "اين اضع هذه توجيهات-الاعدادات؟" 
 والجواب عليه بشكل عام هو "اين تريد تأثير هذه التوجيه ان يعمل". 
 اذا كان تأثير هذا التوجيه عام (يشمل الخادم بشكل عام ) global setting  
 فيجب وضعه في ملف-الاعداد خارج كل من 
 ```<Directory>, <Location>, <VirtualHost>``` 
 اذا كان تأثير توجيه-الاعداد على مجلد معين فيجب وضعه داخل 
 ```<Directory>``` الذي ميثل المجلد المطلوب.. وهكذا 
 انتقل الى اقسام الاعدادات لمزيد من العلومات عن اقسام-الاعدادات
 
