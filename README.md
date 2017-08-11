#I practically invented this <HRDextension> 
This is a quick and dirty chrome extension boilerplate for Harrison to do stuff with

##@Harrison, things to know
To set up the extension:
1) go to chrome://extensions
2) load unpacked extensions
3) select this parent folder 

####manifest.json 
This file is for setting up the extension with chrome and it handles the extension metadata, file structure, permissions, behaviors, applicable urls, and icons. The information for this file can be found here: 
https://developer.chrome.com/extensions/manifest

####user_alert.js
This file contains the actions made when the urls matched from the manifest are visite. Customize this to trigger on the pages you want it to run. This format has a regex feel to it and can be seen here: https://developer.chrome.com/extensions/match_patterns

Currently used is <all_urls> which is just a macro for every url. 

####toastr.min.js & toastr.min.css
I chose this to be a nice, effective way of doing what you were looking for. This and options around this can be modified to your liking. Modifying the address bar is not exposed with the API for Chrome (that I know of), but here is a simple solution.
"toastr is a Javascript library for non-blocking notifications. jQuery is required. The goal is to create a simple core library that can be customized and extended." This information can be found here: https://github.com/CodeSeven/toastr

####jquery.min.js
This is a common Javascript library and included because it is a dependency of toastr. If you decide to not use toastr, you can remove this from the manifest and the extension package
