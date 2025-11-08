### Deprecated

I will not maintain this.

At some point I wanted a library to fine tune the management of Ansible Galaxy
dependencies from within Python, but I decided it's not worth the trouble,
because Ansible Galaxy works just fine as it is from the CLI.

### Installing

```
pip install ansible-galaxy-helper
```

### Usage

```python
import os
import ansible_galaxy_helper

result = ansible_galaxy_helper.ensure_galaxy_dependencies(
        os.path.join('path', 'to', 'ansible-galaxy-requirements.yml'))

try:
    assert result == 0
except AssertionError:
    raise RuntimeError("Didn't work.")
```
