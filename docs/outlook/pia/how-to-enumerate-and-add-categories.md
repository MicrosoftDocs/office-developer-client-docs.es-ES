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
# <a name="enumerate-and-add-categories"></a><span data-ttu-id="a66bb-102">Enumerar y agregar categorías</span><span class="sxs-lookup"><span data-stu-id="a66bb-102">Enumerate and add categories</span></span>

<span data-ttu-id="a66bb-103">En este ejemplo se muestra cómo enumerar las categorías y agregar una categoría a la lista principal de categorías.</span><span class="sxs-lookup"><span data-stu-id="a66bb-103">This example shows how to enumerate categories and add a category to the main category list.</span></span>

## <a name="example"></a><span data-ttu-id="a66bb-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66bb-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a66bb-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="a66bb-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a66bb-106">El modelo de objetos de Microsoft Outlook admite categorías que ayudan a organizar los elementos de la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="a66bb-106">The Outlook object model supports categories that help organize items in a user’s Inbox.</span></span> <span data-ttu-id="a66bb-107">Para mantener un mayor nivel de organización, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a66bb-107">To maintain a higher level of organization, you can do the following:</span></span>

- <span data-ttu-id="a66bb-108">Clasifique los elementos de Outlook y muéstrelos por categoría.</span><span class="sxs-lookup"><span data-stu-id="a66bb-108">Categorize Outlook items and display them by category.</span></span>
- <span data-ttu-id="a66bb-109">Aplicar varias categorías de color a un solo elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="a66bb-109">Apply multiple color categories to a single Outlook item.</span></span>
- <span data-ttu-id="a66bb-110">Agrupar y ordenar elementos de Outlook por categoría de color.</span><span class="sxs-lookup"><span data-stu-id="a66bb-110">Group and sort Outlook items by color category.</span></span>
- <span data-ttu-id="a66bb-111">Asignar teclas de método abreviado a cada categoría de color, lo que permite a los usuarios asignar más fácilmente categorías a los elementos.</span><span class="sxs-lookup"><span data-stu-id="a66bb-111">Assign shortcut keys to each color category, enabling users to more easily categorize items.</span></span>
- <span data-ttu-id="a66bb-112">Cree, elimine y cambie las categorías de color mediante programación o mediante una acción del usuario en la interfaz de usuario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="a66bb-112">Create, delete, and change color categories either programmatically, or by user action within the Outlook user interface.</span></span>

<span data-ttu-id="a66bb-113">Para exponer la funcionalidad de las categorías, el modelo de objetos de Outlook proporciona un objeto [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) que representa una categoría de color definida por el usuario en la lista de categorías principales.</span><span class="sxs-lookup"><span data-stu-id="a66bb-113">To expose the functionality of categories, the Outlook object model provides a [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object that represents a single user-defined color category in the main category list.</span></span> <span data-ttu-id="a66bb-114">La lista principal de categorías contiene categorías de color que se presentan en la interfaz de usuario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="a66bb-114">The main category list contains color categories that are presented in the Outlook user interface.</span></span> <span data-ttu-id="a66bb-115">La lista se representa mediante la colección [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a66bb-115">The list is represented by the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="a66bb-116">Para crear un objeto **Category**, use el método [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) de la colección **Categories**.</span><span class="sxs-lookup"><span data-stu-id="a66bb-116">To create a **Category** object, use the [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) method of the **Categories** collection.</span></span> <span data-ttu-id="a66bb-117">Al crear un objeto **Category**, se crea un identificador único global (GUID). Este identificador no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="a66bb-117">When you create a **Category** object, a globally unique identifier (GUID) is created, and this identifier cannot be changed.</span></span> <span data-ttu-id="a66bb-118">Se representa mediante la propiedad [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a66bb-118">It is represented by the [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)) property.</span></span> <span data-ttu-id="a66bb-119">No obstante, el nombre, el color y la tecla de acceso directo asociados a una categoría de color pueden cambiarse estableciendo las propiedades [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)) y [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)), respectivamente, del objeto **Category**.</span><span class="sxs-lookup"><span data-stu-id="a66bb-119">You can, however, change the name, color, and shortcut key associated with a color category by setting the [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)), and [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) properties, respectively, of the **Category** object.</span></span> <span data-ttu-id="a66bb-120">La propiedad **Color** puede cambiarse estableciendo u obteniendo su constante [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a66bb-120">You can change the **Color** property by setting or getting its [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)) constant.</span></span> <span data-ttu-id="a66bb-121">Para reproducir el color de un control personalizado, utilice las siguientes propiedades de solo lectura del objeto **Category**:</span><span class="sxs-lookup"><span data-stu-id="a66bb-121">To reproduce the color in a custom control, use the following read-only properties of the **Category** object:</span></span>

  - <span data-ttu-id="a66bb-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a66bb-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span></span>

  - <span data-ttu-id="a66bb-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a66bb-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span></span>

  - <span data-ttu-id="a66bb-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="a66bb-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span></span>

<span data-ttu-id="a66bb-125">Estas propiedades devuelven un valor **OLE\_COLOR**, que depende de la propiedad **Color** del objeto **Category**.</span><span class="sxs-lookup"><span data-stu-id="a66bb-125">These properties return an **OLE\_COLOR** value, which is dependent on the **Color** property of the **Category** object.</span></span>

<span data-ttu-id="a66bb-126">Los elementos de Outlook se muestran en función del nombre de categoría.</span><span class="sxs-lookup"><span data-stu-id="a66bb-126">Outlook items are displayed based on the category name.</span></span> <span data-ttu-id="a66bb-127">Cada objeto de elemento tiene una propiedad **Categories** que almacena una cadena delimitada por comas que representa los nombres de categoría.</span><span class="sxs-lookup"><span data-stu-id="a66bb-127">Each item object has a **Categories** property that stores a comma-delimited string that represents category names.</span></span> <span data-ttu-id="a66bb-128">(Por ejemplo, para el objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) , usaría la propiedad de \*\*\*\* [categorías](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) MailItem).</span><span class="sxs-lookup"><span data-stu-id="a66bb-128">(For example, for the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object, you would use the **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) property).</span></span> <span data-ttu-id="a66bb-129">Esto le permite agregar una categoría al elemento, incluso si no existe la categoría en la lista de principal de categorías.</span><span class="sxs-lookup"><span data-stu-id="a66bb-129">This enables you to add a category to the item, even if the category is not present in the main category list.</span></span>


