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
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405843"
---
# <a name="execute-a-rule-on-a-local-computer"></a>Ejecutar una regla en un equipo local

En este ejemplo se muestra cómo ejecutar una regla en un equipo local mediante la propiedad [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) del objeto [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Si el buzón de correo está hospedado en un servidor de Exchange, se puede ejecutar una regla en el servidor de Exchange o en el cliente de Outlook. Si la regla se ejecuta en el servidor, no es necesario que Outlook esté en ejecución para que se evalúen las condiciones de la regla y se completen las acciones de la regla. Si la regla se ejecuta en el cliente, Outlook debe estar ejecutándose para que se ejecute la regla. Si la propiedad [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) del objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) devuelve **true**, la regla se ejecuta en el cliente.

Para las acciones de la regla que se ejecutan en el cliente de forma predeterminada (como, por ejemplo, mostrar una alerta de correo nuevo), se habilitará automáticamente la propiedad **OnLocalMachine**, y la propiedad [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) se establecerá en **true** para un objeto [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) solo del lado del cliente. Para las acciones de la regla que, por lo general, se ejecutan en el servidor, establezca la propiedad **Enabled** del objeto **RuleAction** del lado del cliente para habilitar la condición **OnLocalMachine**. Esto forzará que la regla se ejecute localmente en el cliente. 

Cuando se habilita la condición **OnLocalMachine** para una regla, también se habilita la condición [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) cuando se examina la misma regla desde otro equipo. Una condición de regla de tipo [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indica que la regla solo puede ejecutarse en un equipo específico que no sea el actual, y no puede habilitarse o deshabilitarse mediante programación. Por ejemplo, si se crea una regla en el equipo actual y se habilita la condición **OnLocalMachine**, la regla solo puede ejecutarse en ese equipo. Si se ejecuta la misma regla en otro equipo, la regla mostrará que la condición de regla **OnOtherMachine** está habilitada.

En el ejemplo siguiente, DemoOnMachineOnly crea una regla y habilita la condición [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) y la acción [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) estableciendo las propiedades **Enabled** en **true**. Después, se habilita la condición **OnLocalMachine**, que fuerza que se ejecute localmente una regla del lado del servidor, y se guardan las reglas. De forma predeterminada, en el servidor estarán operativas una acción **Forward** y una condición **OnlyToMe**. Una vez que se haya habilitado la condición **OnLocalMachine**, actuarán como una regla del lado del cliente.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Reglas](rules.md)

