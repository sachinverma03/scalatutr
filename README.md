# scala Tutorial
Tutorial followed: http://allaboutscala.com/tutorials/

Scala Initial setup
Intellij community edition: https://www.jetbrains.com/idea/download/#section=windows
OpenJdk8: https://adoptopenjdk.net/upstream.html
(download and extract wherever needed)
Errors faced: 
- 'Error occurred during initialization of VM Could not reserve enough space for 1572864KB object heap' when project was getting synced intially
 Possible Reason: Using incompatible jdk version(1.8 for 32 bit instead of 64 bit)
 Solution: downloaded openjdk 8 (since oracles' original jdk is now licence has changed and needs logins and lambs bloods and an owl's eye)from the given link and added it to project
 This can be configured when creating the project or in File->Project Structure(ctrl+alt+shift+S)->Project Settings->Project->Project SDK->Click on new select the openjdk
 (It might be pretty much obvious but writing it anyway to make it look cool and because I am defintly going to forget this).
 
- "Error: Could not find or load main class" When running the project.
Reason: jdk did not know where to pick the class from. It was most probably searching in its own home directory. In simple words: Did not add the openjdk to Path environment variable.
Solution added openjdk to system's 'Path' variable and  File -> Invalidate Caches and Restart.
