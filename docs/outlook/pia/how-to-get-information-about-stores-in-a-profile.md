---
title: Obtener información sobre los almacenes en un perfil
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0229294cd6655f9017780ee0d9a7a23de76f2362
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406571"
---
# <a name="get-information-about-stores-in-a-profile"></a><span data-ttu-id="23978-102">Obtener información sobre los almacenes en un perfil</span><span class="sxs-lookup"><span data-stu-id="23978-102">Get information about stores in a profile</span></span>

<span data-ttu-id="23978-103">En este ejemplo se muestra cómo obtener y enumerar los almacenes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="23978-103">This example shows how to get and enumerate stores in a profile.</span></span>

## <a name="example"></a><span data-ttu-id="23978-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23978-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="23978-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="23978-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="23978-106">Puede usar la colección [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para enumerar los almacenes de un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="23978-106">You can use the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to enumerate the stores for a given profile.</span></span> <span data-ttu-id="23978-107">La colección **Stores** proporciona los miembros que muestran información sobre cada objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), por ejemplo, cuando un objeto **Store** se ha agregado o cuando el objeto **Store** va a quitarse del perfil actual.</span><span class="sxs-lookup"><span data-stu-id="23978-107">The **Stores** collection provides members that expose information about each [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, such as when a **Store** object has been added or when a **Store** object is about to be removed in the current profile.</span></span> <span data-ttu-id="23978-108">En el siguiente ejemplo de código, EnumerateStores obtiene el objeto **Stores** que representa los almacenes del perfil actual y los enumera.</span><span class="sxs-lookup"><span data-stu-id="23978-108">In the following code example, EnumerateStores gets the **Stores** object that represents stores in the current profile, and enumerates the stores.</span></span> <span data-ttu-id="23978-109">EnumerateStores examina cada objeto **Store** en la colección **Stores**.</span><span class="sxs-lookup"><span data-stu-id="23978-109">EnumerateStores examines each **Store** object in the **Stores** collection.</span></span> <span data-ttu-id="23978-110">Si la propiedad [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) devuelve **true**, que indica que es un almacén .pst o .ost, las propiedades [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) y [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) se escriben en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="23978-110">If the [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) property returns **true**, indicating that it is a .pst or .ost store, the [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) and [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) properties are written to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="23978-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="23978-111">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="23978-112">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="23978-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="23978-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="23978-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="23978-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="23978-114">See also</span></span>

- <span data-ttu-id="23978-115">[Stores](stores.md) (Almacenes)</span><span class="sxs-lookup"><span data-stu-id="23978-115">[Stores](stores.md)</span></span>

