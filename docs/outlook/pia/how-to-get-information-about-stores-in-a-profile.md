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
# <a name="get-information-about-stores-in-a-profile"></a>Obtener información sobre los almacenes en un perfil

En este ejemplo se muestra cómo obtener y enumerar los almacenes en un perfil.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Puede usar la colección [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para enumerar los almacenes de un perfil determinado. La colección **Stores** proporciona los miembros que muestran información sobre cada objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), por ejemplo, cuando un objeto **Store** se ha agregado o cuando el objeto **Store** va a quitarse del perfil actual. En el siguiente ejemplo de código, EnumerateStores obtiene el objeto **Stores** que representa los almacenes del perfil actual y los enumera. EnumerateStores examina cada objeto **Store** en la colección **Stores**. Si la propiedad [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) devuelve **true**, que indica que es un almacén .pst o .ost, las propiedades [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) y [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) se escriben en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Stores](stores.md) (Almacenes)

