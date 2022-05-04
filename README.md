# A URL Shortener created using Cloudflare Worker

# API

[API Documentation](API.md)

# Getting started
### Workers KV

Go to Workers KV and create a namespace. Choose a KV Namespace name that makes sence for your purpose.
If you haven't already, make shure your cloudflare workers subdomain is named something meaningfull. 

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232805.png">

### Create Worker and bind KV Namespace

Create a Worker. Just like previously, you should change the Worker name to someting meaningfull instead of the default generated name. Then bind your KV Namespace to the worker so that it can access the data.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232536.png">

#### Create `LINKS` variable under Worker settings for the KV Namespace 

In Worker Settings -> Variables add a `LINKS` binding to your KV namespace. This variable is used in `index.js` to reference the KV Namespace.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232704.png">

### Copy the code in `index.js` to your own Cloudflare Worker 

Copy the `index.js` code from this project to Cloudflare Worker. 

### Save and Deploy

Click Save and Deploy

### [optional] Create HTTP Route to worker

If you have Cloudflare as your DNS server for your domain, then create a proxied AAAA DNS record pointing to `100::`.
Then in Worker settings under Trigger create a route to this Worker - i.e. example.com/*
If you don't have Cloudflare DNS for your domain, then you can always access your worker on https://[worker-name].[worker-subdomain].worker.dev and make CNAME records or URL forwards to this domain.

# Demo by xyTom (original auther)
https://lnks.tools/
 
Note: All links on the demo-site will automatically expiree after 24 hours. For long-term use, please deploy your own instance.

