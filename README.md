# Youtube Subscriptions Transfer
![logo](/src/assets/icons/icon128.png)

YouTube Subscriptions Transfer is a browser extension that allows you to transfer subscriptions from one account to another without using any API. The extension collects a list of channels and enables you to subscribe or unsubscribe to each channel. It interacts with the DOM using xpath.



## Installation 
<a href="https://microsoftedge.microsoft.com/addons/detail/ojnekffpabpincdklmmmlnoanffkfahj">
  <img src="https://get.microsoft.com/images/en-us%20dark.svg" alt="Get YST on Microsoft Edge" width="224px">
</a>

Or get the built zip from the [release](https://github.com/biplobsd/yst/releases/latest) tab. Then follow the instructions in the [Load unpacked extensions](#load-unpacked-extensions) section. The ***/dist*** folder should be considered as the unpacked zip files.

## Usages 
To use the extension, open the Y (yst) icon from the extension panel. If you are not on the https://www.youtube.com page, click the Open YouTube button.

![Options](https://user-images.githubusercontent.com/43641536/225968066-01278b17-4ea8-4fd5-954c-525c2a8cc0bd.png)

Wait for the page to load completely and wait for the Ready for accept request signal from the content script. Once connected, the options will look like the screenshot below.

![First time view](https://user-images.githubusercontent.com/43641536/225969173-5372d3ee-8a00-4204-9922-886fdea2ec37.png)

### Data section
In the Data section, you can see how many subscriptions the extension has collected. If you expand the subscriptions, you will see all the channel IDs. You can also add, remove, or update this list and take action from this list.

![Data section](https://user-images.githubusercontent.com/43641536/225971299-38607a74-eee1-488e-acf2-3b18ba99d2de.png)

### Actions
- Collect channel
  > This button will collect all subscriptions from your current active tab on YouTube and save them to the Data section.
- Subscribe 
  > This button first collects all of your current subscriptions and compares them with the past data from the Data section. If any of the IDs are present in your current subscriptions, the ID is removed from the subscriptions list.
- Unsubscribe 
  > This button first collects your subscriptions and compares them with the past data. If any of the IDs are present in your current subscription list, the ID remains on the list.
- Stop
  > This button will appear when any action is running. You can click it to stop the current task.

 The Subscribe and Unsubscribe buttons will only appear when the Subscriptions list is not empty
 
![Actions active](https://user-images.githubusercontent.com/43641536/225979057-af78429a-d0a1-40d2-9704-ba2f9ec66ec8.png)

## Development

```bash
# install dependencies
npm i

# build files to `/dist` directory
# HMR for extension pages and content scripts
npm run dev
```

## Build

```bash
# build files to `/dist` directory
$ npm run build
```

## Load unpacked extensions

[Getting Started Tutorial](https://developer.chrome.com/docs/extensions/mv3/getstarted/)

1. Open the Extension Management page by navigating to `chrome://extensions`.
2. Enable Developer Mode by clicking the toggle switch next to `Developer mode`.
3. Click the `LOAD UNPACKED` button and select the `/dist` directory.

![Example](https://wd.imgix.net/image/BhuKGJaIeLNPW9ehns59NfwqKxF2/vOu7iPbaapkALed96rzN.png?auto=format&w=571)
