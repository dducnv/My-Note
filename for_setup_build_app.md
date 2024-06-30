# keystore create
Linux Mac: 
keytool -genkey -v -keystore ~/upload-keystore.jks -keyalg RSA -keysize 2048 -validity 10000 -alias upload

Windows:
keytool -genkey -v -keystore %userprofile%\upload-keystore.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias upload

# SHA certificate fingerprints debug
Mac: 
keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android

Windows:
keytool -list -v -keystore "\.android\debug.keystore" -alias androiddebugkey -storepass android -keypass android

Linux:
keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android

# Create upload_certificate
keytool -export -rfc -keystore upload-keystore.jks -alias upload -file upload_certificate.pem

# Get public key
keytool -export -v -keystore upload-keystore.jks -alias upload -file my-public-key.cer
