---
title: Agregar una acción personalizada como respuesta a un elemento de correo
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359755"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a>Agregar una acción personalizada como respuesta a un elemento de correo

Este ejemplo muestra cómo agregar acciones personalizadas como respuesta a un elemento de correo electrónico mediante el método [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) de la colección [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Puede crear acciones personalizadas mediante programación para que aparezcan en la cinta del grupo **Acciones** en la ficha **Mensaje** en una respuesta de correo electrónico. En el ejemplo de código siguiente, ReplyWithVoiceMail crea y agrega una acción personalizada denominada "Responder con correo de voz" a la barra de comandos del inspector. ReplyWithVoiceMail primero obtiene un objeto [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) y, luego, crea un objeto [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) llamando al método **Add** de la colección **Actions** que está asociada al **MailItem**. Después, establece la propiedad [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) del objeto **Action** en "Responder con correo de voz". También se establecen las propiedades [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)), y [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)). Por último, se guarda el **MailItem**.


> [!NOTE]
> También puede agregar acciones personalizadas en tiempo de diseño con el Outlook Forms Designer.


Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a>Vea también

- [Correo](mail.md)

