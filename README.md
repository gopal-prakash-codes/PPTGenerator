## Introduction

PyPDFForm is a free and open source pure-Python 3 library for PDF form processing. It contains the essential 
functionalities needed to interact with PDF forms:

* Inspect what data a PDF form needs to be filled with.
* Fill a PDF form by simply creating a Python dictionary.
* Create a subset of form widgets on a PDF.

It also supports other common utilities such as extracting pages and merging multiple PDFs together.

## Installing

Install using [pip](https://pip.pypa.io/en/stable/):

```shell script
pip install PyPDFForm
```
from PyPDFForm import PdfWrapper

filled = PdfWrapper("sample_template.pdf").fill(
    {
        "test": "test_1",
        "check": True,
        "test_2": "test_2",
        "check_2": False,
        "test_3": "test_3",
        "check_3": True,
    },
)

with open("output.pdf", "wb+") as output:
    output.write(filled.read())
```
