# HTML Tag for Tooltip

## Introduction to HTML

HTML stands for **Hypertext Markup Language**. There are different components of HTML that make up a web page. The HTML element is the main structural unit of the web page. HTML tags are used to define the elements and provide structure to the content of the website. HTML attributes provide additional information about the elements. This article will focus on HTML tags, specifically those that can be used for Tooltips on the PrintVis Planning Board and Shop Floor Job.

## HTML Tags

| **HTML Tag** | **Functionality** | **End Tag** | **Example** | **Comments** |
|--------------|-------------------|-------------|-------------|--------------|
| `<b>` | Bold | `</b>` | `<b>Bold Text</b>` |  |
| `<i>` | Italic | `</i>` | `<i>Italic Text</i>` |  |
| `<br>` | Line Break | N/A | `<br>` | Adds extra line space between tooltip lines. |
| `<u>` | Underline | `</u>` | `<u>Underlined Text</u>` |  |
| `<small>` | Smaller text | `</small>` | `<small>Smaller Text</small>` |  |
| `<big>` | Bigger text | `</big>` | `<big>Bigger Text</big>` |  |
| `<span style="color:...">` | Changes font color | `</span>` | `<span style="color:tomato">Colored Text</span>` or `<span style="color:#FF6347">` | Use color name or hex value. |
| `<span style="font-size:...">` | Changes font size | `</span>` | `<span style="font-size:11px">Sized Text</span>` | Type desired font size in pixels. |
| `<span style="font-family:...">` | Changes font type | `</span>` | `<span style="font-family:verdana">Font Text</span>` | Use common font family names. |
| `<span style="background-color:...">` | Highlights text | `</span>` | `<span style="background-color:red">Highlighted Text</span>` | Choose any valid color. |
| `<span style="...; ...;">` | Combine styles | `</span>` | `<span style="font-family:fantasy; color:tomato; font-size:15px">Styled Text</span>` | Separate multiple styles with semicolons. |


 Links for Reference
- [HTML Color Names (w3schools.com)](https://www.w3schools.com/colors/colors_names.asp)
- [HTML Color Values (w3schools.com)](https://www.w3schools.com/colors/colors_picker.asp)
- [Common Font Families](https://www.hostinger.com/tutorials/best-html-web-fonts)

## Example of Tooltips

Below are examples of the text setup for the Tooltip and how the Tooltip appears after designing the line of text. Note: All examples will have the same setup for the line text. The only information that is changing is the Text field.

**Table No:** 6010318  
**Table Name:** Sheet  
**Field No:** 21  

### Text Colors

**Text field:**
- Using text value for color: `<span style="color:tomato"> Sheet Width: %1 </span>`
- Using hex value for color: `<span style="color:#FF6347"> Sheet Width: %1 </span>`

![HTML Tag for Tooltip 1.jpg](./assets/HTML Tag for Tooltip 1.jpg)

### Text Size

**Text field:** `<span style="font-size:20px"> Sheet Width: %1 </span>`

![HTML Tag for Tooltip 2.jpg](./assets/HTML Tag for Tooltip 2.jpg)

### Text Style (Family)

**Text field:** `<span style="font-family:fantasy"> Sheet Width: %1 </span>`

![HTML Tag for Tooltip 3.jpg](./assets/HTML Tag for Tooltip 3.jpg)

### Text Highlighting

**Text field:**
- Using text value for color: `<span style="background-color:red"> Sheet Width: %1 </span>`
- Using hex value for color: `<span style="background-color:#FF0000"> Sheet Width: %1 </span>`

![HTML Tag for Tooltip 4.jpg](./assets/HTML Tag for Tooltip 4.jpg)

### Combining Multiple HTML Tags

**Note:** This is an example of combining multiple text modifications that would require span style to make changes. Bold, italic, underline, etc., can simply have `<i><b>` or any combination next to each other.

**Text field:** `<span style="font-family:fantasy; color:tomato; font-size:15px"> Sheet Width %1 </span>`

![HTML Tag for Tooltip 5.jpg](./assets/HTML Tag for Tooltip 5.jpg)
