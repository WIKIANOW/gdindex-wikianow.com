# Google Drive Index + Dark mode
![Preview](https://raw.githubusercontent.com/cheems/GDIndex/master/images/preview.png)
## Features
 
 - Video Player - | mp4 | webm | avi | mpg | mpeg | mkv | rm | rmvb | mov | wmv | asf | ts | flv
 - Music Player - | mp3 | flac | wav | ogg | m4a
 - Document Viewer - | html | php | css | go | java | js | json | txt | sh | md | pdf
 - Image Viewer - | bmp | jpg | jpeg | png | gif
 - Multi-level Search within default and team/shared drives
 - Multi drive encryption
 - Mobile Friendly
 - Page-level caching, browser forward and backward without reloading
 - Dark Theme
 - Main Color:
	 - red | pink | purple | deep-purple | indigo | blue | light-blue | 
   cyan    | teal | green | light-green | lime yellow | amber orange | 
   deep-orange | brown | greyblue-grey
  - Accent Color:
	  -   red | pink | purple | deep-purple | indigo | blue | light-blue | cyan | teal | green | light-green | lime | yellow | amber | orange | deep-orange
## Deployment

1. Open https://console.cloud.google.com/marketplace/product/google/drive.googleapis.com<br>
2. Create a new project or use one of the existing projects if you already have created. (If you are using Google Cloud Platform for the 1st time: do this only if you want to give your project a custom name. otherwise, your project will be automatically created after the next step with the name "My First Project". If you don't care about the name of the project like me then just skip this step)<br>
3. Click Enable button to enable Google Drive API<br>
4. Click Create Credentials<br>
5. Select "Google Drive API" from the 1st dropdown and select "Other UI" from the 2nd dropdown<br>
6. Select "User data" from radio buttons<br>
7. Click "What credentials do I need" then, a pop-up will appear saying that you need to set up the Consent Screen.<br>
8. click "set up consent screen". it will take you to a new tab<br>
9. Select "External" as the user type and click create<br>
10. Provide app name, User support email, and developer contact information which are required for the consent screen. then finish creating the consent screen.<br>
11. After creating the consent screen, click publish app. (This option can be found under Publishing status)<br>
12. Head back to the previous tab to continue creating credentials<br>
13. Click on refresh and create OAuth client ID then click Done<br>
14. Click on newly created OAuth Client ID to see client id and secret<br>
15. Open the below Colab notebook(which is made for the ones who wish to use their own credentials) in a new tab<br>
<p><a href="https://colab.research.google.com/github/WIKIANOW/gdindex-wikianow.com/blob/master/template/GDIndex_Code_Generator_with_custom_credentials.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="OPEN IN COLAB"/></a></p>
16. Copy your client id and client secret into the Colab notebook and fill the fields in it on your choice and run the cell<br>
17. Download the txt file with the code generated by the notebook<br>
18. Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)<br>

### Extra Options
``` js
const uiConfig = {
  .......
  "hide_madewithlove": false, // Set this to true if you want to hide made-with-love text at the bottom of the page.
  "helpURL": "", // Provide the URL of the help page(instructions for using the index). Leave this empty if you want to hide the help icon. Providing a URL will open the help page in a new tab. (You can use telegra.ph to write instructions)
  .......
};
```
