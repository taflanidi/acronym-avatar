### Description

AcronymAvatar is a terribly simple library to show avatars with acronyms in your application. Would you like to show user's list in your messenger (yet another one...) or just create the unorthodox user profile? This library is the best choice for you.

### Getting started

Just include the library into your project as a Gradle dependency: 
```Groovy
implementation 'com.redmadrobot:acronym-avatar:1.0'
``` 

Then add `AvatarView` into your XML layout:
```XML
    <com.redmadrobot.acronymavatar.AvatarView
        android:id="@+id/user_avatar"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />
```        

And pass full username to the `setText` method:
```Kotlin
user_avatar.setText("Captain Nemo")
```

That's all!


### Capabilities

* Setting text via XML and programmatically
* Using custom placeholders (Drawables only!)
* Configuring zoom out for the acronym

##### Setting text via XML and programmatically
Building acronyms by text works like this: if you pass one word to the `setText` method or to the `app:text` XML field then the library will take only two first symbols and show them as an acronym. If you pass two or more words then the library will take the first symbols from first and second words only and show them as an acronym. For instance:
* Captain -> CA
* Captain Nemo -> CN
* Nemo, my name forever more -> NM

##### Using custom placeholders (Drawables only!)
We like our default placeholder very much, but you won't probably want to use it in real-world applications ;) For this case we augmented our library by setting custom placeholder feature. You can set it via XML as following:
```XML
    <com.redmadrobot.acronymavatar.AvatarView
        android:id="@+id/user_avatar"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" 
        app:placeholder="@drawable/custom_placeholder" />
```

##### Configuring zoom out for the acronym
The library is preconfigured to using optimal text zooming out, but you can set your own value this way:
```XML
    <com.redmadrobot.acronymavatar.AvatarView
        android:id="@+id/user_avatar"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" 
        app:zoom_out="5" />
```