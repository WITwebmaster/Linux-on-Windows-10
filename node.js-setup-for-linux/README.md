# Node.js setup for Linux

![](../.gitbook/assets/590px-node.js_logo.svg%20%281%29.png)

 **Node.js** is an open-source cross-platform JavaScript run-time environment that allows server-side execution of JavaScript code. This means that you can run JavaScript code on your machine as a standalone application, free of any web browser. **Node.js** is mainly used to build back-end server-side applications, but it is also very popular as a full-stack and front-end solution.

Npm is the default package manager for **Node.js** and the world’s largest software registry. 

Ubuntu 18.04 contains a version of **Node.js** in its default repositories that can be used to provide a consistent experience across multiple systems.

Install **Node.js** from the repositories:

```text
apt install nodejs
```

Now check what version you are running of node using this command 

```text
node --version
```

If the package in the repositories suits your needs, this is all you need to do to get set up with Node.js. In most cases, you’ll also want to also install `npm`, the Node.js package manager. You can do this by typing:

```text
apt install npm
```

