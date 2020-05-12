org-roam-server
===================================

![Graph](https://raw.githubusercontent.com/goktug97/org-roam-server/master/org-roam-server.gif)

## Requirements

- [org-roam](https://github.com/jethrokuan/org-roam)
- [simple-httpd](https://github.com/skeeto/emacs-web-server/)

## use-package

```bash
git clone https://github.com/goktug97/org-roam-server
```

```elisp
(use-package org-roam-server
  :ensure nil
  :load-path <path-to-org-roam-server-folder>)
```

## use-package with straight.el

```elisp
(use-package org-roam-server
  :straight (org-roam-server
             :host github
             :repo "org-roam/org-roam-server"
             :files (:defaults ("assets/" . "assets/")))
  :defer t)
```

## Usage

Use `M-x org-roam-server-mode RET` to enable the global mode. 
It will start a web server on http://127.0.0.1:8080/

## Clickable Graph
The graph uses org-roam protocol which means if you click one of the nodes
it opens the org file. For it to work, you should set up the org-roam protocol;
https://org-roam.readthedocs.io/en/develop/roam_protocol/

Also make sure the emacs server is started; `M-x server-start RET`

## License
org-roam-server is licensed under the MIT License.

For Javascript and CSS libraries please refer to;
- https://github.com/jquery/jquery/blob/master/LICENSE.txt
- https://github.com/visjs/vis-network
- https://github.com/twbs/bootstrap/blob/master/LICENSE
- https://github.com/gongzhitaao/orgcss
- https://github.com/select2/select2
