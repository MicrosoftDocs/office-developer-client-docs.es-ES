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
# <a name="display-selected-items-in-the-active-explorer"></a>Mostrar elementos seleccionados en el Explorer activo

En este ejemplo se muestra cómo usar la clase auxiliar OutlookItem para mostrar cómodamente todos los elementos seleccionados en la ventana del Explorer activo.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

El objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) contiene el conjunto de elementos de Outlook seleccionado actualmente en el Explorer activo de Outlook. Ni el Explorer activo, representado por [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), ni el conjunto de elementos seleccionados indica el tipo de los elementos seleccionados. Normalmente, tendrá que identificar primero el tipo de elemento y, luego, llamar al método específico **Display** para ese tipo. Como el método **Display** es común a todos los objetos de elementos de Outlook y la clase auxiliar de OutlookItem incluye dicho método, puede aprovechar las ventajas de la clase auxiliar, declarando una instancia del objeto OutlookItem, MyItem, y usando MyItem.Display para mostrar cada elemento de la selección. Puede ver la implementación de la clase auxiliar de OutlookItem en [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Crear una clase auxiliar para acceder a los miembros de elementos de Outlook comunes](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Elementos generales de Outlook](general-outlook-items.md)

