# Url-Shorten-Worker
A URL Shortener created using Cloudflare Worker

# API

[API Documentation](API.md)

# Getting started
### Workers KV

Go to Workers KV and create a namespace.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232805.png">

### Create Worker and bind KV Namespace

Bind an instance of a KV Namespace to access its data in a Worker.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232536.png">

### Create `LINKS` variable in Worker settings for the KV Namespace 

In Worker Settings -> Variables add a `LINKS` binding to your KV namespace.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232704.png">

### Copy the code in `index.js` to your own Cloudflare Worker 

Copy the `index.js` code from this project to Cloudflare Worker. 

### Save and Deploy

Click Save and Deploy

# Demo by xyTom (original auther)
https://lnks.tools/
 
Note: Because someone abused the demo website, all link will automatically expiree after 24 hours. For long-term use, please deploy your own instance.

