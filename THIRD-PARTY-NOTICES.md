# Avisos de terceiros: BioVez

O BioVez usa componentes de terceiros. Cada um continua sob a licença do seu autor; a licença proprietária do BioVez (arquivo `LICENSE`) **não** se aplica a eles e não altera esses direitos.

Os textos completos das licenças vão junto com o programa instalado, na pasta `licenses` (no código-fonte: `src/BioVez/licenses/`).

## Componentes distribuídos junto com o BioVez

| Componente | Versão | Licença | Titular / autor | Uso no BioVez | Texto da licença |
|---|---|---|---|---|---|
| .NET Runtime (Microsoft.NETCore.App) | 10.0 | MIT | .NET Foundation and Contributors | Base de execução do app (vai embutida no instalador) | `dotnet-runtime-LICENSE.txt`, `dotnet-runtime-THIRD-PARTY-NOTICES.txt` |
| Windows Desktop Runtime (Windows Forms) | 10.0 | MIT | .NET Foundation and Contributors | Janela do aplicativo | `windowsdesktop-runtime-LICENSE.txt` |
| Microsoft.Web.WebView2 (SDK) | 1.0.4314.35 | BSD 3-Clause (Microsoft) e avisos próprios | © Microsoft Corporation | Exibe a interface dentro da janela | `Microsoft.Web.WebView2-LICENSE.txt`, `Microsoft.Web.WebView2-NOTICE.txt` |
| Microsoft.Data.Sqlite / Microsoft.Data.Sqlite.Core | 10.0.14 | MIT | © Microsoft Corporation | Acesso ao banco de dados | `dotnet-runtime-LICENSE.txt` (mesmo texto MIT) |
| SQLitePCLRaw (bundle_e_sqlite3, core, provider, lib) | 2.1.13 | Apache-2.0 | Copyright 2014-2024 SourceGear, LLC (Eric Sink) | Ligação com o mecanismo SQLite | `Apache-2.0.txt` |
| SQLite (biblioteca e_sqlite3) | incluída no SQLitePCLRaw 2.1.13 | Domínio público | D. Richard Hipp e colaboradores | Mecanismo do banco de dados | (domínio público, sem texto de licença) |
| SourceAFIS | 3.14.0 | Apache-2.0 | Robert Važan | Extração e comparação de digitais | `Apache-2.0.txt` |
| SixLabors.ImageSharp | 2.1.13 | Apache-2.0 | Copyright © Six Labors | Dependência do SourceAFIS | `Apache-2.0.txt` |
| Dahomey.Cbor | 1.16.1 | MIT | Copyright © Dahomey Technologies 2020 (Michaël Catanzariti) | Dependência do SourceAFIS | texto MIT abaixo |

### Texto MIT (Dahomey.Cbor)

```
The MIT License (MIT)

Copyright (c) 2020 Dahomey Technologies

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

### Ícones da interface

Os ícones de linha da interface (usuários, cadeado, link externo, GitHub, LinkedIn, Instagram e outros) têm traçado igual ou muito semelhante aos conjuntos **Feather Icons** e **Lucide**. Parte deles veio do protótipo HTML usado como base da interface e parte foi adicionada depois; a origem exata de cada um não foi confirmada. Por precaução, seguem os avisos das duas licenças:

```
Feather Icons — The MIT License (MIT)
Copyright (c) 2013-2023 Cole Bemis

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

```
Lucide — ISC License
Copyright (c) for portions of Lucide are held by Cole Bemis 2013-2022 as part
of Feather (MIT). All other copyright (c) for Lucide are held by Lucide
Contributors 2022.

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY
SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION
OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN
CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```

## Componentes que o BioVez usa, mas não distribui

| Componente | Situação |
|---|---|
| Microsoft Edge WebView2 Runtime | Não vai no instalador. Quando falta, o instalador baixa o instalador oficial da Microsoft (`go.microsoft.com/fwlink/p/?LinkId=2124703`), confere a assinatura digital e o executa. Fica sob os termos de licença da Microsoft para o WebView2 Runtime. |
| Windows Biometric Framework, Serviço de Biometria, `pnputil`, `sc.exe` | Partes do Windows, usadas pelas interfaces do próprio sistema. |
| .NET Framework 4.6.2 (instalador e desinstalador) | Parte do Windows 10/11. O pacote `Microsoft.NETFramework.ReferenceAssemblies` (licença da Microsoft) é usado só na compilação e não é distribuído. |
| Fontes Segoe UI, Segoe UI Variable e Cascadia Mono | Fontes do Windows usadas pela interface. Não são distribuídas com o BioVez. |
| Drivers de leitores biométricos | Do fabricante de cada leitor; só entram no instalador se forem colocados na pasta `drivers` (ver `drivers/LEIA-ME.txt`). Confirme a licença do fabricante antes de redistribuir. |
