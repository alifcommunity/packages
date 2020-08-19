 <div dir="RTL">
 
##### تحذير الحزمة تحت التطوير وغير جاهزة للأستخدام هذا الدليل للمطورين

## فلاتباك
بناء فلاتباك يساعد في تشغيل مترجم ألف في جميع التوزيعات 

### استنسخ المشروع
```bash
git clone git@github.com:aliflanguage/packages.git 
```
اضف في اخر السطر -b <اسم الفرع> حسب الفرع المرغوب 

### البناء 
```bash
cd flatpak
flatpak-builder build-dir org.alif.compiler.yml --ccache
```
### الإختبار 
يمكنك استخدام المترجم مباشرة
```bash
flatpak-builder --run build-dir org.alif.compiler.yml alif
```
او يمكنك الدخول مباشرة في البيئة 
```bash
flatpak-builder --run build-dir org.alif.compiler.yml bash
```

### التثبيت والتشغيل
```bash
flatpak-builder --user --install build-dir org.alif.compiler.yml
flatpak run org.alif.compiler
```
</div>
