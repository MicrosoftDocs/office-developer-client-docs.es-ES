---
title: Quitar archivos adjuntos de nivel 2 de seguridad de los mensajes y guardarlos en el disco mediante programación.
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 135f07f4bd3bdc36cee8547106b955b967150df8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706936"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a>Quitar archivos adjuntos de nivel 2 de seguridad de los mensajes y guardarlos en el disco mediante programación.

En este ejemplo se muestra cómo quitar archivos adjuntos de nivel 2 de seguridad de mensajes de correo y guardarlos en un disco desde donde se pueden abrir.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Outlook protege a los usuarios de un código malintencionado transportado mediante archivos adjuntos de correo con determinadas extensiones de archivo, como .exe o .bat. Estos archivos adjuntos en concreto se bloquean de forma predeterminada y se identifican como archivos adjuntos de nivel 1. Archivos adjuntos de nivel 2 tienen menos posibilidades de contener un código malintencionado, pero los usuarios no pueden abrir un archivo adjunto de nivel 2 directamente desde un mensaje de correo electrónico. Un archivo adjunto de nivel 2 primero debe guardarse en un disco.

Usando el método [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) en el objeto [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)), puede guardar archivos adjuntos en un disco. En el ejemplo siguiente, RemoveAttachmentsAndSaveToDisk primero quita todos los archivos adjuntos de nivel 2 con un tamaño mayor que el especificado de los elementos de correo de una carpeta. Esto se realiza enumerando la propiedad [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) de cada objeto **Attachment** en la colección [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) y quitando las que están iguales a [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)). Luego, RemoveAttachmentsAndSaveToDisk guarda los archivos adjuntos eliminados utilizando el método **SaveAsFile**.

> [!NOTE] 
> Las colecciones de Outlook son lineales. Use el operador [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) para que **Attachment**[1] haga referencia a **Attachments**[n], donde n representa el valor de la propiedad [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).
> 
> No se puede usar una instrucción **foreach** para quitar elementos de una colección. Para ello, use un operador **Index** para obtener el primer elemento de la colección y, a continuación, elimínelo. A continuación, use una instrucción **while** para determinar si ha eliminado la cantidad de elementos adecuada de la colección. Esto garantizará que se haya iterado la cantidad de elementos correcta de la colección.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RemoveAttachmentsAndSaveToDisk(string path,
    Outlook.Folder folder, int size)
{
    Outlook.Items attachItems;
    Outlook.Attachment attachment;
    Outlook.Attachments attachments;
    int byValueCount;
    int removeCount;
    bool saveMessage;
    try
    {
        // The restriction will find all items that
        // have attachments and MessageClass = IPM.Note.
        string filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:hasattachment"
            + "\"" + " = True" + " AND " + "\""
            + "https://schemas.microsoft.com/mapi/proptag/0x001A001E"
            + "\"" + " = 'IPM.Note'";
        attachItems = folder.Items.Restrict(filter);
        foreach (Outlook.MailItem mail in attachItems)
        {
            saveMessage = false;
            byValueCount = 0;
            attachments = mail.Attachments;
            // Obtain the count of ByValue attachments.
            foreach (Outlook.Attachment attach in attachments)
            {
                if (attach.Size > size
                    & attach.Type ==
                    Outlook.OlAttachmentType.olByValue)
                {
                    byValueCount = byValueCount + 1;
                }
            }
            if (byValueCount > 0)
            {
                // removeCount is number of attachments to remove.
                removeCount = attachments.Count - byValueCount;
                while (mail.Attachments.Count != removeCount)
                {
                    // Use indexer to obtain 
                    // first attachment in collection.
                    attachment = mail.Attachments[1];
                    // You can refine this code to save 
                    // separate copies of attachments 
                    // with the same name.
                    attachment.SaveAsFile(path + @"\"
                        + attachment.FileName);
                    attachment.Delete();
                    if (saveMessage != true)
                    {
                        saveMessage = true;
                    }
                }
                if (saveMessage)
                {
                    mail.Save();
                }
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>Vea también

- [Archivos adjuntos](attachments.md)

