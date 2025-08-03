# beingtomgreen.docker

A _really_ simple role for running installing and configuring Docker on Ubuntu/Debian based systems.

You almost certainly shouldn't use this, after all, [geerlingguy/ansible-role-docker](https://github.com/geerlingguy/ansible-role-docker) exists.

## Installation & usage

Given that Galaxy seems to have abandoned roles, I suggest referencing this repository directly in your projects `requirements.yml`:

```yaml
---

roles:
  - name: beingtomgreen.docker
    src: https://github.com/BeingTomGreen/ansible-role-docker.git

collections: []
```

You can then install it alongside your other requirements as normal:

```bash
ansible-galaxy install -r requirements.yml
```

You're then free to use it within your project:

```yaml
---

- hosts: docker-hosts
  become: true
  vars:
    docker_users:
      - 'my_litle_user'
      - 'bob'

  roles:
    - role: beingtomgreen.docker
```

## Role Variables

See [`defaults/main.yml`](defaults/main.yml) for more details.

## Requirements

None.

## Dependencies

None.

## License

[MIT](LICENSE)

## Author Information

[Tom Green](https://github.com/BeingTomGreen)
