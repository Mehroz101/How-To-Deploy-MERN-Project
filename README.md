# How-To-Deploy-MERN-Project

## Javascript based project
## 1. Add versel.json file in backend
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

## 2. Add versel.json file in frontend


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
## Typescript based project

## 1. Add versel.json file in frontend

```
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ],
  "build": {
    "env": {
      "NODE_OPTIONS": "--max-old-space-size=4096"
    }
  }
}

```
aslo edit the package.json file script section
```
  "scripts": {
    "dev": "vite",
    "build": "tsc -b && vite build",
    "lint": "eslint .",
    "preview": "vite preview"
  },
```
add this in env file 
```
NODE_OPTIONS = --max-old-space-size=4096
```
## 2. Add versel.json file in backend

## 3. Deploy Backend

 Go to versel webiste
1. create new project
2. select project from git repo
3. give project name
4. select the backend from root
5. add env file
6. hit deploy


### 4. Deploy Frontend

1. create new project
2. select project from git repo
3. give project name
4. select the frontend from root
5. add env file and give backend api url of backend of versel depolyed project
6. hit deploy

