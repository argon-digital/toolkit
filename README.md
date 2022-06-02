[![Release](https://jitpack.io/v/mahimrocky/ShowMoreText.svg)](https://github.com/mahimrocky/ShowMoreText/releases/tag/1.0.2)

# Argon Digital's Android Toolkit

This is simple library that simplifies RecyclerView Adapter and Adds TextView that has "Read more" and "Read less" functions.


# Root Gradle
```sh
    allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

# App Gradle:

```sh
dependencies {
	   implementation 'com.github.argon-digital:toolkit:1.0.0'
	}
```
You have to use just this xml. You can modify or set color your own textView. **But don`t need to use maxLength or maxLine in text view. It may be confilict with library**.
# XML Section

```sh
    <com.skyhope.showmoretextview.ShowMoreTextView
        android:id="@+id/text_view_show_more"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/text"
        />
```

**So this part describe how you sort your text? You can sort your text by line number or character length**

In Activity you can use like:
```sh
    ShowMoreTextView textView = findViewById(R.id.text_view_show_more);
    
    //You have to use following one of method    
    
    // For using character length
    textView.setShowingChar(numberOfCharacter);
    //number of line you want to short
    textView.setShowingLine(numberOfLine);
```
You can change text of **Show more** or **Show less**

```sh
    textView.addShowMoreText("Continue");
    textView.addShowLessText("Less");
```

You can change text color of **Show more** or **Show less**

```sh
    textView.setShowMoreColor(Color.RED); // or other color
    textView.setShowLessTextColor(Color.RED); // or other color
```
# Happy Coding
