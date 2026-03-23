# Webservice

## REST

**Imports**
```python
from flask import Flask, jsonify, request, make_response
from http import HTTPStatus
```
**App definieren**
```python

app = Flask(__name___)
```

**Routen**

```python
@app.route('/verkehr/<string:verkehrsmittel>', methods=['GET'])
def get_verkehrsmittel(verkehrsmittel)
```

**Request Params**
```python
 data = request.get_json()
month = data["month"]
```

**HTTPStatus*
```python
return jsonify({"error": "Missing required field: monat"}), HTTPStatus.BAD_REQUEST
return jsonify({"message": "OK"}), HTTPStatus.OK
```

* ```200```: ```OK```
* ```201```: ```Created```
* ```204```: ```No Content```
* ```400```: ```Bad Request```
* ```404```: ```Not Found```

## Model
```python
from http.client import responses
```

```python
class Model:
    def __init__(self):
        self.url = "http://localhost:5000/verkehr"
```

**Requests**
```python
response = requests.get(self.url + "/" + verkehrsmittel + "/year")
```

## View
**Imports**

```python
from PyQt6 import uic
from PyQt6.QtWidgets import QMainWindow, QComboBox,
import controller
```
```python
class View(QMainWindow):
    type: QComboBox
    month: QSpinBox
```

```python
 def __init__(self, controller):
        super().__init__()
        uic.loadUi("view.ui", self)
        self.controller = controller
```

**Button Handling**
```python
self.reset.clicked.connect(self.handle_reset)
```
## Controller

**Imports**

```python
import sys
from http.client import responses

import model
import view
import calendar
from PyQt6.QtWidgets import QApplication
```

```python
class Controller:
    def __init__(self):
        self.model = model.Model()
        self.view = view.View(self)
```

```python
if __name__ == '__main__':
    app = QApplication(sys.argv)
    c = Controller()
    c.view.show()
    sys.exit(app.exec())
```
