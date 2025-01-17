## To setup flavor
### 1. Update build.gradle in /android/app/

```gradle
    flavorDimensions "vendorapp", "flavor"
    productFlavors {
        hangmeas {
            dimension "vendorapp"
            applicationId "com.centralmarket.hangmeas"
        }

        dev {
            dimension "vendorapp"
            applicationIdSuffix ".dev"
            versionNameSuffix "-dev"
        }

        stg {
            dimension "vendorapp"
            applicationIdSuffix ".stg"
            versionNameSuffix "-stg"
        }
    }
```
## Purpose:
1. Create many similar apps in the only one project
2. Allows developers to build and manage different versions of every single app from the same codebase, each with distinct behaviors and appearances. Develop app Separately via different environment such as, production, development, staging also.
3. Allows developers to separate the assets for each flavors, so that when they build app, the excluded assets for other flavor will not be build.
4. Additionally, flavors enable you to manage different Firebase projects for each flavor, ensuring that each version of the app can have its own database or other backend services. This setup helps in maintaining a clean and organized project structure while allowing for flexibility and customization across various environments or client-specific requirements.
## Screenshots
1. 
![Screenshot 2025-01-09 145649](https://github.com/user-attachments/assets/d1f0702c-4dbc-40bc-b041-0a02075c376c)
2. When developers setup assets for hangmeasStg only. So when they run or build hangmeasDev, those assets will not be build.
|staging|dev|
|-|-|
|![Screenshot_1736410513](https://github.com/user-attachments/assets/08e9a56c-6f28-490e-bbd7-010e776eb98b)|![Screenshot_1736410542](https://github.com/user-attachments/assets/0222beb5-ecb0-4255-8d27-7dedd770d87c)|
