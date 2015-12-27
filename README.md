[![Build Status](https://travis-ci.org/Data5tream/emoji-lib.svg?branch=master)](https://travis-ci.org/Data5tream/emoji-lib) [![Coverity Scan](https://scan.coverity.com/projects/7409/badge.svg)](https://scan.coverity.com/projects/data5tream-emoji-lib) [![Download](https://api.bintray.com/packages/data5tream/maven/emoji-lib/images/download.svg)](https://bintray.com/data5tream/maven/emoji-lib/_latestVersion)

# Emoji Support Lib

Add emoji support to your Android app!

This library combines the works of [@rocboronat](https://github.com/rocboronat/emojicon), [@ankushsachdeva](https://github.com/ankushsachdeva/emojicon) and [@peibumur](https://github.com/pepibumur/emojize).

## Emoji Support Lib is currently being rewritten to increase performance and reduce size.

## Installation

Gradle:

```
repositories {
    ...
    maven { url "https://jitpack.io" }
  }

...

dependencies {
    compile 'com.github.Data5tream:emoji-lib:0.0.1'
   }


```
Maven:
```
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>

...

  <dependency>
    <groupId>com.github.data5tream</groupId>
    <artifactId>emoji-lib</artifactId>
    <version>0.0.1</version>
  </dependency>
```

## Basic usage

Use `com.github.data5tream.emojilib.EmojiTextView` and `com.github.data5tream.emojilib.EmojiEditText` in your layout XMLs to automatically represent unicode emojis.

Use `EmojiParser` to convert Emoji Cheat Sheet codes into unicode characters:
```java
String formattedAsCheatCode = ":smile:";
String formattedAsUnicode = EmojiParser.parseEmojis(formattedAsCheatCode);
```
`formattedAsUnicode` will be: :smile:

You can also use `EmojiParser` to convert unicode emojis into Emoji Cheat Sheet codes:
```java
String formattedAsUnicode = "😄";
String formattedAsCheatCode = EmojiParser.convertToCheatCode(formattedAsUnicode);
```
`formattedAsCheatCode` will be: `:smile:`

## Acknowledgements

Emoji Support Lib uses emoji graphics from [emoji-cheat-sheet.com](https://github.com/arvida/emoji-cheat-sheet.com/tree/master/public/graphics/emojis).

This project uses code published by [Roc Boronat](https://github.com/rocboronat) and [Ankush Sachdeva](https://github.com/ankushsachdeva) and has a dependency on [Guava](https://github.com/google/guava).

## License

```
Copyright 2015 Simon Barth

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
