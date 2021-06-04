# QAngle class

## Variables

  
 \| Name \| Type \| Description \| \| :--- \| :---- \| :---------- \| \| x \| float \| pitch \| \| y \| float \| yaw \| \| z \| float \| roll \|

## Functions

 \#\#\# IsZero Returns: \| Type \| Description \| \| :--- \| :--------------------------------- \| \| bool \| true if all angle axes equals zero \| Code: \`\`\`lua local angZero = QAngle.new\(0.0, 0.0, 0.0\) local bIsZero = angZero.IsZero\(\) \`\`\` \# \#\#\# Clamp Returns: \| Type \| Description \| \| :----- \| :---------------------------- \| \| QAngle \| clamped to legit values angle \| Code: \`\`\`lua local angUntrusted = QAngle.new\(180.0, 720.0, 100.0\) angUntrusted.Clamp\(\) -- after this call angle will be QAngle\(89.0, 180.0, 0.0\) -- but also able to assign clamped angle to new angle local angClamped = angUntrusted.Clamp\(\) \`\`\` \# \#\#\# Normalize Returns: \| Type \| Description \| \| :----- \| :------------------------------- \| \| QAngle \| normalized to legit values angle \| Code: \`\`\`lua local angUntrusted = QAngle.new\(180.0, 720.0, 100.0\) angUntrusted.Normalize\(\) -- after this call angle will be QAngle\(-90.0, 180.0, 0.0\) -- but also able to assign normalized angle to new angle local angNormalized = angUntrusted.Normalize\(\) \`\`\`

