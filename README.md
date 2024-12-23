# Docu Edges

Document scanner app with edge detection and cropping functionality. 

## Introduction

The app scans a document image, detects the edges and applies a magnifier to crop the document.

### Features

- On-device machine learning for document scanning 
- Edge detection capability
- Use of OpenCV edge detection library and ffi to connect native C++ to Flutter with the help of Dart Isolates.
- Ability to crop and edit images
- Ability to download the cropped image

### Implementation / Architectural Decision

Although the project is a simple app in terms of its frontend capacity, the project was still implemented as though it was going to grow into an enterprise app using the MVVM approach.
- State Management was done with setState (with a growth route towards use of Riverpod for SM and DI)
- File/Folder structure ensures large codebase ease of maintenance

### Build Limitations

The project depends on a plugin I had to develop for the OpenCV integration to work perfectly. This plugin has large files that could not be uploaded to Github, hence, I had to use the local version of the Plugin. Explanation on how to get the files/folders for the Plugin is explained in the [Plugin's Readme](https://github.com/IdrisAdeyemi01/flutter_detect_edges/blob/main/README.md). After this, the plugin path can be changed in the pubspec.yaml file to the local directory of the Plugin on your machine.

### Other Limitations

- The web and desktop environments were not prioritized for this submission.
- CI / CD was not prioritized for this submission.
- Flavors were not prioritized for this submission.
- Analytics and Error Reporting was not prioritized for this submission.

### Setup Instructions

- run `git clone https://github.com/IdrisAdeyemi01/docu_edges.git` in your terminal
- navigate to the directory containing the cloned project (docu_edges)
- open in any code editor of your choice e.g Android studio, VSCode etc
- Complete setup as mentioned in the Build Limitation section
- connect your Android device
- run `flutter run` to test in your connected device

* You can also simply install the app's apk to text. [Docu Edges](https://drive.google.com/file/d/1qOyIJ-Fj0w9doZE4R5QtGB4ZMjKBTCN8/view?usp=drive_link)

Built with ❤️ in Flutter. Powered by OpenCV through Dart FFI.
