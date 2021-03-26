# Changelog
All notable changes to this package will be documented in this file.
The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [25.0.2] - 2021-03-26

### What's Fixed
- removed redundant libraries that also ship with Unity's Oculus integration

## [25.0.1] - 2021-03-26

### What's New
- updated Oculus Integration to 25.0

### Integration Changes
- Updated OVRPlugin to 1.57.0

## [25.0.0] - 2021-02-19

### What's New
- Added support to upload the debug symbols from Unity
- Added animations for controller models
- Color Space API now uses nativeColorGamut and colorGamut variables to manage color spaces
- Added support for Fisheye Layer in OVROverlay
- Exposed OVRPlugin.SetKeyboardOverlayUV() to enable positioning of the OS virtual keyboard overlay
- Added setEyeFovPremultipledAlpha and getEyeFovPremultipledAlpha APIs to enable and disable premultiplied alpha on the EyeFov layer
  - Added support for the following features in OpenXR:
  - Different color spaces
  - Color Scale/Bias
  - Is External Surface
  - Equirect Layer
  - Cubemap Layer
  - Underlays
  - Left/Right Textures
  - Headlocked Layer
  - Cylinder Layer
  - Quad Layer

### What's Fixed
- Null exception error when PollEvent fails
- Memory leak coming from PollEvent
- Color gamut settings not being serialized in OVRManager
- Cylinder layers in Vrapi not applying overriden textyture rectangles properly
- Layout error by moving OVR Quick Scene Preview work to Update()

### Improvements
- Improved stability when app is paused or resumed
- Added new VR intent filter to OVRManifestPreprocessor in Unity
- Color Gamut now defaults to Rift CV1

### Integration Changes
- Updated the Oculus Unity Integration to v25.0, including:
- Updated OVRPlugin to 1.57
- Updated the Audio Spatializer to 25.0
- Updated the Platform integration to 25.0
- Updated the Avatar integration to 20.0
- Updated the LipSync integration to 20.0

Note: You may encounter issues when running ARM7 build on Oculus Go or Oculus Quest, if you are using Unity's XR Management system with the latest OVRPlugin and the Oculus XR Plugin is outdated. In such case, you can either switch to ARM64 build, or upgrade the Oculus XR Plugin to 1.4.0+ to fix the issue.

### License Update
- Updated Oculus master license for the Oculus Integration package.

## [23.1.1-preview] - 2021-01-12

### What's New
- updated Oculus Integration to 23.1

### Integration Changes
- Updated OVRPlugin to 1.55.1

## [23.0.1-preview.3] - 2020-12-10

### What's New
- updated Oculus Integration to 23.0
- fixed Avatar samples

## [23.0.0] - 2020-12-04

### What's New
- Added support for OpenXR experimental plugin for Oculus Quest and Oculus Quest2.
- Added Phase Sync adaptive frame timing to Oculus Quest and Oculus Quest 2 apps.
- Oculus Quest 2 can now set 80Hz and 90Hz display refresh rates when you select Oculus Quest 2 as a target device.
- Note: You may encounter issues when running ARM7 build on Oculus Go or Oculus Quest, if you are using Unity's XR Management system with the latest OVRPlugin and the Oculus XR Plugin is outdated. In such case, you can either switch to ARM64 build, or upgrade the Oculus XR Plugin to 1.4.0+ to fix the issue.

### What's Fixed
- Fixed Unity MRC Vulkan gamma color issue and several validation layer errors
- Support added for OVROverlay for Vulkan (requires upgrading to the latest Unity version for working functionality)
- GetSystemHeadsetType() returns ovrpSystemHeadset_Oculus_Link_Quest_2 when using Oculus Link with Oculus Quest 2
- Enabled GPU boost on Oculus Quest when MRC casting is activated
- Renamed the target device name for Oculus Quest 2 in the Android Manifest file from delmar to quest2

### Integration Changes
- Ended support for Unity version 2017.4. The minimum supported Unity Editor version for Oculus development is 2018.4.
- Updated the Oculus Unity Integration to v18.0, including:
- Updated OVRPlugin to 1.55
- Updated the Audio Spatializer to 23.0
- Updated the Platform integration to 23.0
- Updated the Avatar integration to 20.1
- Updated the LipSync integration to 20.0

