# Adjustable Readable Line Length in Obsidian with Style Settings
This is a CSS [snippet](obsidian-vii-adjustable-readable-line-length.css) that will let you easily change the length used for the Readable Line Length Editor setting in Obsidian. You will need to have the [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) plugin installed and enabled in your vault in order to change the setting in-app. The plugin can be found in the Community Plugins inside of Obsidian, or you can manually install if you wish. If you choose not to use Style Settings, you'll be able to manually adjust the `--read-line-length` property in the snippet instead.  

By default, this snippet uses pixels as its unit, but you can change that in the snippet by changing the line `format: px` to some other unit, such as `format: vw`, and changing the property declaration in `body {}` to use the same unit. You probably should change the default value from 700 to something else, too 😅.

---
## Demo
![Demo](ARLL_StyleSettings.gif)
