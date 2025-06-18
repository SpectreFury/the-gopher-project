---
layout: "../../../layouts/MarkdownLayout.astro"
title: "Installing Go"
subtitle: "The Beginning"
backlink: "/roadmap#the-beginning"
---

It is finally time that we install Go to your system! I know right, exciting. Go is available to all the major operating systems, so choose your operating system, and just go with the steps. You don't have to look at the OS that don't concern you obviously.

### Windows

1. Open your web browser and navigate to [Go](https://go.dev) website.
2. Click on the download button.
3. There should be multiple options to download Go for different operating systems. You want to choose Windows, look for .msi files in specific. Once you find it, just download it by clicking on it.
4. Once it's downloaded successfully, open it either from the browser directly or from your download locations (Downloads folder on windows usually.)
5. Follow all the steps till Go is installed on your computer.

### Linux

1. Open your terminal
2. Paste the command `sudo apt update` and press Enter. This will update all the packages in your system.
3. Paste `sudo apt install golang-go` and press Enter again. This will download Go to your system and install it.

### MacOS

1. Open your web browser and navigate to [Go](https://go.dev) website.
2. Click on the download button.
3. There should be multiple options to download Go for different operating systems. You want to choose MacOS, look for .pkg files in specific. Once you find it, just download it by clicking on it.
4. Follow all the steps till Go is installed on your computer.

Once you're done with installing Go on your system, we can proceed to the next lesson, however it would be best if you checked if your installing was successful. To do that, simply open your preferred terminal and type the following:

```
go version
```

Run the command and you should get something similar to this:

```
go version go1.24.2 windows/amd64
```

If you see something like this or similar, congratulations! You have Go installed in your computer and you are ready to become a _Gopher_.

If you see something like

```
bash: go: command not found
```

Go was either not successfully installed or you have a simple PATH error. 

---
