---
title: Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dba46c851050c3f948ec829ae2340e0492ca135f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360406"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a><span data-ttu-id="6e2bc-102">Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento</span><span class="sxs-lookup"><span data-stu-id="6e2bc-102">Create a rule to file mail items from a manager and flag them for follow-up</span></span>

<span data-ttu-id="6e2bc-103">En este ejemplo se muestra cómo configurar una regla para archivar elementos de correo enviados por el administrador de un usuario y marcarlos para seguimiento.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-103">This example shows how to set up a rule to file mail items from the user’s manager and flag them for follow up.</span></span>

## <a name="example"></a><span data-ttu-id="6e2bc-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e2bc-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6e2bc-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="6e2bc-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="6e2bc-p101">Las reglas de Outlook pueden funcionar en el lado servidor o cliente, según el tipo de cuenta y regla. Hay muchas formas para implementar reglas con el fin de aplicar sus propios esquemas organizativos al organizar los elementos en su buzón. Por ejemplo, puede crear una jerarquía de subcarpetas que organice el correo leído y no leído por áreas temáticas. O bien, puede crear una jerarquía de subcarpetas que corresponda al remitente del mensaje. También, puede clasificar el correo y, después, utilizar las carpetas de búsqueda para agregar el correo por categoría.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-p101">Outlook rules can operate either server-side or client-side, depending on the type of account and rule. There are many ways you can implement rules to enforce your own organizational schemes when you organize items in your mailbox. For example, you can create a subfolder hierarchy that organizes unread mail and read mail by subject area. Or, you can create a subfolder hierarchy that corresponds to the sender of the message. You can also categorize your mail and then use search folders to aggregate the mail by category.</span></span>

<span data-ttu-id="6e2bc-111">El modelo de objetos **Rules**, que incluye un objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) que representa una regla en Outlook, le permite crear reglas mediante programación para aplicar un esquema organizativo determinado, crear una regla específica única para la solución o garantizar que se implementen determinadas reglas para un grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-111">The **Rules** object model, which includes a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object that represents a rule in Outlook, allows you to create rules programmatically to enforce a certain organizational scheme, create a specific rule that is unique to your solution, or ensure that certain rules are deployed to a group of users.</span></span> <span data-ttu-id="6e2bc-112">Al usar el modelo de objetos **Rules**, podrá agregar, editar y eliminar reglas mediante programación.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-112">By using the **Rules** object model, you can programmatically add, edit, and delete rules.</span></span> <span data-ttu-id="6e2bc-113">Al usar la colección [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) y el objeto **Rule**, también podrá agregar y eliminar reglas definidas para una sesión y obtener acceso a las mismas.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-113">By using the [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) collection and the **Rule** object, you can also access, add, and delete rules defined for a session.</span></span> 

<span data-ttu-id="6e2bc-114">Un objeto **Rule** tiene una propiedad [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) que indica si la regla es una regla de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-114">A **Rule** object has a [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) property that indicates whether the rule is a send or receive rule.</span></span> <span data-ttu-id="6e2bc-115">Cuando se crea una regla, se especifica la propiedad **RuleType**, y no se puede modificar a no ser que se elimine y se vuelva a crear la regla con otra propiedad **RuleType**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-115">When a rule is created, the **RuleType** property is specified, and cannot be changed without deleting and re-creating the rule with a different **RuleType** property.</span></span> <span data-ttu-id="6e2bc-116">Los objetos [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) y [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)), los objetos de la colección y los objetos de acción y condición derivados también se usan para permitir la edición de las acciones de las reglas y las condiciones de las reglas.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-116">The [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) and [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) objects, their collection objects, and derived action and condition objects are also used to further support editing rule actions and rule conditions.</span></span>

<span data-ttu-id="6e2bc-p104">El modelo de objetos **Rules** no admite todas las reglas que puede crear mediante el Asistente para reglas y alertas de la interfaz de usuario de Outlook, pero sí admite las acciones y condiciones de reglas más comunes. Las reglas creadas con este asistente que se aplican a los mensajes, que incluyen elementos de correo, convocatorias de reunión, solicitudes de tareas, documentos, confirmaciones de entrega, confirmaciones de lectura, respuestas de votaciones y avisos de fuera de la oficina, también se pueden crear mediante programación.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-p104">The **Rules** object model does not support all rules that you can create by using the Rules and Alert Wizard in the Outlook user interface, but it supports the most commonly used rule actions and conditions. Any rules created by using the Rules and Alerts Wizard that are applied to messages, which include mail items, meeting requests, task requests, documents, delivery receipts, read receipts, voting responses, and out-of-office notices, can also be created programmatically.</span></span>

