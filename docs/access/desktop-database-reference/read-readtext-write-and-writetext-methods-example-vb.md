---
title: Ejemplo de los métodos Read, ReadText, Write y WriteText (VB)
TOCTitle: Read, ReadText, Write, and WriteText Methods Example (VB)
ms:assetid: 13e0bb73-0077-2a15-9ea3-4fd7b3b34787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248911(v=office.15)
ms:contentKeyID: 48543377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f706f36cd1f00635d141d7e5ede67c5789025abe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484724"
---
# <a name="read-readtext-write-and-writetext-methods-example-vb"></a><span data-ttu-id="189b1-102">Ejemplo de los métodos Read, ReadText, Write y WriteText (VB)</span><span class="sxs-lookup"><span data-stu-id="189b1-102">Read, ReadText, Write, and WriteText Methods Example (VB)</span></span>


<span data-ttu-id="189b1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="189b1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="189b1-p101">En este ejemplo se muestra cómo leer el contenido de un cuadro de texto en un objeto [Stream](stream-object-ado.md) de texto y en un objeto **Stream** binario. Los demás métodos y propiedades que se muestran son [Position](position-property-ado.md), [Size](size-property-ado.md), [Charset](charset-property-ado.md) y [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="189b1-p101">This example demonstrates how to read the contents of a text box into both a text [Stream](stream-object-ado.md) and a binary **Stream**. Other properties and methods shown include [Position](position-property-ado.md), [Size](size-property-ado.md), [Charset](charset-property-ado.md), and [SetEOS](seteos-method-ado.md).</span></span>

```vb 
 
'BeginReadVB 
Private Sub cmdRead_Click() 
 On Error GoTo ErrorHandler 
 
 'Declare variables 
 Dim objStream As Stream 
 Dim varA As Variant 
 Dim bytA() As Byte 
 Dim i As Integer 
 Dim strBytes As String 
 
 'Instantiate and Open Stream 
 Set objStream = New Stream 
 objStream.Open 
 
 'Write the text content of a textbox to the stream 
 If Text1.Text = "" Then 
 Err.Raise 1, , "The text field is blank." 
 End If 
 objStream.WriteText Text1.Text 
 
 'Display the text contents and size of the stream 
 objStream.Position = 0 
 Debug.Print "Default text:" 
 Debug.Print objStream.ReadText 
 Debug.Print objStream.Size 
 
 'Switch character set and display 
 objStream.Position = 0 
 objStream.Charset = "Windows-1252" 
 Debug.Print "New Charset text:" 
 Debug.Print objStream.ReadText 
 Debug.Print objStream.Size 
 
 'Switch to a binary stream and display 
 objStream.Position = 0 
 objStream.Type = adTypeBinary 
 Debug.Print "Binary:" 
 Debug.Print objStream.Read 
 Debug.Print objStream.Size 
 
 'Load an array of bytes with the text box text 
 ReDim bytA(Len(Text1.Text)) 
 For i = 1 To Len(Text1.Text) 
 bytA(i - 1) = CByte(Asc(Mid(Text1.Text, i, 1))) 
 Next 
 
 'Write the buffer to the binary stream and display 
 objStream.Position = 0 
 objStream.Write bytA() 
 objStream.SetEOS 
 objStream.Position = 0 
 Debug.Print "Binary after Write:" 
 Debug.Print objStream.Read 
 Debug.Print objStream.Size 
 
 'Switch back to a text stream and display 
 Debug.Print "Translated back:" 
 objStream.Position = 0 
 objStream.Type = adTypeText 
 Debug.Print objStream.ReadText 
 Debug.Print objStream.Size 
 
 ' clean up 
 objStream.Close 
 Set objStream = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not objStream Is Nothing Then 
 If objStream.State = adStateOpen Then objStream.Close 
 End If 
 Set objStream = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndReadVB 
```
