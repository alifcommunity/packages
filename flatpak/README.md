 <div dir="RTL">
 
##### تحذير الحزمة تحت التطوير وغير جاهزة للأستخدام هذا الدليل للمطورين

## فلاتباك
بناء فلاتباك يساعد في تشغيل مترجم ألف في جميع التوزيعات 

### استنسخ المشروع
```bash
git clone git@github.com:aliflanguage/packages.git 
cd packages
git submodule update --init --recursive
```
اضف في اخر السطر -b <اسم الفرع> حسب الفرع المرغوب 

### البناء 
```bash
cd flatpak
flatpak-builder build-dir org.alif.lang.yml --ccache
```
### الإختبار 
استخدام المترجم مباشرة
```bash
flatpak-builder --run build-dir org.alif.lang.yml alif
```
او الدخول مباشرة في البيئة 
```bash
flatpak-builder --run build-dir org.alif.lang.yml bash
```

### التثبيت والتشغيل
```bash
flatpak-builder --user --install build-dir org.alif.lang.yml --ccache
flatpak run --devel org.alif.lang
```
</div>
