![Logo](/logo/logo.png)

[![Wireshark](https://img.shields.io/badge/From-WireShark-blue.svg)](https://www.wireshark.org/tools/oui-lookup.html)
[![PyPi](https://img.shields.io/badge/PyPi-Available-green.svg)](https://opensource.org/licenses/MIT)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![OUI Segment](https://img.shields.io/badge/Available_OUI-50337-red.svg)

PyOUI_DB is a Python package providing a dictionary containing MAC address Organizationally Unique Identifiers (OUIs) and their corresponding company names. This data is derived from The Wireshark OUI lookup tool, compiled from various sources.

## Installation

You can install PyOUI_DB via pip:

```bash
pip install pyoui-db
```

## Usage

```python
from pyoui_db import OUI_LIB

mac_adress = "00:00:08"

# To retrieve the abbreviated company name for a given OUI
oui_abbreviated = OUI_LIB[mac_adress.upper()][0]

# To retrieve the full company name for a given OUI
oui_full = OUI_LIB[mac_adress.upper()][1]
```

## Contributing

Contributions are welcome! If you find any missing OUIs or company names, please consider contributing by adding them to the database.

1. Fork the repository.
2. Add the missing OUIs or company names to the `OUI_LIB` dictionary in the `pyoui_db.py` file.
3. Commit your changes (`git commit -am 'Add missing OUIs or company names'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

Alternatively, you can collaborate directly with Wireshark by visiting their [donate page](https://wiresharkfoundation.org/donate/).


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the Wireshark manufacturer database for providing the data.
