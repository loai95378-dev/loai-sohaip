
# Project Title

 
 
 

مشروع استكشافي في عالم *Flutter* يركز على فهم المكونات (Widgets) وإدارة الحالة (State Management) والتعامل مع الواجهات الرسومية. الهدف منه هو بناء تطبيق تجريبي يوضح قوة ومرونة *Flutter* في إنشاء تجارب مستخدم متميزة.


## 🚀 About Me
"أنا مطور متكامل بخبرة في صياغة التجارب الرقمية المتكاملة، بدءًا من الهيكل وصولاً إلى النشر,الهدف منه بناء تطبيق تجريبي يوضح قوة ومرونة المشروع باستخدام فلاتر في إنشاء واجهات تفاعلية ومرنة. أبحث دائمًا عن التحدي التقني وتطبيق أفضل الممارسات.


## Installation

## 🛠️ التقنيات المستخدمة (Tech Stack)

| التقنية / الأداة | الغرض |
|---|---|
| Flutter (فلاتر) | إطار العمل الأساسي لبناء تطبيقات الهواتف الذكية (Android و iOS) وغيرها من المنصات بواجهة مستخدم واحدة. |
| Dart (دارت) | لغة البرمجة المستخدمة لكتابة كود فلاتر، وهي سريعة وموجهة للكائنات. |
| Provider / Bloc (لإدارة الحالة) | أدوات أساسية لإدارة بيانات التطبيق وضمان تحديث الواجهات بشكل فعال ومنظم. |
| Firebase (خدمات جوجل) | استخدام خدمات مثل قواعد البيانات في الوقت الفعلي أو المصادقة أو التخزين السحابي للتطبيق.
## Usage/Examples

import 'package:flutter/material.dart';

void main() {
  runApp(const PhishingApp());
}

class PhishingApp extends StatelessWidget {
  const PhishingApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Phishing Detector - Single Page',
      theme: ThemeData(primarySwatch: Colors.blue),
      home: const SinglePageHome(),
      debugShowCheckedModeBanner: false,
    );
  }
}

/* ===========================
   SinglePageHome: صفحة واحدة تحتوي
   - إدخال الرابط
   - منطقة عرض النتائج (تتغير حسب الحالة)
   =========================== */
class SinglePageHome extends StatefulWidget {
  const SinglePageHome({super.key});

  @override
  State<SinglePageHome> createState() => _SinglePageHomeState();
}

class _SinglePageHomeState extends State<SinglePageHome> {
  final TextEditingController _controller = TextEditingController();
  AnalysisResult? _lastResult;
  String? _lastUrl;

  void _runAnalysis() {
    final raw = _controller.text.trim();
    if (raw.isEmpty) {
      // حالة الحقل الفارغ
      setState(() {
        _lastResult = null;
        _lastUrl = null;
      });
      _showEmptyDialog();
      return;
    }

    final url = _normalizeUrl(raw);
    final analysis = LinkAnalyzer.analyze(url);

    setState(() {
      _lastUrl = url;
      _lastResult = analysis;
    });
  }

## Used By

* *[@loay-suhaib]* (https://github.com/loay-suhaib)
* *[@sara-Marish]* (https://github.com/sara-Marish)

👥 المساهمون والمطورون (Contributors)

نقدر جهود كل من ساهم في بناء وتطوير هذا المشروع. الشكر الجزيل للمطورين التاليين:


*لؤي صهيب*

*الدور: تطوير وتنفيذ **واجهات فلاتر (Flutter UI)* وتنسيقها.
GitHub: https://github.com/Loay-Suhaib

*صهيب وليد*

*الدور: بناء **المنطق الخلفي (Business Logic)* للتطبيق وإدارة خدمات الـ *API*.
GitHub: https://github.com/Suhaib-Waleed (يرجى استبداله باسم المستخدم الفعلي)

*عبد الملك محمد*

*الدور: إدارة **حالة التطبيق (State Management)* وضمان تكامل الشيفرة (Code Integration).
GitHub: https://github.com/Abdulmalik-Mohamed (يرجى استبداله باسم المستخدم الفعلي)

*عبد القادر محمد*

*الدور: مراجعة الأكواد (Code Review) وضمان **جودة* الشيفرة و*كتابة التوثيق* الفني للمشروع.
GitHub: https://github.com/Abdulqadir-Mohamed (يرجى استبداله باسم المستخدم الفعلي)
## Demo
https://github.com/loai95378-dev/loai-sohaip
