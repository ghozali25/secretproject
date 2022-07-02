# secretproject

Assalamualaikum, Wr, Wb
Selamat Datang di Secret Project
Disini kita akan membahas tentang data analyst, data science, akuntansi, finance serta budgeting

Untuk kalian baru belajar tentang data analyst atau data science semacamnya sudah tidak asing lagi pasti dengan bahasa pemograman seperti python

hal yg pertama yg harus kalian install pada python yaitu pandas, numpy, matplotdb dan openpyxl (untuk membaca file excel)
karena ketiga ini akan sangat berguna sekali di kemudian hari

sedikit ulasan coding untuk standalone library 

.. testcode::
   :hide:

    >>> import os
    >>> import sys
    >>> if sys.version_info[0] < 3:
    ...     from StringIO import StringIO
    ... else:
    ...     from io import BytesIO as StringIO
    >>> PY2 = sys.version_info[0] == 2
    >>> if PY2 and sys.version_info[1] < 7:
    ...      from ordereddict import OrderedDict
    ... else:
    ...     from collections import OrderedDict
    


untuk menulis kedalam file excel yg kalian gunakan

>>> from pyexcel_xls import save_data
>>> data = OrderedDict() # from collections import OrderedDict
>>> data.update({"Sheet 1": [[1, 2, 3], [4, 5, 6]]})
>>> data.update({"Sheet 2": [["row 1", "row 2", "row 3"]]})
>>> save_data("your_file.xls", data)


untuk membaca file excel yg kalian punya

>>> from pyexcel_xls import get_data
>>> data = get_data("your_file.xls")
>>> import json
>>> print(json.dumps(data))
{"Sheet 1": [[1, 2, 3], [4, 5, 6]], "Sheet 2": [["row 1", "row 2", "row 3"]]}


