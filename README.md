# How-To-Deploy-MERN-Project

# Add versel.json file in backend
```
{
  "installCommand": "npm install --legacy-peer-deps",
  "version": 2,
  "builds": [
    {
      "src": "index.js",
      "use": "@vercel/node"
    },
    { "src": "src/**/*", "use": "@vercel/static" }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "/"
    }
  ]
}

```

# Add versel.json file in frontend

```
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ]
}

```


