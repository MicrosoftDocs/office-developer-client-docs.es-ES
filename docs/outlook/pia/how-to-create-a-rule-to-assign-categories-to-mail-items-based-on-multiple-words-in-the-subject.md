---
title: Crear una regla para asignar categorías a elementos de correo basándose en varias palabras del asunto
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f0b8b27eb65ef32f95d5529879dde2721e280e26
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706201"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a>Crear una regla para asignar categorías a elementos de correo basándose en varias palabras del asunto

En este ejemplo se muestra cómo configurar una regla que asigna categorías a elementos de correo basándose en varias palabras del asunto.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En Outlook, se pueden clasificar los elementos para que sea más fácil organizarlos y mostrarlos. El modelo de objetos de Outlook proporciona el objeto [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) y la colección [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) para representar categorías. Para obtener más información sobre el objeto **Category** y la colección **Categories** de un elemento de Outlook, vea [Enumerar y agregar categorías](how-to-enumerate-and-add-categories.md).

Una regla, representada por un objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), puede asignarse con varias condiciones. Puede obtener o establecer una matriz que represente las condiciones que se van a evaluar o las acciones que se van a completar. Por ejemplo, la propiedad [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) del objeto [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) devuelve o establece una matriz de elementos de cadena que representa el texto que se va a evaluar por la condición de la regla. Para la evaluación, debe asignar una matriz que tenga una o varias cadenas. Para evaluar varias cadenas de texto asignadas en una matriz, use la operación OR lógica. 

Las propiedades que puede usar para obtener o establecer una matriz son las siguientes: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) y **TextRuleCondition.Text**. Para obtener más información sobre reglas, vea [Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).

En el ejemplo siguiente, CreateTextAndCategoryRule usa el método CategoryExists para comprobar si en los elementos de correo del usuario hay categorías con el nombre "Office" u "Outlook" en la colección **Categories**. Si no encuentra ninguna categoría, se agregan. El ejemplo crea después una matriz de cadenas que incluyen “Office, “Outlook” y “2007”. Esta matriz representará las condiciones que se van a evaluar. Después, CreateTextAndCategoryRule crea una regla que asigna categorías examinando si hay en el asunto alguna de las condiciones de la matriz mediante la propiedad **Text** del objeto **TextRuleCondition** y la propiedad [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) de la colección [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)). Si se cumple la condición, se asignan las categorías de Office y Outlook al elemento mediante el método [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) del objeto [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateTextAndCategoryRule()
{
    if (!CategoryExists("Office"))
    {
        Application.Session.Categories.Add(
            "Office", Type.Missing, Type.Missing);
    }
    if (!CategoryExists("Outlook"))
    {
        Application.Session.Categories.Add(
            "Outlook", Type.Missing, Type.Missing);
    }
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule textRule =
        rules.Create("Demo Text and Category Rule",
        Outlook.OlRuleType.olRuleReceive);
    Object[] textCondition = 
        { "Office", "Outlook", "2007" };
    Object[] categoryAction = 
        { "Office", "Outlook" };
    textRule.Conditions.BodyOrSubject.Text =
        textCondition;
    textRule.Conditions.BodyOrSubject.Enabled = true;
    textRule.Actions.AssignToCategory.Categories =
        categoryAction;
    textRule.Actions.AssignToCategory.Enabled = true;
    rules.Save(true);
}

// Determines if categoryName exists in Categories collection
private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category =
            Application.Session.Categories[categoryName];
        if (category != null)
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

- [Reglas](rules.md)

