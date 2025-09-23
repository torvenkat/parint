---
date: 2025-09-19
title: Mac Quick Action convert image to webp
tags:
  - macos
---
I have been using webp format for images for quite sometime now.  While it is easy to convert _webp_ format images to _jpg_ or _png_ using Automator Quick Action in mac, going the other way is not straightforward.  Mac does not support converting to _webp_ in preview and one may need a third-party utility/app to do that.  I was waiting for the release of MacOS Tahoe to see if this will be natively supported, but it was futile.   So, I went ahead and set up a Quick Action to convert to webp.  It can be done as follows; 

Open Automator, in the right hand side panel select 

_Workflow receives current > Image file_  and _in > Finder app_

I just left the image icon to Action and Color as Black

 Then in the left hand side search for _Run Shell Script_ and drag and drop that to the the automator window.   Select shell: _/bin/zsh_ and Pass input _as arguments_ (to receive the file selected with the right click as the input for the shell script).

After that paste the following snippet 

```zsh
for file
do
  /opt/homebrew/bin/cwebp -lossless -quiet "$file" -o "${file%.*}.webp"
  rm "$file"
done
```

Save this Quick Action as  "Convert image to webp".

![[webp_convert.webp]]

Now, in the Finder, right click the file (jpg or png) and Quick Actions > Convert Image to webp to convert the image file to _webp_ format.

Note: The original image will be deleted in this Quick Action (which is what I prefer).  But if you want to keep it you may remove  `rm "$file"`in the above shell script. 


