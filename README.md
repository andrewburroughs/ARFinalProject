# UARK AR Campus Tour Phone Application. Contains unity package and READMe

### Step 1: Getting Started
  1. Go here and download the latest .tgz file: https://github.com/CesiumGS/cesium-unity/releases It is Unity cesium which provides the geospatial anchors and origin required for componenets to load properly.
     In order to upload this to your unity project go to package manager and select upload from tarball then select the file.
  2. Add AR foundation to your project if not there already (this should be a searchable package in Unity)
  3. Next you will also need to install the ARCore Extensions package. To do so go back to unity package manager and select add from git URL then paste the following: https://github.com/google-ar/arcore-unity-extensions.git#arf5

### Step 2: Import provided package into Unity and select scene
  1. There should be two scenes contained within this package.

     InClassDemo - This scene was used for our demo day in class where we showed our professor our projects. It contains pathing to 3 locations (JBHunt, Old Main, Library).
         It also contains audio and text associated with different campus locations
     
     FinalSchoolDemo - This scene was setup for the School demo day during finals week. It only contains 2 locations (I3R and Old Main). It has a few extra additions such as the hog anchor
         and play/pause functionality on audio playing.

### Step 3: Update Player/Build Settings in Unity
- Switch Platform to Android 
- Player Settings > Other Settings > Uncheck Auto Graphics API > Remove "Vulkan" from Graphics APIs
- Player Settings > Other Settings > Set API Level at least 24+
- Player Settings > Other Settings > Set 'Scripting Backend' to "IL2CPP"
- Player Settings > Other Settings > Checkmark "ARM64"
- XR Plug-in Management > Checkmark "Google ARCore"
- XR Plug-in Management > ARCore Extensions > Set Android Authentication Strategy API Key (sent via email)
- XR Plug-in Management > ARCore Extensions > Chackmark both Geospatial and Geospatial Creator
- (Optional to get rid of Google.IOS error) Project Search bar type "Google" and search in All > Locate a Google.IOS Resolver file > Right click and hit "Show in explorer" > Delete all "Google.IOSResolver" files should be 4 of them 
