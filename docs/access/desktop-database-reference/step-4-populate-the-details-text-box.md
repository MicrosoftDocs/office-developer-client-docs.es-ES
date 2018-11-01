---
title: 'Paso 4: Rellenar el cuadro de texto de detalles'
TOCTitle: 'Step 4: Populate the Details Text Box'
ms:assetid: fa5e4482-8986-0c03-1e46-7b7fefb5fb58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250278(v=office.15)
ms:contentKeyID: 48548839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c00fd9d1a13a68361c5b1a7c3c2aa39736b3c88
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867261"
---
# <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="3a28e-102">Paso 4: Rellenar el cuadro de texto de detalles</span><span class="sxs-lookup"><span data-stu-id="3a28e-102">Step 4: Populate the Details Text Box</span></span>


<span data-ttu-id="3a28e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a28e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="3a28e-104">Paso 3: Rellenar el cuadro de texto de detalles</span><span class="sxs-lookup"><span data-stu-id="3a28e-104">Step 4: Populate the Details Text Box</span></span>

<span data-ttu-id="3a28e-105">**Para rellenar el cuadro de texto de detalles**</span><span class="sxs-lookup"><span data-stu-id="3a28e-105">**To populate the Details text box**</span></span>

<span data-ttu-id="3a28e-106">Cree una subrutina nueva denominada recFields e inserte el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a28e-106">Create a new subroutine named recFields and insert the following code:</span></span>

```vb 
 
Sub recFields(r As Record, l As ListBox, t As TextBox) 
    Dim f As Field 
    Dim s As Stream 
    Set s = New Stream 
    Dim str As String 
     
    For Each f In r.Fields 
        l.AddItem f.Name & ": " & f.Value 
    Next 
    t.Text = "" 
    If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
        s.Open r, adModeRead, adOpenStreamFromRecord 
        str = s.ReadText(1) 
        s.Position = 0 
        If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
            s.Charset = "ascii" 
            s.Type = adTypeText 
        End If 
        t.Text = s.ReadText(adReadAll) 
    End If 
End Sub 
```

<span data-ttu-id="3a28e-p101">Este código rellena lstDetails con los campos y valores del registro simple pasado a recFields. Si el recurso es un archivo de texto, se abre un \*\* Stream\*\* de texto a partir del registro. El código determina si el juego de caracteres es ASCII y copia el contenido del **Stream** en txtDetails.</span><span class="sxs-lookup"><span data-stu-id="3a28e-p101">This code populates lstDetails with the fields and values of the simple record passed to recFields. If the resource is a text file, a text **Stream** is opened from the resource record. The code determines if the character set is ASCII and copies the **Stream** contents into txtDetails.</span></span>

