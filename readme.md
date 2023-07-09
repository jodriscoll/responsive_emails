#### Email Template Repository
* Small repository of responsive and standard sized email templates built for clients

#### Name Format
* type-pixel-name

#### Type Key
* `resp` = responsive
* `stnd` = standard size (non-responsive)

#### Useful HTML Email Discoveries
* Check for non-HTML characters
 * Apostrophes, single & double quotes, bullet characters, etc
 * Do not copy/paste from Microsoft Word and ignore updating these characters
* Apply styling for containing cell text to the parent cell
 * `<td style=”font-size: 12px”>I should be 12 px</td>` instead of…
 * `<td><span style=”font-size: 12px”>I should be 12px</span></td>`
 * If the cell contains an ASCII character (such as &#149;), you may have to also wrap the text with a span
* Apply spacing for buttons on the containing TD cell
 * `<td style=”padding: 10px 12px;”>`
 * Be aware that Outlook 2013 is tempermental with using “padding: 10px 20px” as opposed to `“padding: 10px 20px 10px 20px”`
 * For Outlook 2013 (and essentially all clients), it’s best to create 
* Avoid scaling of images with Gmail (Android App) when width is > the screen resolution
 * If an image exceeds 350px in width, break it into two separate images to prevent the Gmail App on Android from scaling the image and breaking the template
* Outlook 2013 has issues with validating padding 
 * If an image exceeds 350px in width, break it into two separate images to prevent the Gmail App on Android from scaling the image and breaking the template
- Gmail App (Android) reformats your font-families regardless if you set it to !important or not
 * It will force the usage of ‘Roboto’ but stay true to your font size/color/etc
 * ‘Roboto’ is not a “fixed-font” and may cause formatting issues with your template
- Force Gmail App (Android) to not scale an email template easily
 * Add a single row at the top of the template with a spacer
 * Apply a width to the TD cell
 * Set a min-width on the image to prevent Gmail App scaling
  * Example:
   * `<tr><td height="1" width="560"><img src="https://s3.amazonaws.com/dh-ctc-rd2/spacer.gif" height="1" width="560" style="border: 0; display: block; min-width: 560px;"/></td></tr>`
* Bulletproof usage of preheader text
 * **CSS**
 * `.preheader {display: none !important; font-size: 0 !important; height: 0 !important; line-height: 0 !important; margin: 0 !important; max-height: 0 !important; mso-hide: all; opacity: 0 !important; padding: 0 !important; width: 0 !important;}`
 * **HTML**
 * `<table align="center" border="0" cellpadding="0" cellspacing="0" height="0" width="0" style="border: 0; height: 0; mso-hide: all; width: 0;">
  <tr>
    <td border="0" height="0" width="0" style="border: 0; height: 0; mso-hide: all; width: 0;">
      <span class="preheader" style="display: none !important; font-size: 0 !important; height: 0 !important; line-height: 0 !important; margin: 0 !important; max-height: 0 !important; mso-hide: all !important; opacity: 0 !important; padding: 0 !important; width: 0 !important;">Find top rated classes and degree programs in your area today. Our team reviews thousands of programs to find the best match for you.</span>
    </td>
  </tr>
</table>`
* If setting a border/border-radius on a table element, the border will not adhere to the border-radius in Explorer based environments
 * Example: [http://i.imgur.com/OT6VQp9.jpg](http://i.imgur.com/OT6VQp9.jpg)
  * [Litmus discussion on the bug](https://litmus.com/community/learning/28-pairing-border-size-style-color-with-border-radius-x-in-explorer-browsers)


#### Useful HTML Email Discoveries
- Check for non-HTML characters
-- Apostrophes, single & double quotes, bullet characters, etc
-- Do not copy/paste from Microsoft Word and ignore updating these characters
- Apply styling for containing cell text to the parent cell
-- `<td style=”font-size: 12px”>I should be 12 px</td>` instead of…
-- `<td><span style=”font-size: 12px”>I should be 12px</span></td>`
-- If the cell contains an ASCII character (such as &#149;), you may have to also wrap the text with a span
- Apply spacing for buttons on the containing TD cell
-- <td style=”padding: 10px 12px;”>
-- Be aware that Outlook 2013 is tempermental with using “padding: 10px 20px” as opposed to `“padding: 10px 20px 10px 20px”`
-- For Outlook 2013 (and essentially all clients), it’s best to create 
- Avoid scaling of images with Gmail (Android App) when width is > the screen resolution
-- If an image exceeds 350px in width, break it into two separate images to prevent the Gmail App on Android from scaling the image and breaking the template
- Outlook 2013 has issues with validating padding 
-- If an image exceeds 350px in width, break it into two separate images to prevent the Gmail App on Android from scaling the image and breaking the template
- Gmail App (Android) reformats your font-families regardless if you set it to !important or not
-- It will force the usage of ‘Roboto’ but stay true to your font size/color/etc
-- ‘Roboto’ is not a “fixed-font” and may cause formatting issues with your template
- Force Gmail App (Android) to not scale an email template easily
-- Add a single row at the top of the template with a spacer
-- Apply a width to the TD cell
-- Set a min-width on the image to prevent Gmail App scaling
--- Example:
---- `<tr><td height="1" width="560"><img src="https://s3.amazonaws.com/dh-ctc-rd2/spacer.gif" height="1" width="560" style="border: 0; display: block; min-width: 560px;"/></td></tr>`
- Bulletproof usage of preheader text
-- CSS
-- `.preheader {display: none !important; font-size: 0 !important; height: 0 !important; line-height: 0 !important; margin: 0 !important; max-height: 0 !important; mso-hide: all; opacity: 0 !important; padding: 0 !important; width: 0 !important;}`		
-- HTML
-- `<table align="center" border="0" cellpadding="0" cellspacing="0" height="0" width="0" style="border: 0; height: 0; mso-hide: all; width: 0;">
  <tr>
    <td border="0" height="0" width="0" style="border: 0; height: 0; mso-hide: all; width: 0;">
      <span class="preheader" style="display: none !important; font-size: 0 !important; height: 0 !important; line-height: 0 !important; margin: 0 !important; max-height: 0 !important; mso-hide: all !important; opacity: 0 !important; padding: 0 !important; width: 0 !important;">Find top rated classes and degree programs in your area today. Our team reviews thousands of programs to find the best match for you.</span>
    </td>
  </tr>
</table>`
-If setting a border/border-radius on a table element, the border will not adhere to the border-radius in Explorer based environments
-- Example: http://i.imgur.com/OT6VQp9.jpg
--- Litmus discussion on the bug


