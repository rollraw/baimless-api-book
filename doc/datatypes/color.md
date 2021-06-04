# Color class

## Variables

  
 \| Name \| Type \| Description \| \| :--- \| :--- \| :---------- \| \| r \| byte \| red \| \| g \| byte \| green \| \| b \| byte \| blue \| \| a \| byte \| alpha \|

## Functions

 \#\#\# FromHSB :information\_source: \*\*Note:\*\* \`FromHSB\(\)\` is static class member function constructing color, it doesn't requires to call \`.new\(\)\` Parameters: \| Name \| Type \| Description \| \| :----------- \| :---- \| :------------------------------------ \| \| flHue \| float \| hue factor in HSB color scheme \| \| flSaturation \| float \| saturation factor in HSB color scheme \| \| flBrightness \| float \| brightness factor in HSB color scheme \| \| flApha \| float \| alpha factor \| Returns: \| Type \| Description \| \| :---- \| :------------------------ \| \| Color \| color in HSB color scheme \| Code: \`\`\`lua local colPurple = Color.FromHSB\(0.72, 1.0, 0.8, 1.0\) end\) \`\`\` \#\#\# Hue Returns: \| Type \| Description \| \| :---- \| :----------------------------- \| \| float \| hue factor in HSB color scheme \| Code: \`\`\`lua local colRed = Color.new\(255, 0, 0\) print\('hue of red color is '..tostring\(colRed:Hue\(\)\)\) \`\`\` \# \#\#\# Saturation Returns: \| Type \| Description \| \| :---- \| :------------------------------------ \| \| float \| saturation factor in HSB color scheme \| Code: \`\`\`lua local colGreen = Color.new\(0, 255, 0\) print\('saturation of green color is '..tostring\(colGreen:Saturation\(\)\)\) \`\`\` \# \#\#\# Brightness Returns: \| Type \| Description \| \| :---- \| :------------------------------------ \| \| float \| brightness factor in HSB color scheme \| Code: \`\`\`lua local colBlue = Color.new\(0, 0, 255\) print\('brightness of blue color is '..tostring\(colBlue:Brightness\(\)\)\) \`\`\`

