## Heading with Custom ID (Extended Markdown Syntax) {#custom-id}

Link to this [heading](#custom-id) using the extended Markdown syntax.

## Heading with Custom ID (MultiMarkdown Syntax) [custom-id]

Link to this [heading][custom-id] using the MultiMarkdown syntax or just
[custom-id].


---
title: "Ansible (Galaxy) Skeletons"
slug: "ansible-skeletons"
page:
  showMeta: false
  showTitle: true
list:
  showMeta: false
showToc: true
tableOfContents: true
# project specific front matter

project:
  description: "Short description, markdown allowed. Will also be used in the overview"
  status: "stable" # stable|beta|archived
  license: "WTFPL" # use SPDX id if possible, e.g. MIT, Apache-2.0
  website: "https://foundata.github.io/ansible-docsmith/"
  logo:
     bitmap:
     svg:
     square:

  readme:
    url: "https://raw.githubusercontent.com/foundata/ansible-docsmith/main/README.md"
    render: "html"  # html|code


  source:
    - label: "GitHub"
      url: "https://github.com/foundata/ansible-docsmith"
      primary: true
    - label: "GitLab"
      url: "https://gitlab.com/foundata/ansible-docsmith"
    - label: "Codeberg"
      url: "https://codeberg.org/foundata/ansible-docsmith"

  docs:
    - label: "Main docs"
      url: "https://foundata.github.io/ansible-docsmith/"

  releases:
    - label: "GitHub Releases"
      url: "https://github.com/foundata/ansible-docsmith/releases"

  issues:
    - label: "GitHub Issues"
      url: "https://github.com/foundata/ansible-docsmith/issues"

  # packages:                 # optional registries (add only if relevant)
  #   - label: "Ansible Galaxy"
  #     url: "https://galaxy.ansible.com/foundata/docsmith"

  changelog:
    - label: "GitHub Issues"
      url: "https://github.com/foundata/ansible-docsmith/issues"


  maintainers:              # optional; omit emails if you don’t want them public
    - name: "foundata"
      url: "https://foundata.net"
      email:


  funding:                  # optional
    - label: "GitHub Sponsors"
      url: "https://github.com/sponsors/foundata"

---

```
code
```

also code?

````yaml
what is this
```
# why
nested
```

ok?

````


~~~markdown
what is this
```
# why
nested
```

ok?
~~~

sdsss


```jinja2
111
```

sdsad

~~~markdown
# heello

## Example Playbook

```yaml
[...]
## Author Information
- ansible.builtin.include_role:
    name: "{{ role_name }}"
  vars:
sss
```
## Author Information
{% for var_name, var_spec in options.items() %}
{% if var_spec.default is not none %}
    {{ var_name }}: {{ var_spec.default }}
{% else %}
    # {{ var_name }}: # {{ var_spec.description }}
{% endif %}
{% endfor %}


## Author Information

{% if primary_spec.author %}
{% for author in primary_spec.author %}

- {{ author }}
{% endfor %}
{% endif %}
~~~

ok
ok
