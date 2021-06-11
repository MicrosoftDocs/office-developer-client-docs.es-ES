---
title: Ejecutar una regla instantáneamente
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6bb6ac5422b9785660cb3ec0020c01244002c6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320373"
---
# <a name="execute-a-rule-instantly"></a><span data-ttu-id="7911e-102">Ejecutar una regla instantáneamente</span><span class="sxs-lookup"><span data-stu-id="7911e-102">Execute a rule instantly</span></span>

<span data-ttu-id="7911e-103">En este ejemplo se muestra cómo ejecutar una regla al instante mediante el método [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) del objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7911e-103">This example shows how to execute a rule instantly by using the [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) method of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="7911e-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7911e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7911e-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="7911e-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="7911e-p101">Puede hacer que una regla se ejecute inmediatamente llamando al método **Execute** en el objeto **Rule**. Los parámetros del método **Execute** son opcionales; si no se especifican, la regla se aplicará a todos los mensajes en la Bandeja de entrada pero no a las subcarpetas de esta bandeja y se usarán los valores predeterminados para los parámetros. En la tabla siguiente se enumeran los valores predeterminados para los parámetros opcionales del método **Execute**. </span><span class="sxs-lookup"><span data-stu-id="7911e-p101">You can cause a rule to execute immediately by calling the **Execute** method on the **Rule** object. The parameters to the **Execute** method are optional; if they are not specified, the rule will be applied to all messages in the Inbox but not to the subfolders of the Inbox, and default values for the parameters will be used. The following table lists the default values for the optional parameters of the **Execute** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7911e-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7911e-109">Parameter</span></span></p></th>
<th><p><span data-ttu-id="7911e-110">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7911e-110">Default value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7911e-111">ShowProgress</span><span class="sxs-lookup"><span data-stu-id="7911e-111">ShowProgress</span></span></p></td>
<td><p><span data-ttu-id="7911e-112">False</span><span class="sxs-lookup"><span data-stu-id="7911e-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7911e-113">Carpeta</span><span class="sxs-lookup"><span data-stu-id="7911e-113">Folder</span></span></p></td>
<td><p><span data-ttu-id="7911e-114">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="7911e-114">Inbox</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7911e-115">IncludeSubfolders</span><span class="sxs-lookup"><span data-stu-id="7911e-115">IncludeSubfolders</span></span></p></td>
<td><p><span data-ttu-id="7911e-116">False</span><span class="sxs-lookup"><span data-stu-id="7911e-116">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7911e-117">RuleExecuteOption</span><span class="sxs-lookup"><span data-stu-id="7911e-117">RuleExecuteOption</span></span></p></td>
<td><p><span data-ttu-id="7911e-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span><span class="sxs-lookup"><span data-stu-id="7911e-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7911e-p102">Puede anular una ejecución de la regla mediante el Asistente para reglas y alertas. También puede cancelar una ejecución de la regla si establece el parámetro *ShowProgress* en **true** y, a continuación, cancela el cuadro de diálogo de progreso. Una vez cancelado el cuadro de diálogo de progreso, **Execute** devolverá un error. </span><span class="sxs-lookup"><span data-stu-id="7911e-p102">You can cancel a rule execution by using the Rules and Alerts Wizard. You can also cancel a rule execution by setting the *ShowProgress* parameter to **true** and then canceling the progress dialog box. Once you cancel the progress dialog box, **Execute** will return an error.</span></span>

<span data-ttu-id="7911e-122">En el ejemplo de código siguiente, ExecuteManagerRule obtiene la regla que se creó en el procedimiento CreateManagerRule del tema [Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="7911e-122">In the following code example, ExecuteManagerRule gets the rule that was created in the procedure CreateManagerRule from the topic [Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span> <span data-ttu-id="7911e-123">Después, ExecuteManagerRule comprueba si la regla no es una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="7911e-123">ExecuteManagerRule then checks whether the rule is not a null reference.</span></span> <span data-ttu-id="7911e-124">Si la regla no es una referencia nula, ExecuteManagerRule llama al método **Execute** en la regla con los parámetros predeterminados, lo que ejecuta la regla al instante.</span><span class="sxs-lookup"><span data-stu-id="7911e-124">If the rule is not a null reference, ExecuteManagerRule calls the **Execute** method on the rule with default parameters, instantly executing the rule.</span></span>

> [!NOTE]
> <span data-ttu-id="7911e-125">Para aplicar una regla una vez, independientemente de si la propiedad [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) devuelve **true**, use el método **Rule.Execute**.</span><span class="sxs-lookup"><span data-stu-id="7911e-125">To apply a rule once, regardless of whether the [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) property returns **true**, use the **Rule.Execute** method.</span></span> <span data-ttu-id="7911e-126">Para aplicar la regla en la sesión actual y en sesiones posteriores, use la propiedad **Rule.Enabled** y el método [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="7911e-126">To apply the rule for the current session and beyond the current session, use both the **Rule.Enabled** property and the [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) method.</span></span>

<span data-ttu-id="7911e-127">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7911e-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7911e-128">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="7911e-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7911e-129">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="7911e-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ExecuteManagerRule()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            string managerName = currentUser.
                GetExchangeUser().GetExchangeUserManager().Name;
            Outlook.Rule managerRule =
                Application.Session.DefaultStore.GetRules()[managerName];
            if (managerRule != null)
            {
                managerRule.Execute(false, Type.Missing,
                    Type.Missing, Type.Missing);
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7911e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7911e-130">See also</span></span>

- [<span data-ttu-id="7911e-131">Reglas</span><span class="sxs-lookup"><span data-stu-id="7911e-131">Rules</span></span>](rules.md)

