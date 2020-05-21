# Model

## model.Models

Langkah untuk membuat model:

1. Buat file `model_manusia.py` di folder `/models`
2. Definisikan model tersebut

```py
# Import models dari library odoo
from odoo import models

# Style nama kelas adalah Camel Case
class ModelKu(models.Model):
    # nama model yang di buat
    _name = "model.manusia"
```

3. Import model ke modul dengan mengedir file `__init__.py` yang ada di folder `/models` lalu tuliskan kode berikut

```py
from . import model_manusia.py
```

4. Membuat field pada model

Misalkan akan membuat model/table dengan bentuk seperti ini:

|  `nama`  |   `umur`    | `status_nikah` |
| :------: | :---------: | :------------: |
| `<Char>` | `<Integer>` |  `<Boolean>`   |

Maka kode nya adalah sebagai berikut:

```py
from odoo import models, fields # Tambahkan import fields

class ModelKu(models.Model):
    _name = 'model.manusia'

    # field nama sebagai character
    nama = fields.Char(string='Nama')
    # field umur sebagai integer
    umur = fields.Integer(string='Umur')
    # field status_nikah sebagai boolean
    status_nikah = fields.Boolean(string='Status Nikah')
```

## model.TransientModel
