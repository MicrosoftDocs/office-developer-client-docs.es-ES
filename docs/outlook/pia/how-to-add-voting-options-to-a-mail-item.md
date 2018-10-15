---
title: Agregar opciones de votación a un elemento de correo
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6a65bdd5086a10b2d6e9803047555a8b052ff38e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407173"
---
# <a name="add-voting-options-to-a-mail-item"></a>Agregar opciones de votación a un elemento de correo

Este ejemplo muestra cómo usar la propiedad [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) del objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) para agregar opciones de votación a un mensaje de correo electrónico.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).


Las opciones de votación en los mensajes se usan para darle a los receptores de mensajes una lista de opciones y hacer un seguimiento de sus respuestas. Para crear opciones de votación mediante programación, establezca una cadena, que es una lista delimitada por punto y comas de valores de la propiedad **VotingOptions** del objeto **MailItem**. Los valores de la propiedad **VotingOptions** aparecerán bajo el comando **Votar** en el grupo **Responder ** en la cinta de opciones del mensaje recibido. 

En el siguiente ejemplo, OrderPizza crea opciones de votación en un nuevo mensaje de correo. OrderPizza primero crea un **MailItem** y establece la propiedad **VotingOptions** en “Queso; Champiñón; Jamón; Combinado; Combinado de verduras” y la propiedad [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) en “Pedido de pizza”. Cuando se envía el mensaje “Pedido de pizza” se muestran las opciones de votación a los destinatarios. Para cada respuesta recibida, la opción del destinatario se procesará en la página **Tracking** del mensaje en la carpeta Elementos enviados del remitente.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a>Vea también

- [Correo](mail.md)

