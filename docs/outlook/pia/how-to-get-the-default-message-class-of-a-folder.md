---
title: Obtener la clase de mensaje predeterminada de una carpeta
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 031b7736ed397b9218ea677442f80595da2aa919
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542565"
---
# <a name="get-the-default-message-class-of-a-folder"></a>Obtener la clase de mensaje predeterminada de una carpeta

En este ejemplo se muestra cómo usar la propiedad [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) para obtener la clase de mensaje predeterminada de una carpeta.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Para obtener la clase de mensaje predeterminada de una carpeta, use la propiedad **DefaultMessageClass** del objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)). Por ejemplo, si un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) tiene una **DefaultMessageClass** de IPM. Contact, esto significa que representa una carpeta de contactos. Sin embargo, si la carpeta tiene un formulario personalizado o un formulario de reemplazo como formulario predeterminado, debe usar el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para determinar la clase de mensaje del formulario predeterminado. La propiedad **DefaultMessageClass** no devuelve la clase de mensaje del formulario predeterminado de la carpeta.

En el ejemplo de código siguiente, el procedimiento GetDefaultMessageClass usa el objeto **PropertyAccessor** para determinar el formulario predeterminado de una carpeta. Si no se encuentra la propiedad de carpeta **PR \_ DEF \_ POST \_ MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) y Outlook genera un error, **el try... catch** block devuelve la **propiedad DefaultMessageClass** para **folder**.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"http://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a>Vea también

- [Folders](folders.md) (Carpetas)

