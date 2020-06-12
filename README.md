# FirebaseLex
Wrapper framework that encapsulates several most commonly used Firebase frameworks (Crashlytics, Analytics, Messaging, Core, InstanceID and InAppMessaging) available for Carthage.

## Instructions
1. Specify in your Cartfile:
```
github "ivoleko/FirebaseLex" "master"
```
2. Add FirebaseLex framework in your project (together with input & output paths).

3. Locate "InAppMessagingDisplayResources.bundle" inside FirebaseLex.framework and add it to your project (without copying).

4. In Project Build Phases, add New Run Script Phase. In the script field, add new run script:
```
$PROJECT_DIR/Carthage/Checkouts/FirebaseLex/FirebaseLex/run
```
5. In the Input Files add two paths:
```${DWARF_DSYM_FOLDER_PATH}/${DWARF_DSYM_FILE_NAME}/Contents/Resources/DWARF/${TARGET_NAME}```
```$(SRCROOT)/$(BUILT_PRODUCTS_DIR)/$(INFOPLIST_PATH)```

