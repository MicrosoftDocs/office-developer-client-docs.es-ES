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
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a><span data-ttu-id="ee08a-102">Crear una regla para asignar categorías a elementos de correo basándose en varias palabras del asunto</span><span class="sxs-lookup"><span data-stu-id="ee08a-102">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>

<span data-ttu-id="ee08a-103">En este ejemplo se muestra cómo configurar una regla que asigna categorías a elementos de correo basándose en varias palabras del asunto.</span><span class="sxs-lookup"><span data-stu-id="ee08a-103">This example shows how to set up a rule that assigns categories to mail items based on multiple words in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="ee08a-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee08a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ee08a-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="ee08a-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="ee08a-106">En Outlook, se pueden clasificar los elementos para que sea más fácil organizarlos y mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="ee08a-106">In Outlook, items can be categorized for easier organization and display.</span></span> <span data-ttu-id="ee08a-107">El modelo de objetos de Outlook proporciona el objeto [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) y la colección [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) para representar categorías.</span><span class="sxs-lookup"><span data-stu-id="ee08a-107">The Outlook object model provides the [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object and the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection to represent categories.</span></span> <span data-ttu-id="ee08a-108">Para obtener más información sobre el objeto **Category** y la colección **Categories** de un elemento de Outlook, vea [Enumerar y agregar categorías](how-to-enumerate-and-add-categories.md).</span><span class="sxs-lookup"><span data-stu-id="ee08a-108">For more information about the **Category** object and the **Categories** collection for an Outlook item, see [Enumerate and Add Categories](how-to-enumerate-and-add-categories.md).</span></span>

<span data-ttu-id="ee08a-109">Una regla, representada por un objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), puede asignarse con varias condiciones.</span><span class="sxs-lookup"><span data-stu-id="ee08a-109">A rule, represented by a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object, can be assigned with multiple conditions.</span></span> <span data-ttu-id="ee08a-110">Puede obtener o establecer una matriz que represente las condiciones que se van a evaluar o las acciones que se van a completar.</span><span class="sxs-lookup"><span data-stu-id="ee08a-110">You can get or set an array that represents conditions to be evaluated or actions to be completed.</span></span> <span data-ttu-id="ee08a-111">Por ejemplo, la propiedad [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) del objeto [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) devuelve o establece una matriz de elementos de cadena que representa el texto que se va a evaluar por la condición de la regla.</span><span class="sxs-lookup"><span data-stu-id="ee08a-111">For example, the [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) property of the [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) object returns or sets an array of string elements that represents the text to be evaluated by the rule condition.</span></span> <span data-ttu-id="ee08a-112">Para la evaluación, debe asignar una matriz que tenga una o varias cadenas.</span><span class="sxs-lookup"><span data-stu-id="ee08a-112">You must assign an array with one string or multiple strings for evaluation.</span></span> <span data-ttu-id="ee08a-113">Para evaluar varias cadenas de texto asignadas en una matriz, use la operación OR lógica.</span><span class="sxs-lookup"><span data-stu-id="ee08a-113">To evaluate multiple text strings that are assigned in an array, use the logical OR operation.</span></span> 

<span data-ttu-id="ee08a-114">Las propiedades que puede usar para obtener o establecer una matriz son las siguientes: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) y **TextRuleCondition.Text**.</span><span class="sxs-lookup"><span data-stu-id="ee08a-114">The properties that you can use to get or set an array are as follows: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)), and **TextRuleCondition.Text**.</span></span> <span data-ttu-id="ee08a-115">Para obtener más información sobre reglas, vea [Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="ee08a-115">For more information about rules, see [Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span>

<span data-ttu-id="ee08a-116">En el ejemplo siguiente, CreateTextAndCategoryRule usa el método CategoryExists para comprobar si en los elementos de correo del usuario hay categorías con el nombre "Office" u "Outlook" en la colección **Categories**.</span><span class="sxs-lookup"><span data-stu-id="ee08a-116">In the following example, CreateTextAndCategoryRule uses the CategoryExists method to check the user’s mail items for any categories by the name “Office” or “Outlook” in the **Categories** collection.</span></span> <span data-ttu-id="ee08a-117">Si no encuentra ninguna categoría, se agregan.</span><span class="sxs-lookup"><span data-stu-id="ee08a-117">If no categories are found, they are added.</span></span> <span data-ttu-id="ee08a-118">El ejemplo crea después una matriz de cadenas que incluyen “Office, “Outlook” y “2007”.</span><span class="sxs-lookup"><span data-stu-id="ee08a-118">The example then creates an array of strings that include “Office, “Outlook”, and “2007”.</span></span> <span data-ttu-id="ee08a-119">Esta matriz representará las condiciones que se van a evaluar.</span><span class="sxs-lookup"><span data-stu-id="ee08a-119">This array will represent the conditions to be evaluated.</span></span> <span data-ttu-id="ee08a-120">Después, CreateTextAndCategoryRule crea una regla que asigna categorías examinando si hay en el asunto alguna de las condiciones de la matriz mediante la propiedad **Text** del objeto **TextRuleCondition** y la propiedad [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) de la colección [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ee08a-120">CreateTextAndCategoryRule then creates a rule that assigns categories by examining the subject for any of the conditions in the array by using the **Text** property of the **TextRuleCondition** object and the [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collection.</span></span> <span data-ttu-id="ee08a-121">Si se cumple la condición, se asignan las categorías de Office y Outlook al elemento mediante el método [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) del objeto [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ee08a-121">If the condition is satisfied, the categories of Office and Outlook are assigned to the item by using the [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) method of the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) object.</span></span>

<span data-ttu-id="ee08a-122">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ee08a-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ee08a-123">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="ee08a-123">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ee08a-124">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="ee08a-124">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ee08a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee08a-125">See also</span></span>

- [<span data-ttu-id="ee08a-126">Reglas</span><span class="sxs-lookup"><span data-stu-id="ee08a-126">Rules</span></span>](rules.md)

