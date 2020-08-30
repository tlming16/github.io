---
title: Blog with github.io 
---
## set env 

```powershell
// 以管理员身份运行PowerShell
get-ExecutionPolicy
// 若 Restricted 
set-ExecutionPolicy RemoteSigned 
npm config set registry https://registry.npm.taobao.org 
npm install -g hexo-cli
```

## local blog

```powershell
cd blog 
hexo init 
npm install 
hexo g(generate) // 生成 网页
hexo s(server) // 开启本地服务器 
// 在浏览器 localhost:4000 可以看到配置效果
```

## github.io

```yaml
//准备 github.io repo
//- https://github.com/tlming16/tlming16.github.io
//- git@github.com:tlming16/tlming16.github.io.git
//修改配置 /blog/_config.yml 
deploy:
  type: git 
  repository: git@github.com:tlming16/tlming16.github.io.git 
  branch : master 
npm install hexo-deployer-git --save // github.io 部署
```

## thems

```powershell
//flexy 主题
git clone https://github.com/sjaakvandenberg/flexy themes/flexy
npm un -S hexo-renderer-ejs
npm i -S hexo-renderer-jade
//修改 /blog/_config.yml theme 为 flexy 
```

```powershell
//butterfly 主题
git clone https://github.com/jerryc127/hexo-theme-butterfly themes/butterfly
npm i hexo-theme-butterfly
//修改 /blog/_config.yml theme 为 butterfly
```

```
//more themes
https://hexo.io/themes/
```



## hexo

```bash
hexo  --help 
  clean     Remove generated files and cache.
  config    Get or set configurations.
  deploy    Deploy your website.
  generate  Generate static files.
  help      Get help on a command.
  init      Create a new Hexo folder.
  list      List the information of the site
  migrate   Migrate your site from other system to Hexo.
  new       Create a new post.
  publish   Moves a draft post from _drafts to _posts folder.
  render    Render files with renderer plugins.
  server    Start the server.
  version   Display version information.
```

