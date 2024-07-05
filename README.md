# hexo-notepad

Blog in static page format, using Hexo. This is an skeleton to share the most important custom changes I made for my own [personal Gitlab page of coding notes](https://angelesbroullon.gitlab.io/code-notepad/).

## Notes

* The most relevant changes are documented on [this post](https://angelesbroullon.gitlab.io/code-notepad/2019/04/08/gitlab-and-hexo/).
* The docker image used on CI/CD contains node-12 on alpine, which has longer maintenance period, plus alpine is lighter and faster.
* If you want to put this code on your own Gilab project which is not called hexo-notepad, you may need to change the value `_config.yml` to the same name as your Gitlab project on the repository, or the Gitlab CI will deploy the page without the styles.
  ```yml
  root: '/hexo-notepad'
  ```

---

This is an [Hexo] website using GitLab Pages.

Learn more about GitLab Pages at https://pages.gitlab.io and the official
documentation https://docs.gitlab.com/ee/user/project/pages/.

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [GitLab CI](#gitlab-ci)
- [Building locally](#building-locally)
- [GitLab User or Group Pages](#gitlab-user-or-group-pages)
- [Did you fork this project?](#did-you-fork-this-project)
- [Troubleshooting](#troubleshooting)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## GitLab CI

This project's static Pages are built by [GitLab CI][ci], following the steps
defined in [`.gitlab-ci.yml`](.gitlab-ci.yml):

```
image: node:10.15.3

cache:
  paths:
    - node_modules/

before_script:
  - npm install hexo-cli -g
  - test -e package.json && npm install
  - hexo generate

pages:
  script:
    - hexo generate
  artifacts:
    paths:
      - public
  only:
    - master
```

## Building locally

To work locally with this project, you'll have to follow the steps below:

1. Fork, clone or download this project
1. [Install][] Hexo and [Hexo Server][hexo-server]
1. Install dependencies: `npm install`
1. Preview your site: `hexo server`
1. Add content
1. Generate your site (optional): `hexo generate`

Read more at Hexo's [documentation][].

## GitLab User or Group Pages

To use this project as your user/group website, you will need one additional
step: just rename your project to `namespace.gitlab.io`, where `namespace` is
your `username` or `groupname`. This can be done by navigating to your
project's **Settings**.

Read more about [user/group Pages][userpages] and [project Pages][projpages].

## Did you fork this project?

If you forked this project for your own use, please go to your project's
**Settings** and remove the forking relationship, which won't be necessary
unless you want to contribute back to the upstream project.

## Troubleshooting

1. CSS is missing! That means two things:

    Either that you have wrongly set up the CSS URL in your templates, or
    your static generator has a configuration option that needs to be explicitly
    set in order to serve static assets under a relative URL.

----

Forked from @AngelesBroullon

[ci]: https://about.gitlab.com/gitlab-ci/
[hexo]: https://hexo.io
[install]: https://hexo.io/docs/index.html#Installation
[documentation]: https://hexo.io/docs/
[userpages]: http://doc.gitlab.com/ee/pages/README.html#user-or-group-pages
[projpages]: http://doc.gitlab.com/ee/pages/README.html#project-pages
[hexo-server]: https://hexo.io/docs/server.html