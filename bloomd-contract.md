# The .bloomd as understood by BloomReader-RN

This is a document to keep track of the assumptions I am making about .bloomd files as I'm working on BloomReader-RN. This can then either be or feed into some kind of common spec for both Desktop and Mobile developers to use to ensure compatability.

## Extension

The file extension is ".bloomd". We don't check for ".BLOOMD" or any other variant. The file extension is how we communicate to Android that BloomReader is the app that can handle this kind of file.

## Mime Type

We also register the filetype by MIME type as either "application/bloom" or "application/vnd.bloom". 

## Contents

The .bloomd is a Zip archive with the following contents:

 - A single html file. 
    - Normally the filename is name of the book with the extension ".htm". 
    - Because there is only one html file, BloomReader simply chooses whichever file has the .htm(l) extension.
 - The assets needed by the html file, images and other media
 - Optionally a thumbnail
    - The filename is "thumbnail" plus an appropriate extension
    - The format is PNG or JPG
    - The extension needs to match the format (".png" or ".jpg")
    - Dimensions? (Right now I have BR displaying 70x57 which came from the Moon & Cap thumbnail dimensions)

## We should also talk about MetaData, but I haven't got to that yet

    