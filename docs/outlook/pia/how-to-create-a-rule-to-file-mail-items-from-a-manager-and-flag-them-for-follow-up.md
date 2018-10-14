---
title: Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2fc6f5fe60b2f643590e8f7545804cf6d8a4c11c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405990"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a>Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento

En este ejemplo se muestra cómo configurar una regla para archivar elementos de correo enviados por el administrador de un usuario y marcarlos para seguimiento.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Las reglas de Outlook pueden funcionar en el lado servidor o cliente, según el tipo de cuenta y regla. Hay muchas formas para implementar reglas con el fin de aplicar sus propios esquemas organizativos al organizar los elementos en su buzón. Por ejemplo, puede crear una jerarquía de subcarpetas que organice el correo leído y no leído por áreas temáticas. O bien, puede crear una jerarquía de subcarpetas que corresponda al remitente del mensaje. También, puede clasificar el correo y, después, utilizar las carpetas de búsqueda para agregar el correo por categoría.

El modelo de objetos **Rules**, que incluye un objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) que representa una regla en Outlook, le permite crear reglas mediante programación para aplicar un esquema organizativo determinado, crear una regla específica única para la solución o garantizar que se implementen determinadas reglas para un grupo de usuarios. Al usar el modelo de objetos **Rules**, podrá agregar, editar y eliminar reglas mediante programación. Al usar la colección [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) y el objeto **Rule**, también podrá agregar y eliminar reglas definidas para una sesión y obtener acceso a las mismas. 

Un objeto **Rule** tiene una propiedad [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) que indica si la regla es una regla de envío o recepción. Cuando se crea una regla, se especifica la propiedad **RuleType**, y no se puede modificar a no ser que se elimine y se vuelva a crear la regla con otra propiedad **RuleType**. Los objetos [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) y [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)), los objetos de la colección y los objetos de acción y condición derivados también se usan para permitir la edición de las acciones de las reglas y las condiciones de las reglas.

El modelo de objetos **Rules** no admite todas las reglas que puede crear mediante el Asistente para reglas y alertas de la interfaz de usuario de Outlook, pero sí admite las acciones y condiciones de reglas más comunes. Las reglas creadas con este asistente que se aplican a los mensajes, que incluyen elementos de correo, convocatorias de reunión, solicitudes de tareas, documentos, confirmaciones de entrega, confirmaciones de lectura, respuestas de votaciones y avisos de fuera de la oficina, también se pueden crear mediante programación.

Se puede ejecutar una regla en el servidor de Exchange o en el cliente de Outlook, siempre y cuando el buzón de correo del usuario actual esté alojado en un servidor Exchange. La propiedad [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) del objeto **Rule** devuelve **true** para indicar que la regla se ejecuta en un cliente, y que Outlook debe estar ejecutándose para que se pueda ejecutar la regla. Si la regla se ejecuta en el servidor, no es necesario que Outlook esté en ejecución para que se evalúen las condiciones de la regla y se completen las acciones de la regla.

> [!NOTE]
> No hay ninguna colección independiente que represente las condiciones de excepción de la regla. Use la propiedad [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) del objeto **Rule** para obtener una colección [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) que represente las condiciones de excepción de la regla.

Para crear reglas a través del modelo de objetos de Outlook, siga estos pasos:

1.  Obtenga la colección **Rules** de la propiedad [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) llamando al método [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) en el objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) predeterminado. Use un bloque **try…catch** para incluir a los usuarios que estén desconectados del servidor Exchange. Esto evita que Outlook muestre un error.

2.  Llame al método [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) en el objeto **Rules** para crear una variable de instancia o un objeto **Rule**, especificando un nombre y un parámetro [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).

3.  Use las colecciones [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) y [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) para habilitar las acciones, condiciones y excepciones en el objeto **Rule**. Tenga en cuenta que cualquier condición habilitada en la colección **RuleConditions**, devuelta por la propiedad [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)), se trata como una condición de excepción de regla, y que no se pueden agregar acciones o condiciones personalizadas a la colección.

4.  Establezca la propiedad [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) en **true** para que cualquier acción, condición o excepción de regla determinada esté operativa. Algunas acciones o condiciones, como la propiedad [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)), requieren que se establezcan propiedades adicionales en la acción o condición para guardar sin errores el objeto **Rule**.

5.  Por último, llame al método [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) en la colección **Rules** para guardar las reglas creadas o modificadas. Incluya el método **Save** en un bloque **try... catch** para controlar las excepciones.

En el ejemplo de código siguiente, CreateManagerRule implementa los pasos descritos anteriormente. CreateManagerRule comprueba primero si la propiedad [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) representa un objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), lo que indica que el usuario actual es un usuario de Exchange. Si el usuario actual es un usuario de Exchange, CreateManagerRule obtiene el administrador del usuario actual llamando al método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) en el objeto **ExchangeUser** de la propiedad **CurrentUser** del objeto **NameSpace**. Después se crea una regla de recepción para mover los mensajes recibidos a una subcarpeta de la Bandeja de entrada si se cumplen las condiciones siguientes:

- El mensaje es del administrador del usuario.

- El destinatario se encuentra en la línea **Para:** del mensaje.

- El mensaje no es una actualización ni una convocatoria de reunión.

Por último, el mensaje está marcado para realizar seguimiento hoy. CreateManagerRule también ilustra el adecuado control de errores de las condiciones que podrían provocar una excepción, como que el usuario esté sin conexión o desconectado en modo caché de Exchange.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateManagerRule()
{
    Outlook.ExchangeUser manager;
    Outlook.Folder managerFolder;
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
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
        Outlook.Rules rules;
        try
        {
            rules = Application.Session.DefaultStore.GetRules();
        }
        catch
        {
            Debug.WriteLine("Could not obtain rules collection.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            Outlook.Folders folders =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).Folders;
            try
            {
                managerFolder =
                    folders[displayName] as Outlook.Folder;
            }
            catch
            {
                managerFolder =
                    folders.Add(displayName, Type.Missing)
                    as Outlook.Folder;
            }
            Outlook.Rule rule = rules.Create(displayName,
                Outlook.OlRuleType.olRuleReceive);

            // Rule conditions
            // From condition
            rule.Conditions.From.Recipients.Add(
                manager.PrimarySmtpAddress);
            rule.Conditions.From.Recipients.ResolveAll();
            rule.Conditions.From.Enabled = true;

            // Sent only to me
            rule.Conditions.ToMe.Enabled = true;

            // Rule exceptions
            // Meeting invite or update
            rule.Exceptions.MeetingInviteOrUpdate.Enabled = true;

            // Rule actions
            // MarkAsTask action
            rule.Actions.MarkAsTask.MarkInterval =
                Outlook.OlMarkInterval.olMarkToday;
            rule.Actions.MarkAsTask.FlagTo = "Follow-up";
            rule.Actions.MarkAsTask.Enabled = true;

            // MoveToFolder action
            rule.Actions.MoveToFolder.Folder = managerFolder;
            rule.Actions.MoveToFolder.Enabled = true;
            try
            {
                rules.Save(true);
            }
            catch (Exception ex)
            {
                Debug.WriteLine(ex.Message);
            }
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Reglas](rules.md)

