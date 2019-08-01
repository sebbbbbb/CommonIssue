# Crashlytics

### With firebase integration my crash are uploaded but not desymbolized

Solution :
Use right upload script to upload dsym
```shell
if [ $CONFIGURATION == Debug ]
then
CONF_FILE="GoogleService-Info-dev.plist" 
elif [ $CONFIGURATION == InHouse ]
then
CONF_FILE="GoogleService-Info-inhouse.plist" 
else
CONF_FILE="GoogleService-Info-release.plist"
fi

"${PODS_ROOT}/Fabric/run" <API-KEY> <API-SECRET> -gsp $CONF_FILE

# You shouldn't upload .dsym in debug since it can't take some times
if [ $CONFIGURATION != Debug ]
then
"${PODS_ROOT}/Fabric/upload-symbols" -gsp "${PROJECT_DIR}/***/resources/Firebase/$CONF_FILE" -p ios "${DWARF_DSYM_FOLDER_PATH}/${DWARF_DSYM_FILE_NAME}"
else 
echo "ℹ️ Running in debug : Skipping .dsym upload to save some times .."
fi
```