### License Update
- Updated Oculus master license for the Oculus Integration package.

## [20.1.1-preview] - 2020-12-03

### What's New
- updated Oculus Integration to 20.1
- removed all DLLs that are also part of Unity's Oculus XR Plugin to avoid collisions
- catched a DLLNotFoundException in Spatializer
- disabled "Auto Referenced" from all AsmDefs

## [20.1.0] - 2020-10-05

### What's New
- Added support for Oculus Quest 2 as a target device.
- Added OVRManager.systemHeadsetType() to return the headset type.
  Note: You may encounter issues when running ARM7 build on Oculus Go or Oculus Quest, if you are using Unity's XR Management system with the latest OVRPlugin and the Oculus XR Plugin is outdated. In such case, you can either switch to ARM64 build, or upgrade the Oculus XR Plugin to 1.4.0+ to fix the issue.

### Integration Changes
- Ended support for Unity version 2017.4. The minimum supported Unity Editor version for Oculus development is 2018.4.
- Updated the Oculus Unity Integration to v18.0, including:
- Updated OVRPlugin to 1.52.1
- Updated the Audio Spatializer to 20.0
- Updated the Platform integration to 19.0
- Updated the Avatar integration to 20.1
- Updated the LipSync integration to 20.0

### License Update
- Updated Oculus master license for the Oculus Integration package.

## [20.0.1-preview] - 2020-09-25

### What's New
- Oculus Integration is now an (inofficial) package
- Added AsmDefs for package
- Moved all Samples into Package samples (accessible via Unity Package Manager)

## [20.0.0] - 2020-09-03

### What's New
- Added an option to preview OVROverlay inside the Unity editor.

### Improvements
- Used the culture-invariant string.Format() method when converting OVRPlugin types to string.
- Added support for bottom/top layout via OVROverlay stereo layers. Through this, we added a new OVROverlay flag, invertTextureRects. To use the old behavior, toggle this flag as necessary.

### Bug Fixes
- Fixed random Unity editor crash when building scenes with Oculus XR plugin.

Note: You may encounter issues when running ARM7 build on Oculus Go or Oculus Quest, if you are using Unity's XR Management system with the latest OVRPlugin and the Oculus XR Plugin is outdated. In such case, you can either switch to ARM64 build, or upgrade the Oculus XR Plugin to 1.4.0+ to fix the issue.

### Integration Changes
- Ended support for Unity version 2017.4. The minimum supported Unity Editor version for Oculus development is 2018.4.
- Updated the Oculus Unity Integration to v18.0, including:
  - Updated OVRPlugin to 1.52
  - Updated the Audio Spatializer to 20.0
  - Updated the Platform integration to 19.0
  - Updated the Avatar integration to 20.0
  - Updated the LipSync integration to 20.0

### License Update
- Updated Oculus master license for the Oculus Integration package.

## [19.1.0] - 2020-08-07

### What's New
- Added support to display the system keyboard as an overlay on an Oculus Quest app.
  Note: Restart your Oculus device to use the keyboard overlay functionality.
- Deprecated Oculus Go support. To develop apps for Oculus Go, use Oculus Integration v18.0 or prior. You can retrieve any prior versions of the Oculus Integration package from the Unity Integration Archive page.

### Improvements
- Updated the callback priority of PostGenerateGradleProject to improve the Android manifest generation.
- Removed the Queue Ahead project setting from OVRManager.
- OVRHeadsetEmulator will only set or restore the cursor lock mode when the emulator is activated or deactivated, instead of overriding the cursor lock mode every frame.

### Bug Fixes
- Enforced minimum version of Oculus XR plugin 1.4.0 due to incompatibility with previous versions.
- Fixed errrors in Unity 2020.2 because of usage of UnityEngine.Experimental.XR.Boundary in XR SDK.
- Fixed XRSDK warnings when using Unity 2020.1.x.
- Fixed siginifcant performance regression in the Unity editor when using Oculus Rift S.
- Fixed the OVRPlugin.IsPerfMetricsSupported() method to return the correct value in development builds.

