
### environment variables

Environment variables are passed to the containers using config maps and secrets.

```yaml
# default settings

variables:
- name: 
  store: encrypted ('plaintext', 'encrypted')
  data:
```

```yaml
# explanations

variables:
- name: an arbitrary name
  store: if 'plaintext', variables are stored as a configmap, otherwise, they are stored as a secret
  data: a map of environment variables and values
```
