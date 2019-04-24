---
title: Obtener la clase de mensaje predeterminada de una carpeta
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bef6ebe051e669b831dfee752b1b17db0a9023b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320212"
---
# <a name="get-the-default-message-class-of-a-folder"></a><span data-ttu-id="adef9-102">Obtener la clase de mensaje predeterminada de una carpeta</span><span class="sxs-lookup"><span data-stu-id="adef9-102">Get the default message class of a folder</span></span>

<span data-ttu-id="adef9-103">En este ejemplo se muestra cómo usar la propiedad [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) para obtener la clase de mensaje predeterminada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="adef9-103">This example shows how to use the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>

## <a name="example"></a><span data-ttu-id="adef9-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adef9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="adef9-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="adef9-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="adef9-106">Para obtener la clase de mensaje predeterminada de una carpeta, use la propiedad **DefaultMessageClass** del objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="adef9-106">To obtain the default message class for a folder, use the **DefaultMessageClass** property of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span> <span data-ttu-id="adef9-107">Por ejemplo, si un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) tiene una **DefaultMessageClass**de IPM. Contact, esto significa que representa una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="adef9-107">For example, a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that has a **DefaultMessageClass** of IPM.Contact means that it represents a Contact folder.</span></span> <span data-ttu-id="adef9-108">Sin embargo, si la carpeta tiene un formulario personalizado o un formulario de reemplazo como formulario predeterminado, debe usar el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para determinar la clase de mensaje del formulario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="adef9-108">However, if the folder has a custom form or a replacement form as a default form, you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to determine the message class of the default form.</span></span> <span data-ttu-id="adef9-109">La propiedad **DefaultMessageClass** no devuelve la clase de mensaje del formulario predeterminado de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="adef9-109">The **DefaultMessageClass** property does not return the message class of the default form for the folder.</span></span>

<span data-ttu-id="adef9-110">En el ejemplo de código siguiente, el procedimiento GetDefaultMessageClass usa el objeto **PropertyAccessor** para determinar el formulario predeterminado de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="adef9-110">In the following code example, the GetDefaultMessageClass procedure uses the **PropertyAccessor** to determine the default form of a folder.</span></span> <span data-ttu-id="adef9-111">Si no se encuentra la propiedad de la carpeta **PR\_\_Def\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) y Outlook genera un error, el **bloque try... catch** devuelve la propiedad **DefaultMessageClass** de la **carpeta**.</span><span class="sxs-lookup"><span data-stu-id="adef9-111">If the folder property **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) is not found and Outlook raises an error, the **try…catch** block returns the **DefaultMessageClass** property for the **Folder**.</span></span>

<span data-ttu-id="adef9-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="adef9-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="adef9-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="adef9-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="adef9-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="adef9-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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
            @"https://schemas.microsoft.com/mapi/proptag/0x36E5001E";
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

## <a name="see-also"></a><span data-ttu-id="adef9-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="adef9-115">See also</span></span>

- <span data-ttu-id="adef9-116">[Folders](folders.md) (Carpetas)</span><span class="sxs-lookup"><span data-stu-id="adef9-116">[Folders](folders.md)</span></span>