Note: You may encounter issues when running ARM7 build on Oculus Go or Oculus Quest, if you are using Unity's XR Management system with the latest OVRPlugin and the Oculus XR Plugin is outdated. In such case, you can either switch to ARM64 build, or upgrade the Oculus XR Plugin to 1.4.0+ to fix the issue.

### Integration Changes
- Ended support for Unity version 2017.4. The minimum supported Unity Editor version for Oculus development is 2018.4.
- Updated the Oculus Unity Integration to v18.0, including:
  - Updated OVRPlugin to 1.51.1
  - Updated the Audio Spatializer to 19.0
  - Updated the Platform integration to 19.0
  - Updated the Avatar integration to 19.0
  - Updated the LipSync integration to 1.43

### License Update
- Updated Oculus master license for the Oculus Integration package.

## [18.0.0] - 2020-07-07

### New Features
- Use customized XML to define security configuration for Android instead of using Oculus-generated XML.

### Improvements
- Moved the shader stripping option in OVRManager.
- OVRManager requires Unity version 2018.3 or higher.

### Bug Fixes
- Added support to trigger the RecenteredPose event in stationary experience or when there's no guardian set up.
- Fixed the return value for the GetHmdColorDesc() method to Unknown for macOS or any other unsupported platforms.
- Fixed in-Editor MSAA setting forced off when using XR Management.
- Fixed a race condition in which bone pose updates are retrieved before the mesh is bound to the skeleton causing issues with the appearance of the skinned mesh component.

Note: You may encounter issues when running ARM7 build on Oculus Go or Oculus Quest, if you are using Unity's XR Management system with the latest OVRPlugin and the Oculus XR Plugin is outdated. In such case, you can either switch to ARM64 build, or upgrade the Oculus XR Plugin to 1.4.0+ to fix the issue.

### Integration Changes
- Ended support for Unity version 2017.4. The minimum supported Unity Editor version for Oculus development is 2018.4.
- Updated the Oculus Unity Integration to v18.0, including:
  - Updated OVRPlugin to 1.50
  - Updated the Audio Spatializer to 18.0
  - Updated the Platform integration to 18.0
  - Updated the Avatar integration to 18.0
  - Updated the LipSync integration to 1.43

## [17.0.0] - 2020-05-26

### New Features
- Added support to set specific color space on an Oculus device to overcome the color variation that may occur due to different color spaces in use.
- Added support to check the dominant hand while you set up hand tracking.

### Integration Changes
- Updated the Oculus Unity Integration to v17.0, including:
  - Updated OVRPlugin to 1.49
  - Updated the Audio Spatializer to 16.0
  - Updated the Platform integration to 17.0
  - Updated the Avatar integration to 15.0
  - Updated the LipSync integration to 1.43

## [16.0.0] - 2020-04-28

### New Features
- Added support to strip unused shaders from compilation to reduce the build time.

### Integration Changes
- Updated the Oculus Unity Integration to v16.0, including:
  - Updated OVRPlugin to 1.48
  - Updated the Audio Spatializer to 16.0
  - Updated the Platform integration to 16.0
  - Updated the Avatar integration to 15.0
  - Updated the LipSync integration to 1.43
- Quest Mixed Reality Capture (MRC) now functions with Universal Render Pipeline (URP)/Scriptable Render Pipeline (SRP).
- OVRPlugin.GetSystemHeadsetType() returns Oculus_Link_Quest when using Oculus Link.

## [15.0.0] - 2020-04-06

### New Features
Added support for setting universal menu as a system overlay. For more information, go to the Enabling Focus Awareness for System Overlays guide.

### Integration Changes
- Updated the Oculus Unity Integration to v15.0, including:
  - Updated OVRPlugin (Utilities for Unity) to 1.47
  - Updated the Audio Spatializer to 15.0
  - Updated the Platform integration to 15.0
  - Updated the Avatar integration to 15.0
  - Updated the LipSync integration to 1.43