<span data-ttu-id="6e2bc-119">Se puede ejecutar una regla en el servidor de Exchange o en el cliente de Outlook, siempre y cuando el buzón de correo del usuario actual se hospede en un servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-119">A rule can execute on the Exchange server or on the Outlook client, provided that the current user’s mailbox is hosted on an Exchange server.</span></span> <span data-ttu-id="6e2bc-120">La propiedad [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) del objeto **Rule** devuelve **true** para indicar que la regla se ejecuta en un cliente, y que Outlook debe estar ejecutándose para que se pueda ejecutar la regla.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-120">The [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the **Rule** object returns **true** to indicate that the rule executes on a client, and Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="6e2bc-121">Si la regla se ejecuta en el servidor, no es necesario que Outlook esté en ejecución para que se evalúen las condiciones de la regla y se completen las acciones de la regla.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-121">If the rule executes on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span>

> [!NOTE]
> <span data-ttu-id="6e2bc-122">No hay ninguna colección independiente que represente las condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-122">There is no separate collection that represents rule exception conditions.</span></span> <span data-ttu-id="6e2bc-123">Use la propiedad [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) del objeto **Rule** para obtener una colección [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) que represente las condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-123">Use the [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) property of the **Rule** object to get a [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) collection that represents rule exception conditions.</span></span>

<span data-ttu-id="6e2bc-124">Para crear reglas a través del modelo de objetos de Outlook, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6e2bc-124">To create rules through the Outlook object model, follow these steps:</span></span>

1.  <span data-ttu-id="6e2bc-125">Obtenga la colección **Rules** de la propiedad [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) llamando al método [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) en el objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-125">Get the **Rules** collection from the [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object by calling the [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) method on the default [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object.</span></span> <span data-ttu-id="6e2bc-126">Use un bloque **try…catch** para incluir a los usuarios que estén desconectados del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-126">Use a **try…catch** block to account for the user being offline or disconnected from the Exchange server.</span></span> <span data-ttu-id="6e2bc-127">Esto evita que Outlook muestre un error.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-127">This prevents Outlook from raising an error.</span></span>

2.  <span data-ttu-id="6e2bc-128">Llame al método [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) en el objeto **Rules** para crear una variable de instancia o un objeto **Rule**, especificando un nombre y un parámetro [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6e2bc-128">Call the [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) method on the **Rules** object to create an instance variable or a **Rule** object, specifying a Name and a [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) parameter.</span></span>

3.  <span data-ttu-id="6e2bc-129">Use las colecciones [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) y [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) para habilitar las acciones, condiciones y excepciones en el objeto **Rule**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-129">Use the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) and [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collections to enable actions, conditions, and exceptions on the **Rule** object.</span></span> <span data-ttu-id="6e2bc-130">Tenga en cuenta que cualquier condición habilitada en la colección **RuleConditions**, devuelta por la propiedad [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)), se trata como una condición de excepción de regla, y que no se pueden agregar acciones o condiciones personalizadas integradas a la colección.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-130">Note that any condition enabled in the **RuleConditions** collection, returned by the [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) property, is treated as a rule exception condition, and additional built-in custom actions or conditions cannot be added to the collection.</span></span>

4.  <span data-ttu-id="6e2bc-131">Establezca la propiedad [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) en **true** para que cualquier acción, condición o excepción de regla determinada esté operativa.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-131">Set the [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) property to **true** for any given rule action, condition, or exception to be operational.</span></span> <span data-ttu-id="6e2bc-132">Algunas acciones o condiciones, como la propiedad [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)), requieren que se establezcan propiedades adicionales en la acción o condición para guardar sin errores el objeto **Rule**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-132">Some actions or conditions, such as the [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) property, require that you set additional properties on the action or condition to save the **Rule** object without an error.</span></span>

5.  <span data-ttu-id="6e2bc-133">Por último, llame al método [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) en la colección **Rules** para guardar las reglas creadas o modificadas.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-133">Finally, call the [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) method on the **Rules** collection to save the created or modified rules.</span></span> <span data-ttu-id="6e2bc-134">Incluya el método **Save** en un bloque **try... catch** para controlar las excepciones.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-134">Enclose the **Save** method in a **try…catch** block to handle exceptions.</span></span>

<span data-ttu-id="6e2bc-135">En el ejemplo de código siguiente, CreateManagerRule implementa los pasos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-135">In the following code example, CreateManagerRule implements the steps previously described.</span></span> <span data-ttu-id="6e2bc-136">CreateManagerRule comprueba primero si la propiedad [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) representa un objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), lo que indica que el usuario actual es un usuario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-136">CreateManagerRule first verifies whether the [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) property represents an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, indicating that the current user is an Exchange user.</span></span> <span data-ttu-id="6e2bc-137">Si el usuario actual es un usuario de Exchange, CreateManagerRule obtiene el administrador del usuario actual llamando al método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) en el objeto **ExchangeUser** de la propiedad **CurrentUser** del objeto **NameSpace**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-137">If the current user is an Exchange user, CreateManagerRule gets the current user’s manager by calling the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method on the **ExchangeUser** object of the **CurrentUser** property of the **NameSpace** object.</span></span> <span data-ttu-id="6e2bc-138">Después se crea una regla de recepción para mover los mensajes recibidos a una subcarpeta de la Bandeja de entrada si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="6e2bc-138">A receive rule is then created to move received messages to a subfolder of the Inbox for the following conditions:</span></span>

- <span data-ttu-id="6e2bc-139">El mensaje es del administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-139">The message is from the user’s manager.</span></span>

- <span data-ttu-id="6e2bc-140">El destinatario se encuentra en la línea **Para:** del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-140">The recipient is on the **To:** line of the message.</span></span>

- <span data-ttu-id="6e2bc-141">El mensaje no es una actualización ni una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-141">The message is not a meeting request or update.</span></span>

<span data-ttu-id="6e2bc-p112">Por último, el mensaje está marcado para realizar seguimiento hoy. CreateManagerRule también ilustra el adecuado control de errores de las condiciones que podrían provocar una excepción, como que el usuario esté sin conexión o desconectado en modo caché de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-p112">Finally, the message is flagged for follow-up today. CreateManagerRule also illustrates appropriate error handling for conditions that could raise an exception such as the user being offline or disconnected in cached Exchange mode.</span></span>

<span data-ttu-id="6e2bc-144">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-144">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6e2bc-145">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-145">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6e2bc-146">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="6e2bc-146">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6e2bc-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e2bc-147">See also</span></span>

- [<span data-ttu-id="6e2bc-148">Reglas</span><span class="sxs-lookup"><span data-stu-id="6e2bc-148">Rules</span></span>](rules.md)

