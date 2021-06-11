---
title: Enumerar y agregar categorías
TOCTitle: Enumerate and add categories
ms:assetid: 17a94a01-c463-4332-851e-7d280c66d8c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424467(v=office.15)
ms:contentKeyID: 55119829
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 488e00971adb1f2fa38555039478ac830d3c9f7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320415"
---
# <a name="enumerate-and-add-categories"></a>Enumerar y agregar categorías

En este ejemplo se muestra cómo enumerar las categorías y agregar una categoría a la lista principal de categorías.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

El modelo de objetos de Microsoft Outlook admite categorías que ayudan a organizar los elementos de la Bandeja de entrada del usuario. Para mantener un mayor nivel de organización, puede hacer lo siguiente:

- Clasifique los elementos de Outlook y muéstrelos por categoría.
- Aplicar varias categorías de color a un solo elemento de Outlook.
- Agrupar y ordenar elementos de Outlook por categoría de color.
- Asignar teclas de método abreviado a cada categoría de color, lo que permite a los usuarios asignar más fácilmente categorías a los elementos.
- Cree, elimine y cambie las categorías de color mediante programación o mediante una acción del usuario en la interfaz de usuario de Outlook.

Para exponer la funcionalidad de las categorías, el modelo de objetos de Outlook proporciona un objeto [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) que representa una categoría de color definida por el usuario en la lista de categorías principales. La lista principal de categorías contiene categorías de color que se presentan en la interfaz de usuario de Outlook. La lista se representa mediante la colección [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Para crear un objeto **Category**, use el método [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) de la colección **Categories**. Al crear un objeto **Category**, se crea un identificador único global (GUID). Este identificador no se puede cambiar. Se representa mediante la propiedad [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)). No obstante, el nombre, el color y la tecla de acceso directo asociados a una categoría de color pueden cambiarse estableciendo las propiedades [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)) y [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)), respectivamente, del objeto **Category**. La propiedad **Color** puede cambiarse estableciendo u obteniendo su constante [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)). Para reproducir el color de un control personalizado, utilice las siguientes propiedades de solo lectura del objeto **Category**:

  - [CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))

  - [CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))

  - [CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))

Estas propiedades devuelven un valor **OLE\_COLOR**, que depende de la propiedad **Color** del objeto **Category**.

Los elementos de Outlook se muestran en función del nombre de categoría. Cada objeto de elemento tiene una propiedad **Categories** que almacena una cadena delimitada por comas que representa los nombres de categoría. (Por ejemplo, para el [objeto MailItem,](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) se usa la **propiedad MailItem** [Categories).](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) Esto le permite agregar una categoría al elemento, incluso si no existe la categoría en la lista de principal de categorías.


> [!NOTE]
> Si la propiedad **Categories** de un elemento contiene un nombre de categoría que no está en la colección **Categories** del objeto **NameSpace**, el nombre de categoría asociado a ese elemento de Outlook se muestra, pero sin un color asociado. La propiedad **Categories** en un objeto **Item** no devuelve una colección **Categories**.

En el ejemplo de código siguiente, el primer procedimiento, EnumerateCategories, obtiene la lista principal de categorías del usuario actual representada mediante la colección **Categories**. Después enumera los objetos **Category** de la colección y escribe las propiedades **Name** y **CategoryID** en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx). El segundo procedimiento, AddACategory, obtiene la lista principal de categorías del usuario actual y usa el método CategoryExists para comprobar si existe una categoría denominada "ISV" en la colección. Si no existe ninguna categoría con el nombre "ISV", AddACategory agrega una categoría denominada "ISV" a la lista principal de categorías y le asigna un color azul oscuro mediante el método **Add** de la colección **Categories**. También asigna CTRL+F11 como la tecla de método abreviado para la categoría.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateCategories()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    foreach (Outlook.Category category in categories)
    {
        Debug.WriteLine(category.Name);
        Debug.WriteLine(category.CategoryID);
    }
}

private void AddACategory()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    if (!CategoryExists("ISV"))
    {
        Outlook.Category category = categories.Add("ISV",
            Outlook.OlCategoryColor.olCategoryColorDarkBlue,
            Outlook.OlCategoryShortcutKey.olCategoryShortcutKeyCtrlF11);
    }
}

private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category = 
            Application.Session.Categories[categoryName];
        if(category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>Vea también

- [Color categories](color-categories.md) (Categorías de color)

