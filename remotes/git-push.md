---
title: git push
layout: default
parent: Remotes and Github
nav_order: 3
---

Git push
---

Now that we have set up the remote on GitHub and created our access token, we are ready to send our repository to the cloud. We do this by using git's push command:

```bash
git push origin main
```

Enter your github username when prompted, and paste your access token into the console using Ctrl+Shift+V.

![pushed](../images/push/pushed.png)
{: .terminal}

If you see the above in your terminal, congratulations, you have just pushed your repo to github!

Now if you go to your browser and enter "\<your-username\>.github.io", your site should pop up in the browser. Github will serve whatever is in your index.html file. 

