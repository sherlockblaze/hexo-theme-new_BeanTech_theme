> Ported Theme of [SherlockBlaze's Blog](https://sherlockblaze.com), Thank [Huxpro](https://github.com/Huxpro) for designing such a flawless theme.

> This BeanTech theme created by [YuHsuan](http://beantech.org) modified from the original Porter [Kaijun](http://kaijun.rocks/hexo-theme-huxblog/)

# what is the difference?

- First, I put random picture as the background of topbar, if you don't like it, you can set it back.
- Second, I think leancould comments is better in China, so I integrated the [valine](https://valine.js.org) comment system into it.
- Third, I also integrated the [Travis-CI](http://travis-ci.org) into it, so you can just write post, and push it to your repo, and the Travis-CI will deploy your website automatically. About the travis-ci configuration, see [here](./.travis.yml)
- Fourth, I didn't integrated the reward function into it, because I thinking I write for nothing, just share my knowledge, but if you want it, maybe learn from another version: [hexo-theme-huweihuang](https://github.com/huweihuang/hexo-theme-huweihuang.git)
- Fifth, better read more doc about [Travis-CI](http://travis-ci.org) and [Coding](https://coding.net) if you need. Here are some of the documents I looked at before I encountered problems: [Travis Start](https://docs.travis-ci.com/user/tutorial/), [Coding.net Domain Connect](https://coding.net/help/doc/pages/domain.html). If you wanna use both Github and Coding, better bind the domain name to the project on the coding first, then github. It's difficult.

# Attention

***you'll see some variable named like __GITHU_TOKEN__ *** and so on, they're the environment variables I configured in Travis-CI, so if you want to use Travis-CI, you maybe do it like what I did, it's keep your variables more secret, more safe, especially your Github Token and Coding.net Token. If you don't know how to get one, try this [passage](https://console.bluemix.net/docs/services/ghededicated/index.html#gheded_getting_started), and coding.net is similar with it, try figure it out by yourself.

***And if you have any question about all of it, try to leave a comments on this [page](https://sherlockblaze.com/about/)***, I'll reply you as soon as possible. Thanks.

# Note

***travis-ci.org*** is free, but ***travis-ci.com*** is not.
***When you get a Token of github or coding.net, better save it to your device or notebook, because they only show up at the first time they generated. Or you just need do it again.***

# [Live Demo](https://sherlockblaze.com)

# Usage
I publish the whole project for your convenience, so you can just follow the instruction down below, then you can easily customiz your own blog!

Let's begin!!!

## Init
```bash
git clone https://github.com/sherlockblaze/hexo-theme-new_BeanTech_theme.git
cd hexo-theme-new_BeanTech_theme
npm install # actually, you don't need run this command if you plan to deploy the website on Travis-CI
```

## Modify
Modify `_config.yml` file with your own info.
Especially the section:
### Deployment
Replace to your own repo!

> If you are in China, use both of coding and github is better. And of course you can choose any one you love.

```yml
deploy:
  type: git
  repository: 
    github: https://__GITHUB_TOKEN__@github.com/<yourAccount>/<repo>
    coding: https://<yourAccount>:__CODING_TOKEN__@git.dev.tencent.com/<yourAccount>/<repo>
  branch: <your-branch>
```

### Sidebar settings
Copy your avatar image to `<root>/img/` and modify the `_config.yml`:

```yml
sidebar: true    # whether or not using Sidebar.
sidebar-about-description: "<your description>"
sidebar-avatar: img/<your avatar path>
```
and activate your personal widget you like
```yml
widgets:         # here are widget you can use, you can comment out
- featured-tags
- short-about
- recent-posts
- friends-blog
- archive
- category
```

if you want to add sidebar widget, please add at `layout/_widget`.

### Signature Setup
Copy your signature image to `<root>/img/signature` and modify the `_config.yml`:
```yml
signature: true   # show signature
signature-img: img/signature/<your-signature-ID>
```

### Go to top icon Setup
My icon is using iron man, you can change to your own icon at `css/image`.

> Icon man is the best, so i keep it.

## Hexo Basics

Some hexo command(**And if you use travis-ci, you don't need to run those command every time by yourself.**):

```bash
hexo new post "<post name>" # you can change post to another layout if you want
hexo clean && hexo generate # generate the static file
hexo server # run hexo in local environment
hexo deploy # hexo will push the static files automatically into the specific branch(gh-pages) of your repo!
```

# Have fun ^_^ 

Please [Star](https://github.com/sherlockblaze/hexo-theme-new_BeanTech_theme.git) this Project if you like it! [Follow](https://github.com/sherlockblaze) would also be appreciated!
Peace!
