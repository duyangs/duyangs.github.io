---
title: Android UI 样式 Selector 使用
date: 2020-11-06 14:26:16
categories: 
 Android
tags:
 Android
---

> Selector 算是比较常用的一个东西，记录些容易遗漏的使用方式。



#### ImageView 设置触摸焦点事件（其他View同理）

- 定义Selector

```xml
<?xml version="1.0" encoding="utf-8"?>
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:drawable="@drawable/ic_sel" android:state_checked="true" />
    <item android:drawable="@drawable/ic_sel" android:state_focused="true" />
    <item android:drawable="@drawable/ic_sel" android:state_pressed="true" />
    <item android:drawable="@drawable/ic_default" />
</selector>

<!-- 重点 顺序，xxxed="true" 放前面 -->
```

- 布局中引用

```xml
<ImageView
    android:id="@+id/iv"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_gravity="center_vertical"
    android:background="@drawable/bg_selector"
    android:src="@drawable/ic_selector"
    android:clickable="true"
    android:focusable="true"
    android:visibility="visible" />

<!-- 重点 android:clickable="true" -->
```

