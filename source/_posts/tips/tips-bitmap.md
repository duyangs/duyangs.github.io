---
title: tips-bitmap
date: 2020-11-05 09:49:00
categories:
- Tips
tags:
- Bitmap
---

> Android 中使用 Bitmap 的场景很多，整理一些使用过程中的小技巧。



#### 获取本地图片宽高，但不需要Bitmap对象

> 某些场景需要从本地读取图片的宽高，但是不需要使用这个Bitmap对象

```kotlin
val options: BitmapFactory.Options = BitmapFactory.Options()
options.inJustDecodeBounds = true //这个参数设置为true才有效，
BitmapFactory.decodeFile(answerCacheFile.path, options) //这里的bitmap是个空

val width = options.outWidth //图片宽
val height = options.outHeight //图片高

//--------------------------------------------------------------------------------

//注意：
//decodeFile()方法返回的类型是Bitmap,但是Java语法，未做非空判断，切记不要写出以下这种形式
val bitmap:Bitmap = BitmapFactory.decodeFile(answerCacheFile.path, options) 
//这里的bitmap是个空,会报 java.lang.IllegalStateException
```

