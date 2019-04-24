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
# <a name="execute-a-rule-instantly"></a>Ejecutar una regla instantáneamente

En este ejemplo se muestra cómo ejecutar una regla al instante mediante el método [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) del objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Puede hacer que una regla se ejecute inmediatamente llamando al método **Execute** en el objeto **Rule**. Los parámetros del método **Execute** son opcionales; si no se especifican, la regla se aplicará a todos los mensajes en la Bandeja de entrada pero no a las subcarpetas de esta bandeja y se usarán los valores predeterminados para los parámetros. En la tabla siguiente se enumeran los valores predeterminados para los parámetros opcionales del método **Execute**. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro</p></th>
<th><p>Valor predeterminado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ShowProgress</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Carpeta</p></td>
<td><p>Bandeja de entrada</p></td>
</tr>
<tr class="odd">
<td><p>IncludeSubfolders</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>RuleExecuteOption</p></td>
<td><p>OlRuleExecuteOption.olRuleExecuteAllMessages</p></td>
</tr>
</tbody>
</table>


Puede anular una ejecución de la regla mediante el Asistente para reglas y alertas. También puede cancelar una ejecución de la regla si establece el parámetro *ShowProgress* en **true** y, a continuación, cancela el cuadro de diálogo de progreso. Una vez cancelado el cuadro de diálogo de progreso, **Execute** devolverá un error. 

En el ejemplo de código siguiente, ExecuteManagerRule obtiene la regla que se creó en el procedimiento CreateManagerRule del tema [Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md). Después, ExecuteManagerRule comprueba si la regla no es una referencia nula. Si la regla no es una referencia nula, ExecuteManagerRule llama al método **Execute** en la regla con los parámetros predeterminados, lo que ejecuta la regla al instante.

> [!NOTE]
> Para aplicar una regla una vez, independientemente de si la propiedad [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) devuelve **true**, use el método **Rule.Execute**. Para aplicar la regla en la sesión actual y en sesiones posteriores, use la propiedad **Rule.Enabled** y el método [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Reglas](rules.md)

