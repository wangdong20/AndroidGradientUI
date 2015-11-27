# 运行效果图
![](https://github.com/wangdong20/First-android-repository/blob/master/wechatsample.gif)

# Qucik Setup
## 1. Include library
### Using AndroidStudio
Edit your **build.gradle** file and add below dependency:
```
dependencies {
    compile 'com.david.gradientuilib:gradientuilibrary:1.0.1'
}
```

## 2. Using in layout.xml
### GradientIconView

First the custom attribute should declare in xml like this:
```
xmlns:app="http://schemas.android.com/apk/res-auto"
```

Then you can add GradientIconView in layout.xml
```
<com.david.gradientuilibrary.GradientIconView
    android:id="@+id/id_iconfont_chat"
    app:bottom_icon="@mipmap/chats"
    app:top_icon="@mipmap/chats_green"
    android:layout_width="40dp"
    android:layout_height="35dp" />
```

The **GradientIconView** can **gradient change** itself from top_icon to bottom_icon.
GradientIconView will show top icon completely like this:
```gradientIconView.setIconAlpha(1.0f);```
And it will show bottom icon completely like this:
```gradientIconView.setIconAlpha(0);```

### GradientTextView

You can add GradientTextView in layout.xml like this.
```
<com.david.gradientuilibrary.GradientTextView
    android:id="@+id/id_chats_tv"
    app:bottom_text_color="@color/tab_text_gray"
    app:text="@string/chats"
    app:text_size="12sp"
    app:top_text_color="@color/tab_bg_green"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content" />
```

The **GradientTextView** can **gradient change** itself textcolor from top_text_color to bottom_text_color.
GradientIconView will show top textcolor completely like this:
```gradientTextView.setTextViewAlpha(1.0f);```
And it will show bottom textcolor completely like this:
```gradientTextView.setTextViewAlpha(0);```