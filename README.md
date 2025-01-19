# How-To-Deploy-MERN-Project

### Add versel.json file in backend
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

### Add versel.json file in frontend

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
### Go to versel webiste
1. create new project
2. select project from git repo
3. give project name
4. select the backend from root
5. add env file
6. hit deploy

