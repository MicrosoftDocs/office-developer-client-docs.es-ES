---
title: Ejecutar una regla en un equipo local
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 76587a72d9c77a5484d9aa9788173f9f40f57614
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405843"
---
# <a name="execute-a-rule-on-a-local-computer"></a><span data-ttu-id="ff8ad-102">Ejecutar una regla en un equipo local</span><span class="sxs-lookup"><span data-stu-id="ff8ad-102">Execute a rule on a local computer</span></span>

<span data-ttu-id="ff8ad-103">En este ejemplo se muestra cómo ejecutar una regla en un equipo local mediante la propiedad [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) del objeto [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ff8ad-103">This example shows how to execute a rule on a local computer by using the [P:Microsoft.Office.Interop.Outlook._RuleConditions.OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) property of the [T:Microsoft.Office.Interop.Outlook.RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="ff8ad-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff8ad-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ff8ad-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="ff8ad-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="ff8ad-106">Si el buzón de correo está hospedado en un servidor de Exchange, se puede ejecutar una regla en el servidor de Exchange o en el cliente de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-106">If your mailbox is hosted on an Exchange server, a rule can be executed on the Exchange server or on the Outlook client.</span></span> <span data-ttu-id="ff8ad-107">Si la regla se ejecuta en el servidor, no es necesario que Outlook esté en ejecución para que se evalúen las condiciones de la regla y se completen las acciones de esta.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-107">If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span> <span data-ttu-id="ff8ad-108">Si la regla se ejecuta en el cliente, Outlook debe estar ejecutándose para que se ejecute la regla.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-108">If the rule is executed on the client, Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="ff8ad-109">Si la propiedad [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) del objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) devuelve **true**, la regla se ejecuta en el cliente.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-109">If the [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object returns **true**, the rule is executed on the client.</span></span>

<span data-ttu-id="ff8ad-110">Para las acciones de la regla que se ejecutan en el cliente de forma predeterminada (como, por ejemplo, mostrar una alerta de correo nuevo), se habilitará automáticamente la condición **OnLocalMachine**, y la propiedad [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) se establecerá en **true** para un objeto [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) solo del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-110">For rule actions that execute on the client by default (such as displaying a new mail alert), the **OnLocalMachine** condition will automatically be enabled, and the [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) property is set to **true** for a client-side-only [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) object.</span></span> <span data-ttu-id="ff8ad-111">Para las acciones de la regla que, por lo general, se ejecutan en el servidor, establezca la propiedad **Enabled** del objeto **RuleAction** del lado cliente para habilitar la condición **OnLocalMachine**.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-111">For rule actions that generally execute on the server, set the **Enabled** property of the client-side-only **RuleAction** object to enable the **OnLocalMachine** condition.</span></span> <span data-ttu-id="ff8ad-112">Esto forzará que la regla se ejecute localmente en el cliente.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-112">This will force the rule to execute locally on the client.</span></span> 

<span data-ttu-id="ff8ad-113">Cuando se habilita la condición **OnLocalMachine** para una regla, también se habilita la condición [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) cuando se examina la misma regla desde otro equipo.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-113">When the **OnLocalMachine** condition for a rule is enabled, the [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) condition will also be enabled when the same rule is examined from another machine.</span></span> <span data-ttu-id="ff8ad-114">Una condición de regla de tipo [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indica que la regla solo puede ejecutarse en un equipo específico que no sea el actual, y no puede habilitarse o deshabilitarse mediante programación.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-114">A rule condition of type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indicates that the rule can execute only on a specific computer other than the current one, and cannot be programmatically enabled or disabled.</span></span> <span data-ttu-id="ff8ad-115">Por ejemplo, si se crea una regla en el equipo actual y se habilita la condición **OnLocalMachine**, la regla solo puede ejecutarse en ese equipo.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-115">For example, if a rule is created on the current computer and the **OnLocalMachine** rule condition is enabled, the rule can execute only on that computer.</span></span> <span data-ttu-id="ff8ad-116">Si se ejecuta la misma regla en otro equipo, la regla mostrará que la condición de regla **OnOtherMachine** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-116">When you run the same rule on another computer, the rule will show that the condition **olConditionOtherMachine** is enabled.</span></span>

<span data-ttu-id="ff8ad-117">En el ejemplo siguiente, DemoOnMachineOnly crea una regla y habilita la condición [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) y la acción [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) estableciendo las propiedades **Enabled** en **true**.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-117">In the following code example, DemoOnMachineOnly creates a rule and enables the [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) condition and [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) action by setting the **Enabled** properties to **true**.</span></span> <span data-ttu-id="ff8ad-118">Después, se habilita la condición **OnLocalMachine**, que fuerza que se ejecute localmente una regla del lado del servidor, y se guardan las reglas.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-118">The **OnLocalMachine** condition is then enabled, forcing a server-side rule to execute locally, and the rules are saved.</span></span> <span data-ttu-id="ff8ad-119">De forma predeterminada, en el servidor estarán operativas una acción **Forward** y una condición **OnlyToMe**.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-119">By default, a **Forward** action and **OnlyToMe** condition will operate on the server.</span></span> <span data-ttu-id="ff8ad-120">Una vez que se haya habilitado la condición **OnLocalMachine**, actuarán como una regla del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-120">Once the **OnLocalMachine** condition has been enabled, they will operate as a client-side rule.</span></span>

<span data-ttu-id="ff8ad-121">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-121">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="ff8ad-122">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ff8ad-123">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="ff8ad-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoOnMachineOnly()
{
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule rule =
        rules.Create("Demo Machine Only Rule",
        Outlook.OlRuleType.olRuleReceive);
    rule.Conditions.OnlyToMe.Enabled = true;
    rule.Actions.Forward.Enabled = true;
    rule.Actions.Forward.Recipients.Add("someone@example.com");
    rule.Actions.Forward.Recipients.ResolveAll();

    // Force the rule to execute locally
    rule.Conditions.OnLocalMachine.Enabled = true;
    rules.Save(true);
}
```

## <a name="see-also"></a><span data-ttu-id="ff8ad-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff8ad-124">See also</span></span>

- [<span data-ttu-id="ff8ad-125">Reglas</span><span class="sxs-lookup"><span data-stu-id="ff8ad-125">Rules</span></span>](rules.md)

