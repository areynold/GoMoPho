# GoMoPho
Google motion photos video extractor.

History: Android backups to Google Drive did not upload the video. Read  https://www.bitquabit.com/post/moving-and-backing-up-google-moving-images/ why.

Google Drive should now support backing up the video portion. https://www.guidingtech.com/share-motion-photos-google/

#### Compilation
```
dotnet build src\GoogleMotionImage.sln
```
Windows: Run  Build-Test-Zip.bat file to compile and test the program.

#### Testing in windows
```
Build-Test-Zip.bat
```

#### Running
When running any of the options below, you can either pass in a directory with your MVIMG files as an argument, or run it with no argument, then type or paste in the location of the directory with your MVIMG files.

**Windows .NET framework** 
```
.\bin\Windows\GoMoPhoConsole.exe
```
or
```
GoMoPhoConsole.exe "C:\Users\Clive\OneDrive\Documents\Pictures\Camera Roll"
```
**.NET Core runtime on GNU/Linux MacOS or Windows** 
Use the dotnet runtime https://www.microsoft.com/net/download to execute bin/netcoreapp2.0/publish/GoMoPhoCoreConsole.dll
```
dotnet bin/netcoreapp2.0/publish/GoMoPhoCoreConsole.dll test-image
```

**.NET core natively compiled Windows** 
```
bin\netcoreapp2.0\win-x64\GoMoPhoCoreConsole.exe test-image\
```

**.NET core natively compiled GNU/Linux**
```
bin/netcoreapp2.0/linux-x64/publish/GoMoPhoCoreConsole test-image
```

**.NET core natively compiled GNU/Linux Ubuntu-x64**
```
bin/netcoreapp2.0/ubuntu-x64/publish/GoMoPhoCoreConsole test-image
```

**.NET core natively compiled MacOS**
```
bin/netcoreapp2.0/osx-x64/publish/GoMoPhoCoreConsole test-image
```
## Result
On completion, new video.mp4 files will be created for any motion photo found.
This will not create the wiz-bang google AI versions.. https://ai.googleblog.com/2018/03/behind-motion-photos-technology-in.html
Just the originals.


```
No directory given to process

First argument is the folder i.e. "c:\somewhere with spaces\"
Second optional agument is the search pattern, i.e. default of *MVIMG_*.jpg
Third optional agument is the search pattern for video file, where file ends with i.e. default of .mp4


You can 1) type (or paste) in a folder now - without quotes and press <ENTER>
        2) press <ENTER> to exit


    Example typed text, afterwards pressing <ENTER>
    >c:\somewhere with spaces

> C:\temp\New folder (2)
Found the following number of google motion photos: 5
Searching C:\temp\New folder (2)\MVIMG_20180906_092408.jpg   Found the video
Searching C:\temp\New folder (2)\MVIMG_20180906_102344.jpg   Found the video
Searching C:\temp\New folder (2)\MVIMG_20180906_102350.jpg   Found the video
Searching C:\temp\New folder (2)\MVIMG_20180906_102352.jpg   Found the video
Searching C:\temp\New folder (2)\MVIMG_20180906_104633.jpg   Found the video
Finished. Processed 5 videos for 5 images files.
Press any key to exit
```