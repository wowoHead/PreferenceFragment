# PreferenceFragment
实验四

![](https://github.com/wowoHead/PreferenceFragment/blob/master/%E4%B8%BB%E7%95%8C%E9%9D%A2.jpg)

、、、

<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android">

    <PreferenceCategory android:title="In-line preferences">

        <CheckBoxPreference
            android:title="Checkbox preference"
            android:summary="This is a checkbox">

        </CheckBoxPreference>

    </PreferenceCategory>

    <PreferenceCategory
        android:title="Dialog-based preferences"
        android:key="Edit_sms_storage_title">

        <EditTextPreference
            android:key="edit_key"
            android:title="Edit text preference"
            android:summary="An example that uses an edit text dialog"
            android:dialogTitle="Enter your favorite animal">

        </EditTextPreference>

        <ListPreference
            android:key="list_key"
            android:title="List preference"
            android:summary="An example that uses a List dialog"
            android:dialogTitle="Choose one"
            android:entries="@array/option"
            android:entryValues="@array/option_value"
            >

        </ListPreference>

    </PreferenceCategory>

    <PreferenceCategory
        android:key="Launch_key"
        android:title="Launch preferences">

        <PreferenceScreen
            android:key="Screen_key"
            android:title="Screen preference"
            android:summary="Shows another screen of preferences">

            <CheckBoxPreference
                android:title="Toggle preference"
                android:summary="Preference that is on the next screen but same hierarchy">

            </CheckBoxPreference>

        </PreferenceScreen>

        <Preference android:title="Intent preference"
            android:summary="Launches an Activity from an Intent">

            <intent
                android:action="android.intent.action.VIEW"
                android:data="http://www.baidu.com">

            </intent>

        </Preference>

    </PreferenceCategory>

    <PreferenceCategory android:title="PreFerence attributes">

        <CheckBoxPreference
            android:key="Parent_key"
            android:title="Parent checkbox preference"
            android:summary="This is visually a parent"
            android:defaultValue="false">

        </CheckBoxPreference>

        <CheckBoxPreference
            android:title="Child checkbox preference"
            android:summary="This is visually a child"
            android:defaultValue="false"
            android:dependency="Parent_key">

        </CheckBoxPreference>

    </PreferenceCategory>


</PreferenceScreen>

、、、
