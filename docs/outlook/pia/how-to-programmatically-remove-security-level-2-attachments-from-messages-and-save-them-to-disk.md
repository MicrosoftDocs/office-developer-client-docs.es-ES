---
title: Quitar archivos adjuntos de nivel 2 de seguridad de los mensajes y guardarlos en el disco mediante programación.
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 3646ff17a6200a6b46b7796537a40e7bdab40781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406599"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a><span data-ttu-id="fa0f6-102">Quitar archivos adjuntos de nivel 2 de seguridad de los mensajes y guardarlos en el disco mediante programación.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-102">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>

<span data-ttu-id="fa0f6-103">En este ejemplo se muestra cómo quitar archivos adjuntos de nivel 2 de seguridad de mensajes de correo y guardarlos en un disco desde donde se pueden abrir.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-103">This example shows how to remove security Level 2 attachments from e-mail messages and save them to a disk, from where they can be opened.</span></span>

## <a name="example"></a><span data-ttu-id="fa0f6-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa0f6-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fa0f6-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fa0f6-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="fa0f6-106">Outlook protege a los usuarios de un código malintencionado transportado mediante archivos adjuntos de correo con determinadas extensiones de archivo, como .exe o .bat.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-106">Outlook protects users from malicious code transported via email attachments that have certain file extensions such as .exe or .bat.</span></span> <span data-ttu-id="fa0f6-107">Estos archivos adjuntos en concreto se bloquean de forma predeterminada y se identifican como archivos adjuntos de nivel 1.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-107">Those particular attachments are blocked by default and identified as Level 1 attachments.</span></span> <span data-ttu-id="fa0f6-108">Archivos adjuntos de nivel 2 tienen menos posibilidades de contener un código malintencionado, pero los usuarios no pueden abrir un archivo adjunto de nivel 2 directamente desde un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-108">Level 2 attachments have a lesser chance of containing malicious code, but users cannot open a Level 2 attachment directly from an email message.</span></span> <span data-ttu-id="fa0f6-109">Un archivo adjunto de nivel 2 primero debe guardarse en un disco.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-109">A Level 2 attachment must first be saved to a disk.</span></span>

<span data-ttu-id="fa0f6-110">Usando el método [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) en el objeto [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)), puede guardar archivos adjuntos en un disco.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-110">By using the [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) method in the [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) object, you can save attachments to a disk.</span></span> <span data-ttu-id="fa0f6-111">En el ejemplo siguiente, RemoveAttachmentsAndSaveToDisk primero quita todos los archivos adjuntos de nivel 2 con un tamaño mayor que el especificado de los elementos de correo de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-111">In the following code example, RemoveAttachmentsAndSaveToDisk first removes from mail items in a folder all Level 2 attachments that are greater than a specified size.</span></span> <span data-ttu-id="fa0f6-112">Esto se realiza enumerando la propiedad [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) de cada objeto **Attachment** en la colección [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) y quitando las que están iguales a [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="fa0f6-112">This is done by enumerating the [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) property of each **Attachment** object in the [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) collection and removing the ones that are equal to [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)).</span></span> <span data-ttu-id="fa0f6-113">Luego, RemoveAttachmentsAndSaveToDisk guarda los archivos adjuntos eliminados utilizando el método **SaveAsFile**.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-113">RemoveAttachmentsAndSaveToDisk then saves the removed attachment by using the **SaveAsFile** method.</span></span>

> [!NOTE] 
> <span data-ttu-id="fa0f6-114">Las colecciones de Outlook son lineales.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-114">Collections in Outlook are linear.</span></span> <span data-ttu-id="fa0f6-115">Use el operador [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) para que **Attachment**[1] haga referencia a **Attachments**[n], donde n representa el valor de la propiedad [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="fa0f6-115">Collections in Outlook are linear. Use the P:Microsoft.Office.Interop.Outlook.Attachment.Index[n] operator to reference Attachments[1] to Attachments[n] where n represents the value of the P:Microsoft.Office.Interop.Outlook.Attachments.Count property.</span></span>
> 
> <span data-ttu-id="fa0f6-p104">No se puede usar una instrucción **foreach** para quitar elementos de una colección. Para ello, use un operador **Index** para obtener el primer elemento de la colección y, a continuación, elimínelo. A continuación, use una instrucción **while** para determinar si ha eliminado la cantidad de elementos adecuada de la colección. Esto garantizará que se haya iterado la cantidad de elementos correcta de la colección.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-p104">You cannot use a **foreach** statement to remove items in a collection. Instead, use an **Index** operator to obtain the first item in the collection, and then delete the item. Then use a **while** statement to determine when you have deleted the appropriate number of items in the collection. This will ensure that you have iterated over the correct number of items in the collection.</span></span>

<span data-ttu-id="fa0f6-120">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-120">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="fa0f6-121">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fa0f6-122">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="fa0f6-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fa0f6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa0f6-123">See also</span></span>

- [<span data-ttu-id="fa0f6-124">Archivos adjuntos</span><span class="sxs-lookup"><span data-stu-id="fa0f6-124">Attachments</span></span>](attachments.md)

