---
title: Mostrar elementos seleccionados en el Explorer activo
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b722bcb404f987a6f07a9fe305046ea6673dc231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356388"
---
# <a name="display-selected-items-in-the-active-explorer"></a><span data-ttu-id="8d7eb-102">Mostrar elementos seleccionados en el Explorer activo</span><span class="sxs-lookup"><span data-stu-id="8d7eb-102">Display selected items in the active Explorer</span></span>

<span data-ttu-id="8d7eb-103">En este ejemplo se muestra cómo usar la clase auxiliar OutlookItem para mostrar cómodamente todos los elementos seleccionados en la ventana del Explorer activo.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-103">This example shows how to use the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="8d7eb-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d7eb-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8d7eb-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="8d7eb-106">El objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) contiene el conjunto de elementos de Outlook seleccionado actualmente en el Explorer activo de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-106">The [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object contains the set of Outlook items currently selected in the active Outlook explorer.</span></span> <span data-ttu-id="8d7eb-107">Ni el Explorer activo, representado por [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), ni el conjunto de elementos seleccionados indica el tipo de los elementos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-107">Neither the active explorer, represented by [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), nor the set of selected items indicates the type of the items that are selected.</span></span> <span data-ttu-id="8d7eb-108">Normalmente, tendrá que identificar primero el tipo de elemento y, luego, llamar al método específico **Display** para ese tipo.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-108">Normally, you would have to first identify the item type and then call the specific **Display** method for that type.</span></span> <span data-ttu-id="8d7eb-109">Como el método **Display** es común a todos los objetos de elementos de Outlook y la clase auxiliar de OutlookItem incluye dicho método, puede aprovechar las ventajas de la clase auxiliar, declarando una instancia del objeto OutlookItem, MyItem, y usando MyItem.Display para mostrar cada elemento de la selección.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-109">Because the **Display** method is common to all Outlook items objects and the OutlookItem helper class includes this method, you can take advantage of the helper class, by declaring an instance of the OutlookItem object, myItem, and using myItem.Display to display each item in the selection.</span></span> <span data-ttu-id="8d7eb-110">Puede ver la implementación de la clase auxiliar de OutlookItem en [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span><span class="sxs-lookup"><span data-stu-id="8d7eb-110">You can see the implementation of the OutlookItem helper class in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span></span>

<span data-ttu-id="8d7eb-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="8d7eb-112">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8d7eb-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="8d7eb-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d7eb-114">See also</span></span>

- [<span data-ttu-id="8d7eb-115">Crear una clase auxiliar para acceder a los miembros de elementos de Outlook comunes</span><span class="sxs-lookup"><span data-stu-id="8d7eb-115">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="8d7eb-116">Elementos generales de Outlook</span><span class="sxs-lookup"><span data-stu-id="8d7eb-116">General Outlook items</span></span>](general-outlook-items.md)

