# frdlweb-cdn-module
Proxies the Frdlweb CDN and caches/saves locally into your cdn/assets directory.
So, if the file is not found in your local project, it lloks up at Frdlweb CDN.

## Installation
* Create a directory in your web-root, e.g. "/my-assets".
* Copy the [the files](https://github.com/frdlweb/frdlweb-cdn-module/archive/refs/heads/main.zip) into this new created directory.
* Edit the [config section](https://github.com/frdlweb/frdlweb-cdn-module/blob/main/cdn.php#L2348) if required:
  ````PHP 
    'FRDL_UPDATE_CHANNEL' => 'latest', // latest | stable		
    'FRDL_CDN_HOST'=>'cdn.webfan.de',  // cdn.webfan.de | cdn.frdl.de 		
    'FRDL_CDN_PROXY_REMOVE_QUERY'=>	true,     
    'FRDL_CDN_SAVING_METHODS'=>	['GET'],  //Only save files to disk, if Request-Methods...
  ````

## Prune files
* Provide the sha1 hash of the YOUR_KEY and the required cache time in [the config of cdn.php](https://github.com/frdlweb/frdlweb-cdn-module/blob/main/cdn.php#L2333)
* Call https://example.com/your-assets-path/cdn.php?web=cron.php&key=YOUR_KEY e.g. by a cronjob
