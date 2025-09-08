## Heading with Custom ID (Extended Markdown Syntax) {#custom-id}

Link to this [heading](#custom-id) using the extended Markdown syntax.

## Heading with Custom ID (MultiMarkdown Syntax) [custom-id]

Link to this [heading][custom-id] using the MultiMarkdown syntax or just
[custom-id].


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
