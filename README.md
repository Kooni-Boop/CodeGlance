CodeGlance2
==========
Original CodeGlance: https://github.com/Vektah/CodeGlance
Plugin Repository: https://plugins.jetbrains.com/plugin/15562-codeglance2
Latest build: https://github.com/Kooni-Boop/CodeGlance2/Release

InteliJ plugin that displays a zoomed out overview or minimap similar to the one found in Sublime into the editor pane. The minimap allows for quick scrolling letting you jump straight to sections of code.

 - Works with both light and dark themes using your customized colors for syntax highlighting.
 - Worker thread for rendering
 - Color rendering using InteliJ's tokenizer
 - Scrollable!
 - Embedded into editor window
 - Complete replacement for Code Outline that supports new Intellij builds.

![Dracula](https://raw.github.com/Vektah/CodeGlance/master/pub/example.png)

Building using Gradle
====================
```
git clone https://github.com/Kooni-Boop/CodeGlance2
cd CodeGlance2
# run the tests
./gradlew test

# build the plugin and install it in the sandbox then start idea
./gradlew runIdea

# build a release
./gradlew buildPlugin

```
The result will be saved as build/distributions/CodeGlance-{version}.zip


Running from source in IntellJ
===================
1. Make sure you have the Plugin DevKit installed.
2. Checkout sources from github
3. Create a new Intellij Platform plugin project
4. Select source directory, chose a plugin sdk (create one that points to your intellij install).
5. Mark src/main/java as source root, and src/test/java as test root.
6. In order to run tests you will need to find mockito and testing jars. I usually do this with Gradle.
7. In module settings set the path to META-INF to src/main/resources
8. Hit Run.


Show/Hide or Enable/Disable Minimap
===================
* **Ctrl-Shift-G** to toggle minimap.
* Settings > Other Settings > CodeGlance
