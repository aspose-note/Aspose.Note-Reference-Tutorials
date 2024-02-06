---
title: Apply Aspose.Note License from Path
linktitle: Apply Aspose.Note License from Path
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 11
url: /net/licensing/apply-license-from-path/
---

## Complete Source Code
```csharp
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.ApplyLicense
{
    public class ApplyLicenseByPath
    {
        public static void Run() 
        {
            // ExStart:ApplyLicenseByPath        
            // ExFor:License
            // ExFor:License.SetLicense(System.String)
            // ExSummary:Shows how to load a license for Aspose.Note from a file.

            Aspose.Note.License license = new Aspose.Note.License();
            license.SetLicense("Aspose.Note.lic");

            // ExEnd:ApplyLicenseByPath
        }
    }
}

```
