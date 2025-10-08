# Build Instructions - FLAM Edge Detection

## Quick Setup Guide

### Prerequisites Installation
1. **Android Studio**: Download from developer.android.com
2. **NDK**: Install via SDK Manager in Android Studio
3. **OpenCV 4.8.0**: Download Android SDK from opencv.org
4. **Git**: For version control and repository cloning

### Repository Setup
Clone the repository
git clone https://github.com/SwayamPandey19/flam-edge-detection-swayam.git
cd flam-edge-detection-swayam

Open in Android Studio
File -> Open -> Select project directory


### Android Studio Configuration
1. **SDK Configuration**: Ensure Android SDK 34 is installed
2. **NDK Setup**: Install NDK version 25.1.8937393 or later
3. **OpenCV Integration**: Link OpenCV Android SDK to project
4. **Build Tools**: Sync project and resolve dependencies

### Building the Project
From Android Studio Terminal
./gradlew assembleDebug

Or use Android Studio Build menu
Build -> Make Project


### Device Testing
1. **Enable Developer Options** on Android device
2. **USB Debugging**: Enable in Developer Options
3. **Install APK**: Deploy via Android Studio or ADB
4. **Camera Permissions**: Grant when prompted

## Web Demo Setup

### TypeScript Viewer
Install TypeScript globally
npm install -g typescript

Initialize TypeScript configuration
tsc --init

Compile TypeScript files (if modifications needed)
tsc main.ts

Serve web content
python -m http.server 8000

Or use any local web server


### Live Demo Access
- **Direct URL**: https://codepen.io/Swayam-Pandey/pen/azdWobd
- **Local Development**: Modify TypeScript source as needed
- **Browser Compatibility**: Modern browsers with Canvas API support

## Development Workflow

### Code Organization
project/
├── app/src/main/
│ ├── java/ # Android Java/Kotlin source
│ ├── cpp/ # Native C++ implementation
│ ├── res/ # Android resources
│ └── AndroidManifest.xml
├── web/ # TypeScript web viewer
├── docs/ # Documentation
└── demo/ # Demo assets


### Debugging Setup
1. **Native Debugging**: Configure NDK debugging in Android Studio
2. **OpenCV Integration**: Verify library linking and initialization
3. **JNI Interface**: Test Java ↔ C++ communication
4. **Performance Profiling**: Use Android Studio profiler tools

## Research Integration Notes

### Parameter Configuration


// Research-optimized values from IIT and DRDO experience
const double GAUSSIAN_SIGMA = 1.4; // From materials analysis
const double CANNY_THRESHOLD_LOW = 75.0; // Architectural optimization
const double CANNY_THRESHOLD_HIGH = 150.0; // Vision Transformer insights
const int MORPHOLOGY_KERNEL_SIZE = 3; // Edge continuity enhancement


### Performance Optimization
- **Memory Management**: Efficient Mat allocation patterns
- **Processing Pipeline**: Optimized algorithm sequencing
- **Hardware Acceleration**: OpenGL ES texture operations
- **Battery Efficiency**: Balanced processing intensity

## Troubleshooting Guide

### Common Issues
1. **NDK Build Errors**: Verify NDK version compatibility
2. **OpenCV Linking**: Check library path configuration
3. **JNI Crashes**: Validate native method signatures
4. **Performance Issues**: Profile memory usage and CPU load

### Resolution Steps
Clean and rebuild project
./gradlew clean
./gradlew assembleDebug

Verify NDK installation
ndk-which gcc

Check OpenCV integration
grep -r "opencv" app/build.gradle



## Deployment Considerations

### Production Build
Release build with optimization
./gradlew assembleRelease

Sign APK for distribution
Configure signing in build.gradle

### Performance Monitoring
- **Frame Rate**: Monitor real-time FPS in production
- **Memory Usage**: Track heap allocation patterns
- **Processing Time**: Measure algorithm execution latency
- **Device Compatibility**: Test across Android form factors

---

**Build Status**: Verified and tested  
**Last Updated**: October 8, 2025  
**Maintainer**: Swayam Pandey  
**Support**: pandeyswayam19@gmail.com
