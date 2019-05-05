# activity4
Android实验4

**题目要求：**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190505165138961.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
**核心代码:**
MainActivity.java
```java
package com.example.myapplication4;

import android.preference.PreferenceActivity;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

public class MainActivity extends PreferenceActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        addPreferencesFromResource(R.xml.preference);
    }
}
```
preference.xml：
```java
<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android">

    <EditTextPreference android:key="edit"
        android:title="Edit text preference"
        android:summary="An example that uses an edit text dialog"
        android:dialogTitle="Enter your favorite animal" />

    <ListPreference
        android:key="list"
        android:title="List preference"
        android:summary="An example that uses a list dialog"
        android:entries="@array/entry_list"
        android:entryValues="@array/values_list"
        android:dialogTitle="Choose one"
        android:defaultValue="1"
        />

    <PreferenceScreen
        android:key="screen"
        android:title="Screen preference"
        android:summary="Shows another screen of preferences">

        <CheckBoxPreference
            android:key="checkbox"
            android:title="Toggle preference"
            android:summary="Preference that is on the next screen but same hierachy" />

    </PreferenceScreen>

    <Preference
        android:key="progressBar"
        android:title="Intent preference"
        android:summary="Launches an Activity from an Intent">
        <intent android:action="android.intent.action.VIEW"
            android:data="https://www.baidu.com" />
    </Preference>

    <CheckBoxPreference
        android:key="pref_key_auto_delete"
        android:title="Parent checkbox preference"
        android:summary="This is vissually a parent"
        android:defaultValue="false" />

    <CheckBoxPreference
        android:key="pref_sync"
        android:title="Parent checkbox preference"
        android:summary="This is vissually a parent"
        android:dependency="pref_key_auto_delete"
        android:defaultValue="true" />

</PreferenceScreen>
```

**截图：**
1
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190505170141688.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
2![在这里插入图片描述](https://img-blog.csdnimg.cn/20190505170214570.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
3![在这里插入图片描述](https://img-blog.csdnimg.cn/20190505170327819.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
4![在这里插入图片描述](https://img-blog.csdnimg.cn/20190505170404394.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
5![在这里插入图片描述](https://img-blog.csdnimg.cn/2019050517042747.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
