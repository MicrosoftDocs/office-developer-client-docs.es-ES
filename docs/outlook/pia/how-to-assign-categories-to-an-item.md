---
title: Asignar categorías a un elemento
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 762fd5954e6ec47aed24a9c91b41839f6d292cd9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407194"
---
# <a name="assign-categories-to-an-item"></a>Asignar categorías a un elemento

En este ejemplo se muestra cómo asignar categorías a un elemento mediante su propiedad **Categories**.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).


Para asignar categorías a un elemento use la propiedad **Categories** del elemento. Este ejemplo de código utiliza la clase auxiliar OutlookItem, definida en [Create a Helper class to access common Outlook item members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) (Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook) para llamar a la propiedad OutlookItem.**Categories** sin tener que convertir antes el elemento. La propiedad **Categories** obtiene o establece las categorías que se representan mediante una cadena delimitada por comas que puede contener un máximo de 255 caracteres. Las comas y los espacios se usan para separar los valores de categoría. Asignar una categoría que no esté en la colección [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) provocará que una categoría no muestre un color.

En el ejemplo de código siguiente, AssignCategories crea una restricción para los elementos que contienen “ISV” en el asunto. Para ello, primero usa una consulta de búsqueda y ubicación DAV (DASL) para filtrar los elementos de la Bandeja de entrada que contienen “ISV” en el asunto. A continuación, AssignCategories itera a través de los elementos filtrados mediante la clase **OutlookItem** y, si la cadena que devuelve **item.Categories** no es una referencia nula o ya se asignó a ISV, la categoría ISV se asigna al elemento.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a>Vea también

- [Color categories](color-categories.md) (Categorías de color)

