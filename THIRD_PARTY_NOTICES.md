# B45 Labs | Library – Third-Party Notices

**Last updated:** 2026-08-05
**Applies to:** B45 Labs | Library 2.0.0 (Revit 2023, 2024, 2025, 2026, 2027 builds)

> Revised on 2026-08-05 for the OpenMcdf packaging change. From the release that
> follows v1.1.0, the Revit 2025 / 2026 / 2027 builds combine OpenMcdf into
> `B45Labs.Library.dll` instead of installing it as a separate file, so the
> previous wording ("redistributed in unmodified binary form") no longer
> described those builds. The same pass corrected two errors that predate the
> change: OpenMcdf 3.1.4 lives in a different repository from 2.4.1 (the project
> moved to the `openmcdf` organisation), and the 3.1.4 copyright names a second
> author. Exact source commits are now given per version.

> Rebuilt on 2026-07-23 from the **actual build output** of all five configs, not from the
> csproj. The previous revision listed only 4 components and was missing 8 that the
> installer has been shipping, including SixLabors.Fonts, which is Apache-2.0 and not MIT.
> `System.IO.Packaging` moved to 10.0.10 in response to the Autodesk App Store
> vulnerability scan of 2026-07-23.

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
| ClosedXML | 0.104.2 | MIT | https://github.com/ClosedXML/ClosedXML |
| ClosedXML.Parser (the assembly self-reports `1.0.0`; the shipped binary is byte-identical to the `netstandard2.1` asset of package **1.2.0**) | 1.2.0 | MIT | https://github.com/ClosedXML/ClosedXML.Parser |
| DocumentFormat.OpenXml (incl. `DocumentFormat.OpenXml.Framework.dll`) | 3.1.1 | MIT | https://github.com/dotnet/Open-XML-SDK |
| ExcelNumberFormat | 1.1.0 | MIT | https://github.com/andersnm/ExcelNumberFormat |
| Newtonsoft.Json | 13.0.3 | MIT | https://www.newtonsoft.com/json |
| OpenMcdf (net8 / net10: combined into `B45Labs.Library.dll`, not a separate file) | 3.1.4 | MPL-2.0 | https://github.com/openmcdf/openmcdf |
| OpenMcdf (net48: separate `OpenMcdf.dll`) | 2.4.1 | MPL-2.0 | https://github.com/ironfede/openmcdf |
| RBush | 4.0.0 | MIT | https://github.com/viceroypenguin/RBush |
| SixLabors.Fonts | 1.0.0 | Apache-2.0 | https://github.com/SixLabors/Fonts |
| System.Data.SQLite (`System.Data.SQLite.dll` + `SQLite.Interop.dll`) | 1.0.119 | Public Domain / SQLite License | https://www.sqlite.org |
| System.IO.Packaging (Revit 2025 / 2026 builds only) | 10.0.10 | MIT | https://github.com/dotnet/dotnet |

> The net48 builds (Revit 2023 / 2024) ship OpenMcdf 2.4.1 as a separate
> `OpenMcdf.dll`. The net8 / net10 builds (Revit 2025 / 2026 / 2027) ship OpenMcdf
> 3.1.4 **combined into `B45Labs.Library.dll`**, so no `OpenMcdf.dll` file is
> installed for those Revit versions. Both are MPL-2.0-licensed, and the MPL-2.0
> section below states how to obtain the source for each. The two versions are
> also maintained in different repositories: 2.4.1 predates the project's move to
> the `openmcdf` organisation.

> The **Revit 2023 / 2024** (net48) builds additionally ship the following Microsoft
> compatibility packages, all **MIT**-licensed and published from
> https://github.com/dotnet/maintenance-packages. They are absent from the net8 / net10
> builds, where the runtime provides them natively. Versions are kept in lock-step with
> B45 Labs · Coordination, because both products load into the same Revit process.
>
> | Component | Version |
> |---|---:|
> | `Microsoft.Bcl.HashCode` | 6.0.0 |
> | `System.Buffers` | 4.6.1 |
> | `System.Memory` | 4.6.3 |
> | `System.Numerics.Vectors` | 4.6.1 |
> | `System.Runtime.CompilerServices.Unsafe` | 6.1.2 |
> | `System.Threading.Tasks.Extensions` | 4.6.3 |
>
> `System.IO.Packaging` is shipped only by the **Revit 2025 / 2026** builds. The
> Revit 2027 (net10) build does not ship it, because that runtime provides it.

---

## License texts

### MIT License

Applies to BouncyCastle.Cryptography, ClosedXML, ClosedXML.Parser,
DocumentFormat.OpenXml, ExcelNumberFormat, Newtonsoft.Json, RBush, and the Microsoft
`System.*` and `Microsoft.Bcl.*` packages listed above.

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

**Copyright notices.** The MIT license requires the copyright notice to travel
with the software, so each line below is the notice the component itself
declares, quoted verbatim from the shipped assembly's `LegalCopyright` resource
or from the published NuGet package metadata. They are not paraphrased.

