## Desktop Notifications

Simple cross-platform Python3 module for displaying desktop notifications.

### Installation
```bash
$ pip install py-notifier
```

### Requirements
If running on Windows: `win10toast`

If running on MacOS:
 - [alerter]( https://github.com/vjeantet/alerter ) binary in your `PATH` for full feature support.
 - The fallback support ignores:
   - duration
   - urgency
   - icon_path

*Note: MacOS does not support `urgency` for notifications regardless of installed dependencies.*

### Example
```python
from pynotifier import Notification


Notification(
	title='Notification Title',
	description='Notification Description',
	icon_path='path/to/image/file/icon.png', # On Windows .ico is required, on Linux - .png, on MacOS it can be a file path or URL
	duration=5,                              # Duration in seconds
	urgency=Notification.URGENCY_CRITICAL
).send()
```

### Author
* [Yuriy Lisovskiy](https://github.com/YuriyLisovskiy)

### Contributors
* [Tom White](https://github.com/tmwbook)

### License
The project is licensed under the terms of the [GNU General Public License v3.0](https://opensource.org/licenses/GPL-3.0), see the [LICENSE](LICENSE) file for more information.
