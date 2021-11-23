# Guide For GDTOT Module

### > Follow These Steps to get cookies for GDTOT Module

1) Login / Signup 

2) Copy this code and paste in search box / bar of your browser
  - Note : After pasting the code check in the starting of code if <code>javascript:</code> is not there then kindly add it as shown below.
```
javascript:(function () {
  const input = document.createElement('input');
  input.value = JSON.stringify({url : window.location.href, cookie : document.cookie});
  document.body.appendChild(input);
  input.focus();
  input.select();
  var result = document.execCommand('copy');
  document.body.removeChild(input);
  if(result)
    alert('Cookie copied to clipboard');
  else
    prompt('Failed to copy cookie. Manually copy below cookie\n\n', input.value);   
})();
```
After pressing enter your browser will prompt a alert like this:<br>
![Alert Prompt](https://telegra.ph/file/ac467c05ec9715559fe9c.png)<br>

3) Now you'll get this type of data in your clipboard
```
{"url":"https://new.gdtot.org/","cookie":"PHPSESSID=k2xxxxxxxxxxxxxxxxxxxxj63o; crypt=NGxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxWdSVT0%3D"}
```
> From this you have to paste value of <code>PHPSESSID</code> & <code>crypt</code> in <a href='https://github.com/TempAccForForking/Mirror-Bot-Tweaks/blob/a287d279ec9503f6f54d5ad856ee423b9673e66d/gdtot.py#L17'>line no.17</a> of gdtot module. (just the part after equal to sign)

Terms & Conditions:
  - This module will clone the file in drive and when drive storage gets full it'll automatically clone further files in a shared drive but you cannot set specific shared drive to clone the data, It's server side so it'll take the first shared drive from all available drives.
  - So to use specific shared drive make new gmail and add that mail into that drive and use cookies of that mail in this module.
  - Clone limit of google drive is 750GB/Day per account so module cannot clone more than that per day.
  - If you are using edu then module will clone all the files in default drive (you cannot set specific shared drive using edu mail)
