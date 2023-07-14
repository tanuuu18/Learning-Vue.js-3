# Hello World

# Four ways to add Vue

## 1. <ins>CDN Package</ins>

```
 <script src="https://unpkg.com/vue@next"></script>
```

## 2. <ins>npm</ins>
```
npm install vue@next
```
Preferred approach over CDN when building large scale applications with Vue.


## 3. <ins>Vue CLI</ins>
Vue provides an official CLI for quickly scaffolding single page applications.

```
npm install -g @vue/cli
vue create hello-world
```

## 4. <ins>Vite </ins>
An opinionated web dev build tool that serves your code via native ES Module imports.
Your code is served at a lightning fast speed and you get nearly instant hot module replacement.

```
npm init vite-app hello-world
```



## Approach choosen for the series

 <b>  CDN</b> : incorporate Vue into a really old legacy code base for quickly prototype.
  
<b>  npm</b> : is the recommended approach for building large scale applications with Vue.

✔️ <b> Vue CLI</b> : Takes only a few minutes to get up and running with hot-reload, lint-on-save, and production-ready builds.

  <b>  Vite</b> : Its currently in beta version.