| Component | Copyright notice as declared |
|---|---|
| BouncyCastle.Cryptography 2.5.0 | Copyright © Legion of the Bouncy Castle Inc. 2000-2024 |
| DocumentFormat.OpenXml 3.1.1 (incl. `.Framework`) | © Microsoft Corporation. All rights reserved. |
| Newtonsoft.Json 13.0.3 | Copyright © James Newton-King 2008 |
| RBush 4.0.0 | Copyright © 2017-2024 Turning Code, LLC (and others) |
| `Microsoft.Bcl.HashCode`, `System.Buffers`, `System.Memory`, `System.Numerics.Vectors`, `System.Runtime.CompilerServices.Unsafe`, `System.Threading.Tasks.Extensions` (net48 builds) | © Microsoft Corporation. All rights reserved. |
| `System.IO.Packaging` 10.0.10 (Revit 2025 / 2026 builds) | © Microsoft Corporation. All rights reserved. |

Two components publish no copyright line of their own, in either the assembly or
the package metadata. Rather than invent one, they are attributed by their
declared authors, and the authoritative notice is the LICENSE file in each
project's repository:

| Component | Declared authors | Authoritative notice |
|---|---|---|
| ClosedXML 0.104.2 and ClosedXML.Parser 1.2.0 | Jan Havlíček, Francois Botha, Aleksei Pankratev, Manuel de Leon, Amir Ghezelbash | https://github.com/ClosedXML/ClosedXML/blob/develop/LICENSE |
| ExcelNumberFormat 1.1.0 | ExcelNumberFormat developers | https://github.com/andersnm/ExcelNumberFormat/blob/master/LICENSE |

### Apache License 2.0 (SixLabors.Fonts)

SixLabors.Fonts 1.0.0 is licensed under the **Apache License, Version 2.0**.
The full license text is available at https://www.apache.org/licenses/LICENSE-2.0.
It is redistributed here in unmodified binary form; the corresponding source is
available at https://github.com/SixLabors/Fonts.

Copyright notice as declared by the package: **Copyright © Six Labors**.

Apache-2.0 section 4(d): the package ships no NOTICE file, so there is no
attribution text to reproduce beyond the copyright line above.

### Mozilla Public License 2.0 (OpenMcdf)

OpenMcdf is licensed under the **Mozilla Public License, version 2.0 (MPL-2.0)**.
The full license text is available at https://www.mozilla.org/en-US/MPL/2.0/.

**How OpenMcdf is distributed.** B45 Labs makes no change to OpenMcdf's Source
Code Form. What differs between builds is only how the compiled library is
packaged:

- **Revit 2023 / 2024 (net48):** OpenMcdf 2.4.1 is installed as a separate,
  unmodified `OpenMcdf.dll` next to the add-in.
- **Revit 2025 / 2026 / 2027 (net8 / net10):** OpenMcdf 3.1.4 is combined at
  build time into `B45Labs.Library.dll`, so no separate `OpenMcdf.dll` is
  installed. Its types are made internal to that assembly, and the resulting
  assembly is processed by a commercial obfuscator, which renames symbols in the
  compiled output. This packaging is done under MPL-2.0 section 3.3, which
  permits the Covered Software to be distributed as part of a Larger Work under
  different terms, provided the Covered Software itself remains under the
  MPL-2.0. It is done so that OpenMcdf loads reliably inside Revit, where every
  add-in shares one assembly load context and a version published by another
  vendor can otherwise win the binding.

**How to obtain the source.** As required by MPL-2.0 section 3.2, the complete
Source Code Form of the exact OpenMcdf version in each build is publicly
available at no charge:

| Build | Version | Repository | Commit |
|---|---|---|---|
| Revit 2025 / 2026 / 2027 | 3.1.4 | https://github.com/openmcdf/openmcdf | `11ffb7cafff6eea99639df6b2b249dcf6bcca3ef` |
| Revit 2023 / 2024 | 2.4.1 | https://github.com/ironfede/openmcdf | `03ef8cb7a735cdf569886d6c8b21809be3bc38e6` |

The published NuGet packages `OpenMcdf 3.1.4` and `OpenMcdf 2.4.1` are the same
builds and are also available from https://www.nuget.org/packages/OpenMcdf.

Nothing in the B45 Labs license terms limits, and nothing in them is intended to
limit, any right you have in OpenMcdf under the MPL-2.0. Where the B45 Labs
license and the MPL-2.0 disagree as to OpenMcdf, the MPL-2.0 governs.

- OpenMcdf 3.1.4: Copyright (c) 2010-2026 Federico Blaseotto, Jeremy Powell.
- OpenMcdf 2.4.1: Copyright (c) Federico Blaseotto.

### SQLite (System.Data.SQLite)

SQLite is in the **Public Domain**. The System.Data.SQLite ADO.NET wrapper is
distributed under the same terms. See https://www.sqlite.org/copyright.html.

Two files are involved, both from System.Data.SQLite 1.0.119: the managed
`System.Data.SQLite.dll` and the native `SQLite.Interop.dll` (x64, taken from
`x64\` on the net48 builds and from `runtimes\win-x64\native\` on the net8 /
net10 builds, and installed flat next to the add-in).

Although the code is public domain and no attribution is required, the package
declares a copyright line, reproduced here verbatim rather than dropped:
**Copyright © 2004-2008 Hipp, Wyrick & Company, Inc.** Authors are declared as
the SQLite Development Team; the wrapper's home is https://system.data.sqlite.org/.

---

## Questions

For questions about licensing or third-party components in B45 Labs | Library,
contact:

- **Vendor:** B45 Labs
- **Email:** support@b45labs.com
