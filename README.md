# Complete Appium Capabilities Reference

> A comprehensive list of all Appium capabilities across different drivers and platforms for Appium 2.0+

## Table of Contents

- [Standard W3C WebDriver Capabilities](#standard-w3c-webdriver-capabilities)
- [Global Appium Capabilities](#global-appium-capabilities)
- [iOS XCUITest Driver Capabilities](#ios-xcuitest-driver-capabilities)
- [Android UIAutomator2 Driver Capabilities](#android-uiautomator2-driver-capabilities)
- [Windows Driver Capabilities](#windows-driver-capabilities)
- [Mac Driver Capabilities](#mac-driver-capabilities)
- [Browser Driver Capabilities](#browser-driver-capabilities)
- [Cloud Provider Capabilities](#cloud-provider-capabilities)
- [Advanced Capabilities](#advanced-and-experimental-capabilities)
- [Usage Examples](#usage-examples)

## Standard W3C WebDriver Capabilities

These are the standard capabilities defined by the W3C WebDriver specification:

| Capability | Type | Description |
|------------|------|-------------|
| `browserName` | string | The name of the browser to launch and automate |
| `browserVersion` | string | The specific version of the browser |
| `platformName` | string | The type of platform hosting the browser/app |
| `acceptInsecureCerts` | boolean | Whether untrusted and self-signed TLS certificates should be accepted |
| `pageLoadStrategy` | string | The page loading strategy to use (`normal`, `eager`, `none`) |
| `proxy` | object | Proxy configuration |
| `setWindowRect` | boolean | Whether browser supports resizing and repositioning |
| `timeouts` | object | Session timeout configuration |
| `strictFileInteractability` | boolean | Whether strict file interactability is enabled |
| `unhandledPromptBehavior` | string | How to handle unexpected alerts |

## Global Appium Capabilities

These capabilities are recognized by all Appium drivers:

| Capability | Type | Required | Description |
|------------|------|----------|-------------|
| `platformName` | string | ✅ | The type of platform hosting the app or browser |
| `appium:automationName` | string | ✅ | The name of the Appium driver to use |
| `appium:app` | string | | The path to an installable application |
| `appium:deviceName` | string | | The name of a particular device to automate |
| `appium:platformVersion` | string | | The version of a platform |
| `appium:newCommandTimeout` | number | | Timeout in seconds for client commands |
| `appium:noReset` | boolean | | Avoid reset logic during session start |
| `appium:fullReset` | boolean | | Perform additional reset steps |
| `appium:eventTimings` | boolean | | Collect timing information for events |
| `appium:printPageSourceOnFindFailure` | boolean | | Print page source when element find fails |
| `appium:connectHardwareKeyboard` | boolean | | Connect hardware keyboard (iOS) |
| `appium:orientation` | string | | Initial device orientation |
| `appium:autoWebview` | boolean | | Automatically switch to webview context |
| `appium:language` | string | | Language for the session |
| `appium:locale` | string | | Locale for the session |
| `appium:udid` | string | | Unique device identifier |
| `appium:autoLaunch` | boolean | | Automatically launch the app |
| `appium:autoGrantPermissions` | boolean | | Automatically grant all permissions |
| `appium:otherApps` | array | | Array of apps to install alongside main app |

## iOS XCUITest Driver Capabilities

### General iOS Capabilities

| Capability | Type | Description |
|------------|------|-------------|
| `appium:bundleId` | string | Bundle ID of the app to launch |
| `appium:xcodeOrgId` | string | Apple developer team identifier |
| `appium:xcodeSigningId` | string | Certificate name for app signing |
| `appium:updatedWDABundleId` | string | Bundle ID for WebDriverAgent |
| `appium:derivedDataPath` | string | Custom derived data path |
| `appium:useNewWDA` | boolean | Use fresh WebDriverAgent for each session |
| `appium:wdaLaunchTimeout` | number | Timeout for WebDriverAgent launch |
| `appium:wdaConnectionTimeout` | number | Timeout for WebDriverAgent connection |
| `appium:iosInstallPause` | number | Pause between app installation steps |
| `appium:autoAcceptAlerts` | boolean | Automatically accept all alerts |
| `appium:autoDismissAlerts` | boolean | Automatically dismiss all alerts |
| `appium:nativeInstrumentsLib` | boolean | Use native instruments library |
| `appium:nativeWebTap` | boolean | Use native tap for web elements |
| `appium:safariInitialUrl` | string | Initial URL when launching Safari |
| `appium:safariAllowPopups` | boolean | Allow popups in Safari |
| `appium:safariIgnoreFraudWarning` | boolean | Ignore fraud warnings in Safari |
| `appium:safariOpenLinksInBackground` | boolean | Open links in background |
| `appium:keepKeyChains` | boolean | Keep keychains between sessions |
| `appium:localizableStringsDir` | string | Directory for localizable strings |
| `appium:processArguments` | object | Arguments to pass to app process |
| `appium:interKeyDelay` | number | Delay between keystrokes |
| `appium:showIOSLog` | boolean | Show iOS system log |
| `appium:sendKeyStrategy` | string | Strategy for sending keys |
| `appium:screenshotWaitTimeout` | number | Timeout for screenshot capture |
| `appium:waitForAppScript` | string | Script to wait for app launch |

### iOS Simulator Specific

| Capability | Type | Description |
|------------|------|-------------|
| `appium:wdaLocalPort` | number | Local port for WebDriverAgent |
| `appium:wdaBaseUrl` | string | Base URL for WebDriverAgent |
| `appium:resetOnSessionStartOnly` | boolean | Reset only at session start |
| `appium:commandTimeouts` | object | Custom command timeouts |
| `appium:wdaEventloopIdleDelay` | number | WebDriverAgent event loop delay |
| `appium:usePrebuiltWDA` | boolean | Use prebuilt WebDriverAgent |
| `appium:preventWDAAttachments` | boolean | Prevent WDA from creating attachments |
| `appium:webDriverAgentUrl` | string | Custom WebDriverAgent URL |
| `appium:simpleIsVisibleCheck` | boolean | Use simple visibility check |

### iOS Real Device Specific

| Capability | Type | Description |
|------------|------|-------------|
| `appium:xcodeOrgId` | string | Development team ID |
| `appium:xcodeSigningId` | string | Signing identity |
| `appium:keychainPath` | string | Path to keychain |
| `appium:keychainPassword` | string | Keychain password |
| `appium:wdaStartupRetries` | number | WebDriverAgent startup retry count |
| `appium:wdaStartupRetryInterval` | number | Retry interval in ms |
| `appium:wdaRemotePort` | number | Remote port for WebDriverAgent |

## Android UIAutomator2 Driver Capabilities

### General Android Capabilities

| Capability | Type | Description |
|------------|------|-------------|
| `appium:appPackage` | string | Java package of the app |
| `appium:appActivity` | string | Activity name for the Android activity |
| `appium:appWaitActivity` | string | Activity to wait for |
| `appium:appWaitPackage` | string | Package to wait for |
| `appium:appWaitDuration` | number | Timeout in ms to wait for activity |
| `appium:deviceReadyTimeout` | number | Timeout for device ready |
| `appium:androidCoverage` | string | Instrumentation class for coverage |
| `appium:androidCoverageEndIntent` | string | Intent to broadcast when coverage ends |
| `appium:androidDeviceReadyTimeout` | number | Device ready timeout |
| `appium:androidInstallTimeout` | number | App installation timeout |
| `appium:adbPort` | number | ADB server port |
| `appium:systemPort` | number | System port used by UIAutomator2 |
| `appium:remoteAdbHost` | string | Remote ADB host |
| `appium:androidDeviceSocket` | string | Device socket for ADB connection |
| `appium:avd` | string | Android Virtual Device name |
| `appium:avdLaunchTimeout` | number | AVD launch timeout |
| `appium:avdReadyTimeout` | number | AVD ready timeout |
| `appium:avdArgs` | string | Additional AVD arguments |
| `appium:useKeystore` | boolean | Use custom keystore |
| `appium:keystorePath` | string | Path to keystore |
| `appium:keystorePassword` | string | Keystore password |
| `appium:keyAlias` | string | Key alias |
| `appium:keyPassword` | string | Key password |
| `appium:chromedriverExecutable` | string | Path to ChromeDriver |
| `appium:autoWebviewTimeout` | number | Timeout for webview detection |
| `appium:intentAction` | string | Intent action for app launch |
| `appium:intentCategory` | string | Intent category |
| `appium:intentFlags` | string | Intent flags |
| `appium:optionalIntentArguments` | string | Optional intent arguments |
| `appium:dontStopAppOnReset` | boolean | Don't stop app on reset |
| `appium:unicodeKeyboard` | boolean | Enable Unicode keyboard |
| `appium:resetKeyboard` | boolean | Reset keyboard after session |
| `appium:noSign` | boolean | Skip app signing |
| `appium:ignoreUnimportantViews` | boolean | Ignore unimportant views |
| `appium:disableAndroidWatchers` | boolean | Disable Android watchers |
| `appium:chromeLoggingPrefs` | object | Chrome logging preferences |
| `appium:recreateChromeDriverSessions` | boolean | Recreate ChromeDriver sessions |
| `appium:nativeWebScreenshot` | boolean | Use native screenshot for webviews |
| `appium:androidScreenshotPath` | string | Path for screenshots |

### Android Espresso Driver Capabilities

| Capability | Type | Description |
|------------|------|-------------|
| `appium:espressoServerPort` | number | Port for Espresso server |
| `appium:espressoBuildConfig` | string | Espresso build configuration |
| `appium:showGradleLog` | boolean | Show Gradle build logs |
| `appium:skipServerInstallation` | boolean | Skip server installation |
| `appium:espressoServerLaunchTimeout` | number | Server launch timeout |

## Windows Driver Capabilities

| Capability | Type | Description |
|------------|------|-------------|
| `appium:app` | string | Application path or identifier |
| `appium:appArguments` | string | Arguments for application |
| `appium:appTopLevelWindow` | string | Top level window class name |
| `appium:appWorkingDir` | string | Working directory for app |
| `appium:createSessionTimeout` | number | Session creation timeout |
| `appium:ms:experimental-webdriver` | boolean | Enable experimental features |
| `appium:ms:waitForAppLaunch` | number | Wait time for app launch |

## Mac Driver Capabilities

| Capability | Type | Description |
|------------|------|-------------|
| `appium:bundleId` | string | Bundle ID of macOS app |
| `appium:prerun` | object | Pre-run script configuration |
| `appium:postrun` | object | Post-run script configuration |
| `appium:skipAppKill` | boolean | Skip killing app on session end |

## Browser Driver Capabilities

### Gecko (Firefox) Driver

| Capability | Type | Description |
|------------|------|-------------|
| `moz:firefoxOptions` | object | Firefox-specific options |
| `moz:useNonSpecCompliantPointerOrigin` | boolean | Use non-spec pointer origin |
| `moz:webdriverClick` | boolean | Use WebDriver click implementation |

### Safari Driver

| Capability | Type | Description |
|------------|------|-------------|
| `safari:useSimulator` | boolean | Use iOS Simulator |
| `safari:deviceType` | string | Device type for iOS Simulator |
| `safari:deviceName` | string | Device name for iOS Simulator |
| `safari:deviceUDID` | string | Device UDID |
| `safari:platformVersion` | string | Platform version |
| `safari:automaticInspection` | boolean | Enable automatic inspection |
| `safari:automaticProfiling` | boolean | Enable automatic profiling |

## Specialized Driver Capabilities

### YouiEngine Driver

| Capability | Type | Description |
|------------|------|-------------|
| `appium:youiEngineAppAddress` | string | You.i Engine app address |
| `appium:youiEngineAppPort` | number | You.i Engine app port |

### Flutter Driver

| Capability | Type | Description |
|------------|------|-------------|
| `appium:retryBackoffTime` | number | Retry backoff time |
| `appium:maxRetryCount` | number | Maximum retry count |
| `appium:observatoryWsUri` | string | Observatory WebSocket URI |

## Cloud Provider Capabilities

### BrowserStack

| Capability | Type | Description |
|------------|------|-------------|
| `bstack:options` | object | BrowserStack specific options |
| `browserstack.user` | string | BrowserStack username |
| `browserstack.key` | string | BrowserStack access key |
| `browserstack.debug` | boolean | Enable debug mode |
| `browserstack.video` | boolean | Enable video recording |
| `browserstack.networkLogs` | boolean | Enable network logs |

### Sauce Labs

| Capability | Type | Description |
|------------|------|-------------|
| `sauce:options` | object | Sauce Labs specific options |
| `username` | string | Sauce Labs username |
| `accessKey` | string | Sauce Labs access key |
| `build` | string | Build identifier |
| `name` | string | Test name |
| `tags` | array | Test tags |

### LambdaTest

| Capability | Type | Description |
|------------|------|-------------|
| `lt:options` | object | LambdaTest specific options |
| `user` | string | LambdaTest username |
| `accessKey` | string | LambdaTest access key |
| `build` | string | Build name |
| `name` | string | Test name |
| `video` | boolean | Enable video recording |
| `network` | boolean | Enable network logs |
| `console` | boolean | Enable console logs |
| `visual` | boolean | Enable visual logs |

## Advanced and Experimental Capabilities

| Capability | Type | Description |
|------------|------|-------------|
| `appium:enforceAppInstall` | boolean | Force app installation |
| `appium:autoWebviewTimeout` | number | Webview detection timeout |
| `appium:ensureWebviewsHavePages` | boolean | Ensure webviews have pages |
| `appium:enablePerformanceLogging` | boolean | Enable performance logging |
| `appium:enableAsyncExecuteFromHttps` | boolean | Enable async execute from HTTPS |
| `appium:skipLogcatCapture` | boolean | Skip logcat capture |
| `appium:suppressKillServer` | boolean | Suppress kill server |
| `appium:waitForQuiescence` | boolean | Wait for UI quiescence |
| `appium:maxTypingFrequency` | number | Maximum typing frequency |
| `appium:useJSONSource` | boolean | Use JSON source format |
| `appium:waitForIdleTimeout` | number | Wait for idle timeout |
| `appium:disableIdLocatorAutocompletion` | boolean | Disable ID locator autocompletion |
| `appium:shouldTerminateApp` | boolean | Terminate app on session end |
| `appium:forceAppLaunch` | boolean | Force app launch |
| `appium:useNativeCachingStrategy` | boolean | Use native caching strategy |
| `appium:shouldUseSingletonTestManager` | boolean | Use singleton test manager |
| `appium:maxDepth` | number | Maximum depth for element search |
| `appium:forceSimulatorSoftwareKeyboardPresence` | boolean | Force software keyboard |

## Usage Examples

### Basic iOS Example

```json
{
  "platformName": "iOS",
  "appium:automationName": "XCUITest",
  "appium:deviceName": "iPhone 14",
  "appium:platformVersion": "16.0",
  "appium:app": "/path/to/app.app",
  "appium:noReset": true
}
```

### Basic Android Example

```json
{
  "platformName": "Android",
  "appium:automationName": "UIAutomator2",
  "appium:deviceName": "Android Emulator",
  "appium:appPackage": "com.example.app",
  "appium:appActivity": "MainActivity",
  "appium:autoGrantPermissions": true
}
```

### Using appium:options

```json
{
  "platformName": "iOS",
  "appium:options": {
    "automationName": "XCUITest",
    "deviceName": "iPhone 14",
    "platformVersion": "16.0",
    "app": "/path/to/app.app",
    "noReset": true,
    "autoAcceptAlerts": true
  }
}
```

### Cloud Provider Example (BrowserStack)

```json
{
  "platformName": "iOS",
  "appium:deviceName": "iPhone 14",
  "appium:platformVersion": "16.0",
  "appium:app": "bs://app-id",
  "bstack:options": {
    "userName": "your-username",
    "accessKey": "your-access-key",
    "projectName": "My Project",
    "buildName": "Build 1.0",
    "sessionName": "Test Session",
    "debug": true,
    "networkLogs": true
  }
}
```

## Important Notes

- **Appium 2.0+**: This list is for Appium 2.0 and later versions
- **Driver-Specific**: Many capabilities are specific to particular drivers
- **Version Dependencies**: Some capabilities may only be available in specific versions
- **Platform Constraints**: Certain capabilities only work on specific platforms
- **Cloud Providers**: Additional capabilities available when using cloud services
- **Custom Drivers**: Third-party drivers may introduce their own capabilities
- **Deprecation**: Some capabilities may be deprecated in newer versions

## Contributing

Found a missing capability or error? Please contribute by:
1. Opening an issue
2. Submitting a pull request
3. Checking the official [Appium documentation](https://appium.io/docs/en/latest/)

## Resources

- [Official Appium Capabilities Documentation](https://appium.io/docs/en/2.0/guides/caps/)
- [Appium GitHub Repository](https://github.com/appium/appium)
- [W3C WebDriver Specification](https://w3c.github.io/webdriver/#capabilities)

---

*Last updated: June 2025*