> [!NOTE]
> <span data-ttu-id="a66bb-p104">Si la propiedad **Categories** de un elemento contiene un nombre de categoría que no está en la colección **Categories** del objeto **NameSpace**, el nombre de categoría asociado a ese elemento de Outlook se muestra, pero sin un color asociado. La propiedad **Categories** en un objeto **Item** no devuelve una colección **Categories**.</span><span class="sxs-lookup"><span data-stu-id="a66bb-p104">If the **Categories** property of an item contains a category name that is not in the **Categories** collection of the **NameSpace** object, the category name associated with that Outlook item is displayed, but without an associated color. The **Categories** property on an **Item** object does not return a **Categories** collection.</span></span>

<span data-ttu-id="a66bb-132">En el ejemplo de código siguiente, el primer procedimiento, EnumerateCategories, obtiene la lista principal de categorías del usuario actual representada mediante la colección **Categories**.</span><span class="sxs-lookup"><span data-stu-id="a66bb-132">In the following code example, the first procedure, EnumerateCategories, gets the current user’s main list of categories, represented by the **Categories** collection.</span></span> <span data-ttu-id="a66bb-133">Después enumera los objetos **Category** de la colección y escribe las propiedades **Name** y **CategoryID** en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="a66bb-133">It then enumerates the **Category** objects in that collection, and writes the **Name** and **CategoryID** properties to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="a66bb-134">El segundo procedimiento, AddACategory, obtiene la lista principal de categorías del usuario actual y usa el método CategoryExists para comprobar si existe una categoría denominada "ISV" en la colección.</span><span class="sxs-lookup"><span data-stu-id="a66bb-134">The second procedure, AddACategory, gets the current user’s main list of categories and uses the CategoryExists method to check whether a category named “ISV” exists in the collection.</span></span> <span data-ttu-id="a66bb-135">Si no existe ninguna categoría con el nombre "ISV", AddACategory agrega una categoría denominada "ISV" a la lista principal de categorías y le asigna un color azul oscuro mediante el método **Add** de la colección **Categories**.</span><span class="sxs-lookup"><span data-stu-id="a66bb-135">If no category with the name “ISV” exists, AddACategory adds a category named “ISV” to the main category list and assigns it a dark blue color by using the **Add** method of the **Categories** collection.</span></span> <span data-ttu-id="a66bb-136">También asigna CTRL+F11 como la tecla de método abreviado para la categoría.</span><span class="sxs-lookup"><span data-stu-id="a66bb-136">It also assigns CTRL+F11 as the shortcut key for the category.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a66bb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a66bb-137">See also</span></span>

- <span data-ttu-id="a66bb-138">[Color categories](color-categories.md) (Categorías de color)</span><span class="sxs-lookup"><span data-stu-id="a66bb-138">[Color categories](color-categories.md)</span></span>

