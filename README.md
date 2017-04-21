### Downloader Cordova Download Plugin

Cordova plugin for downloading files from server.

### Supported Platforms

- Android
- iOS

### Installation

This requires Phonegap / Cordova CLI 3.0 +

- Cordova CLI

```sh
cordova plugin add https://github.com/Whebcraft/cordova-plugin-downloader
```


- Phonegap Build

```sh
    <plugin spec="https://github.com/Whebcraft/cordova-plugin-downloader.git" source="git" />
```

### Usage

```js
var Downloader = window.plugins.Downloader;

var downloadSuccessCallback = function(folder) {
    
};

var downloadErrorCallback = function(error) {
    //error: string
};

var options = {
    title: 'Downloading...', // Download Notification Title
    description: 'The pdf file is downloading', // Download description Notification String
    url: "http://www.website.com/file.pdf", // File Url
    path: "My Pdf.pdf" // The File Name
}

Downloader.download(options, downloadSuccessCallback, downloadErrorCallback);
```

### Get download folder
Where the file has been downloaded

This is usually in app folder.

Internal storage `file:///storage/sdcard0/Android/data/YOUR.APP.ID/files/Download/THE-FILE-NAME`

`Or`

SD Card `file:///storage/sdcard1/Android/data/YOUR.APP.ID/files/Download/THE-FILE-NAME`

The ressource will be downloaded within the application's external files directory.

WARNING: `will not overwrite existing file if it already exists.`

License
--------

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
