### Setup Instructions

1. Update ERN platform to 0.34.0

  + `ern platform use 0.34.0`
  
2. Setup the cauldron

  + `ern cauldron repo add AndroidCauldron git@github.com:noor-mohiuddin-agilea/AndroidCauldron.git`
  
3. Generate ERN container locally
  
  + `rm -rf ~/.ern/containergen/out/android;`
  + `ern cauldron repo use AndroidCauldron && ern create-container --platform android -outDir ~/.ern/containergen/out/android`
  + `ern publish-container --containerPath ~/.ern/containergen/out/android --platform android --publisher maven -v 0.0.1`

4. Clone Native Android repo

  + `git clone git@github.com:noor-mohiuddin-agilea/ERNativeAndroid.git`

5. Run the cauldron

  + `ern start`
