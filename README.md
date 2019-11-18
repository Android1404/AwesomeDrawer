# Awesome Drawer

## Introduction
实现Android窗帘拉开折叠效果

## Usage

### xml布局文件使用

```xml
<com.hx.curtain.drawer.CurtainContentLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/curtain_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    app:behind_menu="@layout/menu_left"
    app:content="@layout/layout_curtain_content"
    app:maxRate="0.5" />
```

### 监听滑动的系数

```java
CurtainContentLayout curtain_layout = findViewById(R.id.curtain_layout);
curtain_layout.setCurtainLayoutListener(new CurtainContentLayout.OnCurtainLayoutListener() {
    @Override
    public void onSlide(View caurtainLayout, float slideOffset) {
        Log.e("CurtainActivity", "slideOffset: " + slideOffset);
    }
});
```

### 自定义属性

  * `behind_menu` menu后面的布局
  * `content`     menu的内容，必须提供这个属性，不然会异常
  * `maxRate`     menu最大的收缩比
### 应用在Menu中,和CurtainContentLayout的各种style预览如下：

效果1|效果2 
---|---
 ![image](effect/curtain_menu.gif)|![image](effect/mutil_curtain_views.gif)

## Bolg

  * [https://www.jianshu.com/u/c95d21153470](https://www.jianshu.com/u/c95d21153470)

## License
```

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

