---
title: Marcar los elementos de correo de un administrador para su seguimiento
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 06e6bdd91198cabeff689681f2999d6fd2cb725a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542593"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a>Marcar los elementos de correo de un administrador para su seguimiento

En este ejemplo se muestra cómo marcar los elementos de correo electrónico que se recibieron desde el administrador del usuario para su seguimiento.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Microsoft Outlook dispone de un sistema de marcación de tareas que permite marcar ciertos elementos de Outlook como los elementos de correo o los elementos de contacto para hacerles un seguimiento. Al marcar un elemento de Outlook para su seguimiento, se muestra información sobre ese elemento de Outlook, junto con otra información basada en tareas, en la **Barra Tareas pendientes** y el módulo de navegación Calendario en la interfaz de usuario de Outlook. La **Barra Tareas pendientes** se muestra como un panel vertical en una configuración habitual de la ventana del explorador de Outlook. Contiene un control del navegador de fechas, próximas citas y elementos que se han marcado para su seguimiento. La **Barra Tareas pendientes** no es extensible y puede establecer opciones de configuración de la **Barra Tareas pendientes** solo a través de la interfaz de usuario de Outlook. Marcar elementos permite organizar y priorizar las tareas y los elementos pendientes.

En el siguiente ejemplo de código se marca un grupo de elementos para un intervalo especificado de seguimiento. El ejemplo obtiene todos los elementos de la Bandeja de entrada del usuario actual que provengan del administrador del usuario actual mediante una consulta de búsqueda DASL (DAV Searching and Locating) para filtrar los mensajes de tipo "IPM.NOTE"con el nombre del administrador como remitente. Luego, marca todos los elementos de acuerdo con el valor [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) de la propiedad [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)). Todos los elementos de alta importancia están marcados para el seguimiento hoy y todos los elementos de normal importancia están marcados para el seguimiento esta semana mediante el método [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).


> [!NOTE]
> La propiedad **Importance** y el método **MarkAsTask** son miembros del objeto **Item**


Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "http://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "http://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager;
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            string filter = "@SQL=" + "\""
                + PR_SENT_REPRESENTING_NAME + "\""
                + " = '" + displayName + "'" + " AND " + "\""
                + PR_MESSAGE_CLASS + "\"" + " = 'IPM.NOTE'";
            Outlook.Items items =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).
                Items.Restrict(filter);
            foreach (Outlook.MailItem mail in items)
            {
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceHigh)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkToday);
                    mail.Save();
                }
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceNormal)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkThisWeek);
                    mail.Save();
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Tareas](tasks.md)

