# B45 Labs | Library – Third-Party Notices

**Last updated:** 2026-07-08
**Applies to:** B45 Labs | Library v1.0.0 (Revit 2023, 2024, 2025, 2026, 2027 builds)

This document lists the third-party components redistributed with the
B45 Labs | Library installer and their applicable licenses.

B45 Labs' own assemblies (`B45Labs.Library.dll`, `B45Labs.Shared.dll`,
`B45Labs.Connect.Sdk.dll`, `B45Labs.Connect.Contracts.dll`) are proprietary and
are not listed here. Platform components (the Autodesk Revit API and the
Microsoft .NET runtime) are referenced where present on the user's machine and
are **not** redistributed by this installer.

---

## Redistributed third-party libraries

| Component | Version | License | Source |
|---|---:|---|---|
| BouncyCastle.Cryptography | 2.5.0 | MIT | https://github.com/bcgit/bc-csharp |
| Newtonsoft.Json | 13.0.3 | MIT | https://www.newtonsoft.com/json |
| OpenMcdf | 3.1.4 (net8 / net10) · 2.4.1 (net48) | MPL-2.0 | https://github.com/ironfede/openmcdf |
| System.Data.SQLite (`System.Data.SQLite.dll` + `SQLite.Interop.dll`) | 1.0.119 | Public Domain / SQLite License | https://www.sqlite.org |

> The net48 builds (Revit 2023 / 2024) ship OpenMcdf 2.4.1; the net8 / net10
> builds (Revit 2025 / 2026 / 2027) ship OpenMcdf 3.1.4. Both are MPL-2.0-licensed.

---

## License texts

### MIT License

Applies to BouncyCastle.Cryptography and Newtonsoft.Json.

```
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

Copyright holders:
- BouncyCastle.Cryptography — Copyright (c) The Legion of the Bouncy Castle Inc. (https://www.bouncycastle.org)
- Newtonsoft.Json — Copyright (c) James Newton-King

### Mozilla Public License 2.0 (OpenMcdf)

OpenMcdf is licensed under the **Mozilla Public License, version 2.0 (MPL-2.0)**.
The full license text is available at https://www.mozilla.org/en-US/MPL/2.0/.

OpenMcdf is redistributed here in **unmodified** binary form. As required by the
MPL-2.0, the corresponding source code is available from the project's public
repository: https://github.com/ironfede/openmcdf

Copyright (c) Federico Blaseotto.

### SQLite (System.Data.SQLite)

SQLite is in the **Public Domain**. The System.Data.SQLite ADO.NET wrapper is
distributed under the same terms. See https://www.sqlite.org/copyright.html.

---

## Questions

For questions about licensing or third-party components in B45 Labs | Library,
contact:

- **Vendor:** B45 Labs
- **Email:** support@b45labs.com
