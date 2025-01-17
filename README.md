# setup_flavor

### Flutter Launcher Icons

## Add flutter launcher icons for new flavor [![flutter_launcher_icons](https://img.shields.io/badge/Flutter%20Community-flutter__launcher__icons-blue)](https://pub.dev/packages/flutter_launcher_icons)
* Create a new `flutter_launcher_icons-flavor.yaml` file in `app/`
* In `flutter_launcher_icons-flavor.yaml`:

```yaml
flutter_icons:
  android: true
  ios: true
  image_path: "assets/dimension/flavor/dimension_icon.png" # example: "assets/hangmeas/staging/hangmeas_icon.png"
  adaptive_icon_background: "#FFFFFF"
  adaptive_icon_foreground: "assets/dimension/flavor/dimension_icon.png"
  min_sdk_android: 21

  flavors:
    sambathStg:
      image_path: "assets/dimension/flavor/dimension_icon.png"
      android: true
      ios: true
      web:
        generate: true
        image_path: "assets/dimension/flavor/dimension_icon.png"
        background_color: "#FFFFFF"
        theme_color: "#FFFFFF"  # custom the flavor color
      windows:
        generate: true
        image_path: "assets/dimension/staging/dimension_icon.png"
      macos:
        generate: true
        image_path: "assets/dimension/staging/dimension_icon.png"
```
* After create `flutter_launcher_icons-flavor.yaml`, run the command:
```bash
dart run flutter_launcher_icons -f flavor # example: dart run flutter_launcher_icons -f hangmeasStg
```


## Screenshot
![image](https://github.com/user-attachments/assets/4da08dc9-f6e5-49ab-831c-c6b4cfea8731)

## Demonstration
|Staging|Dev|
|-|-|
|https://github.com/user-attachments/assets/a370094f-b351-4ec2-8816-c241bc538d33|https://github.com/user-attachments/assets/084fad24-13b9-41c2-95a9-f0b9dc5fa1a4|

## Reference (Figma) : 

https://www.figma.com/design/UeBViZFBWnRnxHbw0CYVpT/Hang-meas-App?node-id=0-1&p=f&t=PObcm9wx5kmQeF7p-0
