---
title: Apply Aspose.Note License using FileStream
linktitle: Apply Aspose.Note License using FileStream
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 12
url: /net/licensing/apply-license-using-filestream/
---

## Complete Source Code
```csharp
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.ApplyLicense
{
    public class ApplyLicenseUsingFileStream
    {
        public static void Run()
        {
            // ExStart:ApplyLicenseUsingFileStream
            // ExFor:License
            // ExFor:License.SetLicense(System.IO.Stream)
            // ExSummary:Shows how to load a license for Aspose.Note from a stream.

            Aspose.Note.License license = new Aspose.Note.License();
            using (FileStream myStream = new FileStream("Aspose.Note.lic", FileMode.Open))
            {
                license.SetLicense(myStream);
            }

            // ExEnd:ApplyLicenseUsingFileStream
        }
    }
}

```
