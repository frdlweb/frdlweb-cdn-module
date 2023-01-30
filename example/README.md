# CND-Racer Fallback Example
Please read the [readme at github](https://github.com/frdlweb/frdlweb-cdn-module/blob/main/README.md)!

* This example directory demonstrates the usage within a subdirectory of the DOCUMENT_ROOT directory.
* This readme file demonstrates an existing local file.
* Although it may be shown in this example for convenience, you SHOULD **NOT**:
  * Do **not** use this directory as a "local directory" Adapter, as it may be
    - not secure
    - is the DOCUMENT_ROOT already
    Instead use "local directory" Adapters OUTSIDE the public web directory!
  * Do **not** use this directory to store files cached or downloaded by the proxy for the same reason above.
    Instead use "local directory" Adapters OUTSIDE the public web directory!
