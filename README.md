# Student Profile Card

This is a simple profile card project built with HTML, CSS, and JavaScript.

## Project Files

- index.html: Page structure
- style.css: Design and styling
- script.js: Profile data, image file name, and quote logic

## What You Need To Do

Follow these steps to customize the card with your own information.

## 1) Upload Your Picture

- Put your image file inside this same folder (the project root).
- Open script.js.
- Find this variable:

```js
const profileImageFile = 'userprofilepic.jpg';
```

- Replace userprofilepic.jpg with your actual file name.

Examples:

- myphoto.jpg
- profile.png
- pic.webp

Important:

- File name must match exactly (including extension and uppercase/lowercase).
- The image file must be in the same folder as index.html.

## 2) Add Your Personal Details

- Open script.js.
- Find the myInfo object and update all fields:

```js
const myInfo = {
  name: 'Your Name',
  tagline: 'Your Tagline',
  roll: 'Your ID / Roll Number',
  department: 'Your Department',
  year: 'Your Year',
  email: 'your.email@example.com',
  gpa: '0.00'
};
```

- Replace values with your own details.

 

## Troubleshooting

If image is not loading:

- Check file name spelling in profileImageFile.
- Check image extension (.jpg, .jpeg, .png, .webp).
- Make sure file is in the project root folder.

If details are not updating:

- Confirm you edited myInfo in script.js.
- Refresh the browser after saving.

## Current Default Values

- Image file: userprofilepic.jpg
- Name: Your Name
- Tagline: Your Tagline
- Roll: Your ID / Roll Number
- Department: Your Department
- Year: Your Year
- Email: your.email@example.com
- GPA: 0.00
