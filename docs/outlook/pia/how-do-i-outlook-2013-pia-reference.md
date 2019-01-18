---
title: ¿Cómo se puede... (Referencia a PIA de Outlook 2013)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bc4e19271e2747f5ffa8586b9f2ab226d6658b4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711725"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a><span data-ttu-id="5eee2-102">¿Cómo se puede... (Referencia a PIA de Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="5eee2-102">How do I... (Outlook 2013 PIA reference)</span></span>

<span data-ttu-id="5eee2-103">Esta sección contiene temas de tareas de procedimientos y ejemplos de código en Visual Basic y C\# que muestran cómo realizar algunas tareas comunes en Outlook.</span><span class="sxs-lookup"><span data-stu-id="5eee2-103">This section contains procedural tasks topics and code examples in Visual Basic and C\# that demonstrate how to perform some common tasks in Outlook.</span></span>

<span data-ttu-id="5eee2-104">Para ejecutar estos ejemplos de código, debe tener instalado Outlook 2010 y Visual Studio 2008,o una versión posterior de estos productos.</span><span class="sxs-lookup"><span data-stu-id="5eee2-104">To run these code examples, you must have installed Outlook 2010 and Visual Studio 2008, or a later version of these products.</span></span>

<span data-ttu-id="5eee2-105">Los ejemplos de código que se muestran en sección no requieren que tenga instalado Office Developer Tools para Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5eee2-105">The code examples in this section do not require that you have installed Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="5eee2-106">Sin embargo, puede consultar el portal [Introducción al desarrollo de Office](https://developer.microsoft.com/office/docs) para obtener información sobre cómo usar las herramientas, y consultar [Soluciones de Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) para ver ejemplos de tareas básicas escritas en código administrado.</span><span class="sxs-lookup"><span data-stu-id="5eee2-106">However, you can refer to the [Getting started with Office development](https://developer.microsoft.com/office/docs) portal for information about using the tools, and refer to [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) for some basic how-to tasks written in managed code.</span></span>

<span data-ttu-id="5eee2-107">En esta sección se muestran ejemplos de código de nivel básico e intermedio, y algunos de ellos son adaptaciones del libro [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="5eee2-107">Code examples in this section range from the beginner to the intermediate levels, and some of them are adapted from the book [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span></span>

<span data-ttu-id="5eee2-108">El equipo de documentación para desarrolladores de Office agradece los códigos de ejemplo y las ideas sobre tareas que desee enviarnos.</span><span class="sxs-lookup"><span data-stu-id="5eee2-108">The Office Developer Documentation team welcomes your task ideas and code samples.</span></span> <span data-ttu-id="5eee2-109">Si usamos sus ejemplos de código en el contenido de Outlook, se reconocerá su trabajo con una línea de autor y un vínculo a su sitio web.</span><span class="sxs-lookup"><span data-stu-id="5eee2-109">If we use your code samples in Outlook content, we will recognize your work with a byline and a link to your website.</span></span> <span data-ttu-id="5eee2-110">Para obtener más información, póngase en contacto con nosotros a través de la dirección docthis@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5eee2-110">For more information, contact us at docthis@microsoft.com.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5eee2-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5eee2-111">In this section</span></span> 

[<span data-ttu-id="5eee2-112">Cuentas</span><span class="sxs-lookup"><span data-stu-id="5eee2-112">Accounts</span></span>](accounts.md)

- [<span data-ttu-id="5eee2-113">Obtener información de la cuenta</span><span class="sxs-lookup"><span data-stu-id="5eee2-113">Get account information</span></span>](how-to-get-account-information.md)
- [<span data-ttu-id="5eee2-114">Crear un elemento que puede enviarse para una cuenta específica basándose en la carpeta actual</span><span class="sxs-lookup"><span data-stu-id="5eee2-114">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [<span data-ttu-id="5eee2-115">Obtener la cuenta de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-115">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md)
- [<span data-ttu-id="5eee2-116">Obtener información de varias cuentas</span><span class="sxs-lookup"><span data-stu-id="5eee2-116">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md)
- [<span data-ttu-id="5eee2-117">Enviar un elemento de correo con una cuenta de Hotmail</span><span class="sxs-lookup"><span data-stu-id="5eee2-117">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[<span data-ttu-id="5eee2-118">Administración de complementos</span><span class="sxs-lookup"><span data-stu-id="5eee2-118">Add-in administration</span></span>](add-in-administration.md)

- [<span data-ttu-id="5eee2-119">Determinar si Outlook es una aplicación de Hacer clic y ejecutar en un equipo</span><span class="sxs-lookup"><span data-stu-id="5eee2-119">Determine whether Outlook is a Click-to-Run application on a computer</span></span>](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[<span data-ttu-id="5eee2-120">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="5eee2-120">Address book</span></span>](address-book.md)

- [<span data-ttu-id="5eee2-121">Mostrar en el cuadro de diálogo Seleccionar nombres la libreta de direcciones correspondiente a una carpeta Contactos</span><span class="sxs-lookup"><span data-stu-id="5eee2-121">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [<span data-ttu-id="5eee2-122">Obtener la lista global de direcciones o un conjunto de listas de direcciones para un almacén</span><span class="sxs-lookup"><span data-stu-id="5eee2-122">Get the Global Address List or a set of address lists for a store</span></span>](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [<span data-ttu-id="5eee2-123">Enumerar las entradas en la lista global de direcciones</span><span class="sxs-lookup"><span data-stu-id="5eee2-123">Enumerate the entries in the Global Address List</span></span>](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [<span data-ttu-id="5eee2-124">Mostrar las listas de direcciones para un perfil</span><span class="sxs-lookup"><span data-stu-id="5eee2-124">Display the address lists for a profile</span></span>](how-to-display-the-address-lists-for-a-profile.md)

[<span data-ttu-id="5eee2-125">Citas</span><span class="sxs-lookup"><span data-stu-id="5eee2-125">Appointments</span></span>](appointments.md)

- [<span data-ttu-id="5eee2-126">Crear una cita que sea un evento de todo el día</span><span class="sxs-lookup"><span data-stu-id="5eee2-126">Create an appointment that is an all-day event</span></span>](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [<span data-ttu-id="5eee2-127">Crear una cita que comience en la zona horaria del Pacífico y finalice en la zona horaria oriental</span><span class="sxs-lookup"><span data-stu-id="5eee2-127">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [<span data-ttu-id="5eee2-128">Especificar diferentes tipos de destinatarios de un elemento de reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-128">Specify different recipient types for an appointment item</span></span>](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [<span data-ttu-id="5eee2-129">Crear una cita periódica mediante el patrón de periodicidad predeterminado</span><span class="sxs-lookup"><span data-stu-id="5eee2-129">Create a recurring appointment by using the default recurrence pattern</span></span>](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [<span data-ttu-id="5eee2-130">Crear una cita periódica con un patrón semanal</span><span class="sxs-lookup"><span data-stu-id="5eee2-130">Create a recurring appointment that has a weekly pattern</span></span>](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [<span data-ttu-id="5eee2-131">Crear una cita de periodicidad anual que usa un patrón YearNth</span><span class="sxs-lookup"><span data-stu-id="5eee2-131">Create an annual recurring appointment that uses a YearNth pattern</span></span>](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [<span data-ttu-id="5eee2-132">Buscar una cita específica de una serie de citas periódicas</span><span class="sxs-lookup"><span data-stu-id="5eee2-132">Find a specific appointment in a recurring appointment series</span></span>](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="5eee2-133">Crear una excepción para una cita en una serie de citas periódicas</span><span class="sxs-lookup"><span data-stu-id="5eee2-133">Create an exception appointment in a recurring appointment series</span></span>](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="5eee2-134">Crear un recordatorio para un elemento de cita</span><span class="sxs-lookup"><span data-stu-id="5eee2-134">Create a reminder for an appointment item</span></span>](how-to-create-a-reminder-for-an-appointment-item.md)
- [<span data-ttu-id="5eee2-135">Importar datos XML de una cita en objetos de citas de Outlook</span><span class="sxs-lookup"><span data-stu-id="5eee2-135">Import appointment XML data into Outlook appointment objects</span></span>](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[<span data-ttu-id="5eee2-136">Archivos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5eee2-136">Attachments</span></span>](attachments.md)

- [<span data-ttu-id="5eee2-137">Adjuntar un archivo a un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="5eee2-137">Attach a file to a mail item</span></span>](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [<span data-ttu-id="5eee2-138">Adjuntar un elemento de contacto de Outlook a un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="5eee2-138">Attach an Outlook Contact item to an email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [<span data-ttu-id="5eee2-139">Limitar el tamaño de los datos adjuntos de un mensaje de correo electrónico de Outlook</span><span class="sxs-lookup"><span data-stu-id="5eee2-139">Limit the size of an attachment to an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [<span data-ttu-id="5eee2-140">Modificar los datos adjuntos de un mensaje de correo electrónico de Outlook</span><span class="sxs-lookup"><span data-stu-id="5eee2-140">Modify an attachment of an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [<span data-ttu-id="5eee2-141">Quitar datos adjuntos de nivel 2 de seguridad de los mensajes y guardarlos en el disco mediante programación</span><span class="sxs-lookup"><span data-stu-id="5eee2-141">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[<span data-ttu-id="5eee2-142">Calendario</span><span class="sxs-lookup"><span data-stu-id="5eee2-142">Calendar</span></span>](calendar.md)

- [<span data-ttu-id="5eee2-143">Compartir la programación de disponibilidad en un período específico de un calendario</span><span class="sxs-lookup"><span data-stu-id="5eee2-143">Share Free/Busy schedule within a specified period in a calendar</span></span>](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [<span data-ttu-id="5eee2-144">Compartir información del calendario por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="5eee2-144">Share calendar information through email</span></span>](how-to-share-calendar-information-through-e-mail.md)
- [<span data-ttu-id="5eee2-145">Mostrar un calendario compartido de un destinatario</span><span class="sxs-lookup"><span data-stu-id="5eee2-145">Display a shared calendar of a recipient</span></span>](how-to-display-a-shared-calendar-of-a-recipient.md)
- [<span data-ttu-id="5eee2-146">Guardar un calendario en el disco</span><span class="sxs-lookup"><span data-stu-id="5eee2-146">Save a calendar to disk</span></span>](how-to-save-a-calendar-to-disk.md)
- [<span data-ttu-id="5eee2-147">Abrir y ver los contenidos de un archivo de iCalendar</span><span class="sxs-lookup"><span data-stu-id="5eee2-147">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[<span data-ttu-id="5eee2-148">Categorías de color</span><span class="sxs-lookup"><span data-stu-id="5eee2-148">Color categories</span></span>](color-categories.md)

- [<span data-ttu-id="5eee2-149">Enumerar y agregar categorías</span><span class="sxs-lookup"><span data-stu-id="5eee2-149">Enumerate and add categories</span></span>](how-to-enumerate-and-add-categories.md)
- [<span data-ttu-id="5eee2-150">Asignar categorías a un elemento</span><span class="sxs-lookup"><span data-stu-id="5eee2-150">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)

[<span data-ttu-id="5eee2-151">Contactos</span><span class="sxs-lookup"><span data-stu-id="5eee2-151">Contacts</span></span>](contacts.md)

- [<span data-ttu-id="5eee2-152">Crear un elemento de contacto</span><span class="sxs-lookup"><span data-stu-id="5eee2-152">Create a Contact item</span></span>](how-to-create-a-contact-item.md)
- [<span data-ttu-id="5eee2-153">Crear un elemento de contacto personalizado</span><span class="sxs-lookup"><span data-stu-id="5eee2-153">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)
- [<span data-ttu-id="5eee2-154">Crear un elemento de contacto desde un archivo vCard y guardar el elemento en una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-154">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[<span data-ttu-id="5eee2-155">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="5eee2-155">Conversations</span></span>](conversations.md)

- [<span data-ttu-id="5eee2-156">Administrar elementos en una conversación</span><span class="sxs-lookup"><span data-stu-id="5eee2-156">Get and display items in a conversation</span></span>](how-to-get-and-display-items-in-a-conversation.md)
- [<span data-ttu-id="5eee2-157">Obtener y enumerar las conversaciones seleccionadas</span><span class="sxs-lookup"><span data-stu-id="5eee2-157">Get and enumerate selected conversations</span></span>](how-to-get-and-enumerate-selected-conversations.md)

[<span data-ttu-id="5eee2-158">Tarjetas de presentación electrónicas</span><span class="sxs-lookup"><span data-stu-id="5eee2-158">Electronic business cards</span></span>](electronic-business-cards.md)

- [<span data-ttu-id="5eee2-159">Modificar el diseño de una tarjeta de presentación electrónica</span><span class="sxs-lookup"><span data-stu-id="5eee2-159">Modify the layout of an electronic business card</span></span>](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [<span data-ttu-id="5eee2-160">Enviar un elemento de correo con una tarjeta de presentación electrónica</span><span class="sxs-lookup"><span data-stu-id="5eee2-160">Send a mail item with an electronic business card</span></span>](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[<span data-ttu-id="5eee2-161">Usuarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="5eee2-161">Exchange users</span></span>](exchange-users.md)

- [<span data-ttu-id="5eee2-162">Obtener información sobre el usuario actual</span><span class="sxs-lookup"><span data-stu-id="5eee2-162">Get information about the current user</span></span>](how-to-get-information-about-the-current-user.md)
- [<span data-ttu-id="5eee2-163">Obtener información sobre todas las listas de distribución de las que el usuario actual es un miembro</span><span class="sxs-lookup"><span data-stu-id="5eee2-163">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [<span data-ttu-id="5eee2-164">Crear una lista de distribución</span><span class="sxs-lookup"><span data-stu-id="5eee2-164">Create a distribution list</span></span>](how-to-create-a-distribution-list.md)
- [<span data-ttu-id="5eee2-165">Obtener miembros de una lista de distribución de Exchange</span><span class="sxs-lookup"><span data-stu-id="5eee2-165">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)
- [<span data-ttu-id="5eee2-166">Obtener información sobre el administrador de usuario actual</span><span class="sxs-lookup"><span data-stu-id="5eee2-166">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)
- [<span data-ttu-id="5eee2-167">Obtener información de disponibilidad de un administrador de usuario de Exchange</span><span class="sxs-lookup"><span data-stu-id="5eee2-167">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [<span data-ttu-id="5eee2-168">Consultar la respuesta de un administrador a una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-168">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [<span data-ttu-id="5eee2-169">Obtener información sobre subordinados directos del administrador del usuario actual</span><span class="sxs-lookup"><span data-stu-id="5eee2-169">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[<span data-ttu-id="5eee2-170">Carpetas</span><span class="sxs-lookup"><span data-stu-id="5eee2-170">Folders</span></span>](folders.md)

- [<span data-ttu-id="5eee2-171">Agregar una carpeta a la lista de carpetas</span><span class="sxs-lookup"><span data-stu-id="5eee2-171">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md)
- [<span data-ttu-id="5eee2-172">Enumerar carpetas</span><span class="sxs-lookup"><span data-stu-id="5eee2-172">Enumerate folders</span></span>](how-to-enumerate-folders.md)
- [<span data-ttu-id="5eee2-173">Obtener una carpeta predeterminada y enumerar sus subcarpetas</span><span class="sxs-lookup"><span data-stu-id="5eee2-173">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [<span data-ttu-id="5eee2-174">Obtener una carpeta con la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5eee2-174">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)
- [<span data-ttu-id="5eee2-175">Seleccionar una carpeta y mostrar la información de la carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-175">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)
- [<span data-ttu-id="5eee2-176">Obtener la clase de mensaje predeterminada de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-176">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)
- [<span data-ttu-id="5eee2-177">Acceder a datos específicos de la solución almacenados como un mensaje oculto en una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-177">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [<span data-ttu-id="5eee2-178">Asegurarse de que las propiedades personalizadas del elemento se admiten en las consultas de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-178">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[<span data-ttu-id="5eee2-179">Elementos generales de Outlook</span><span class="sxs-lookup"><span data-stu-id="5eee2-179">General Outlook items</span></span>](general-outlook-items.md)

- [<span data-ttu-id="5eee2-180">Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook</span><span class="sxs-lookup"><span data-stu-id="5eee2-180">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="5eee2-181">Mostrar elementos seleccionados en el Explorer activo</span><span class="sxs-lookup"><span data-stu-id="5eee2-181">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)

[<span data-ttu-id="5eee2-182">Uso compartido de grupos</span><span class="sxs-lookup"><span data-stu-id="5eee2-182">Group sharing</span></span>](group-sharing.md)

- [<span data-ttu-id="5eee2-183">Suscribirse a una fuente RSS</span><span class="sxs-lookup"><span data-stu-id="5eee2-183">Subscribe to an RSS feed</span></span>](how-to-subscribe-to-an-rss-feed.md)
- [<span data-ttu-id="5eee2-184">Sincronizar Outlook con una carpeta de SharePoint</span><span class="sxs-lookup"><span data-stu-id="5eee2-184">Synchronize Outlook with a SharePoint folder</span></span>](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[<span data-ttu-id="5eee2-185">Correo</span><span class="sxs-lookup"><span data-stu-id="5eee2-185">Mail</span></span>](mail.md)

- [<span data-ttu-id="5eee2-186">Crear un elemento de correo con una plantilla de mensaje</span><span class="sxs-lookup"><span data-stu-id="5eee2-186">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)
- [<span data-ttu-id="5eee2-187">Crear un elemento de correo, adjuntar un informe y enviar el elemento de correo al administrador del usuario</span><span class="sxs-lookup"><span data-stu-id="5eee2-187">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [<span data-ttu-id="5eee2-188">Enviar un correo electrónico según la dirección SMTP de una cuenta</span><span class="sxs-lookup"><span data-stu-id="5eee2-188">Send an email given the SMTP address of an account</span></span>](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [<span data-ttu-id="5eee2-189">Agregar opciones de votación a un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="5eee2-189">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md)
- [<span data-ttu-id="5eee2-190">Agregar una acción personalizada como respuesta a un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="5eee2-190">Add a custom action as a response to a mail item</span></span>](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [<span data-ttu-id="5eee2-191">Obtener la dirección SMTP del remitente de un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="5eee2-191">Get the SMTP address of the sender of a mail item</span></span>](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [<span data-ttu-id="5eee2-192">Especificar diferentes tipos de destinatarios para un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="5eee2-192">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md)

[<span data-ttu-id="5eee2-193">Convocatorias de reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-193">Meeting requests</span></span>](meeting-requests.md)

- [<span data-ttu-id="5eee2-194">Crear una convocatoria de reunión, agregar destinatarios y especificar una ubicación</span><span class="sxs-lookup"><span data-stu-id="5eee2-194">Create a meeting request, add recipients, and specify a location</span></span>](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [<span data-ttu-id="5eee2-195">Obtener el organizador de una reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-195">Get the organizer of a meeting</span></span>](how-to-get-the-organizer-of-a-meeting.md)
- [<span data-ttu-id="5eee2-196">Comprobar todas las respuestas a una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-196">Check all responses to a meeting request</span></span>](how-to-check-all-responses-to-a-meeting-request.md)
- [<span data-ttu-id="5eee2-197">Buscar el elemento de cita asociado a una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-197">Find the appointment item associated with a meeting request</span></span>](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [<span data-ttu-id="5eee2-198">Aceptar automáticamente una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-198">Automatically accept a meeting request</span></span>](how-to-automatically-accept-a-meeting-request.md)
- [<span data-ttu-id="5eee2-199">Mostrar una notificación al usuario para que responda a una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="5eee2-199">Prompt a user to respond to a meeting request</span></span>](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[<span data-ttu-id="5eee2-200">Destinatarios</span><span class="sxs-lookup"><span data-stu-id="5eee2-200">Recipients</span></span>](recipients.md)

- [<span data-ttu-id="5eee2-201">Mostrar el cuadro de diálogo Seleccionar nombres para resolver los destinatarios</span><span class="sxs-lookup"><span data-stu-id="5eee2-201">Display the Select Names dialog box to resolve recipients</span></span>](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [<span data-ttu-id="5eee2-202">Usar el cuadro de diálogo Seleccionar nombres para obtener y asignar destinatarios a una cita</span><span class="sxs-lookup"><span data-stu-id="5eee2-202">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [<span data-ttu-id="5eee2-203">Obtener la dirección de correo electrónico de un destinatario</span><span class="sxs-lookup"><span data-stu-id="5eee2-203">Get the email address of a recipient</span></span>](how-to-get-the-e-mail-address-of-a-recipient.md)

[<span data-ttu-id="5eee2-204">Reglas</span><span class="sxs-lookup"><span data-stu-id="5eee2-204">Rules</span></span>](rules.md)

- [<span data-ttu-id="5eee2-205">Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento</span><span class="sxs-lookup"><span data-stu-id="5eee2-205">Create a rule to file mail items from a manager and flag them for follow-up</span></span>](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [<span data-ttu-id="5eee2-206">Ejecutar una regla instantáneamente</span><span class="sxs-lookup"><span data-stu-id="5eee2-206">Execute a rule instantly</span></span>](how-to-execute-a-rule-instantly.md)
- [<span data-ttu-id="5eee2-207">Ejecutar una regla en un equipo local</span><span class="sxs-lookup"><span data-stu-id="5eee2-207">Execute a rule on a local computer</span></span>](how-to-execute-a-rule-on-a-local-computer.md)
- [<span data-ttu-id="5eee2-208">Crear una regla para asignar categorías a elementos de correo basándose en varias palabras del asunto</span><span class="sxs-lookup"><span data-stu-id="5eee2-208">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[<span data-ttu-id="5eee2-209">Tareas de ejemplo que usan eventos de Outlook</span><span class="sxs-lookup"><span data-stu-id="5eee2-209">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

- [<span data-ttu-id="5eee2-210">Implementar un contenedor para inspectores y realizar un seguimiento de eventos al nivel del elemento en cada inspector</span><span class="sxs-lookup"><span data-stu-id="5eee2-210">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[<span data-ttu-id="5eee2-211">Buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="5eee2-211">Search and filter</span></span>](search-and-filter.md)

- [<span data-ttu-id="5eee2-212">Filtrar y enumerar de forma eficaz elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-212">Filter and efficiently enumerate items in a folder</span></span>](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="5eee2-213">Usar SetColumns para enumerar de forma eficaz elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-213">Use SetColumns to efficiently enumerate items in a folder</span></span>](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="5eee2-214">Usar matrices para enumerar de forma eficaz elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-214">Use arrays to efficiently enumerate items in a folder</span></span>](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="5eee2-215">Enumerar los elementos de la carpeta Bandeja de entrada en función de la hora de la última modificación</span><span class="sxs-lookup"><span data-stu-id="5eee2-215">Enumerate items in the Inbox based on the last modification time</span></span>](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [<span data-ttu-id="5eee2-216">Filtrar y mostrar los elementos de la bandeja de entrada modificados en el último mes</span><span class="sxs-lookup"><span data-stu-id="5eee2-216">Filter and display Inbox items modified in the last month</span></span>](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [<span data-ttu-id="5eee2-217">Filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-217">Filter and display multivalued properties when enumerating items in a folder</span></span>](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="5eee2-218">Filtrar y mostrar propiedades calculadas al enumerar elementos en una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-218">Filter and display computed properties when enumerating items in a folder</span></span>](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="5eee2-219">Enumerar elementos ocultos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-219">Enumerate hidden items in a folder</span></span>](how-to-enumerate-hidden-items-in-a-folder.md)
- [<span data-ttu-id="5eee2-220">Usar la Búsqueda instantánea para buscar en todas las carpetas y todos los almacenes una frase en el asunto</span><span class="sxs-lookup"><span data-stu-id="5eee2-220">Use instant search to search all folders and all stores for a phrase in the subject</span></span>](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [<span data-ttu-id="5eee2-221">Buscar una frase en el cuerpo de los elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-221">Search for a phrase in the body of items in a folder</span></span>](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [<span data-ttu-id="5eee2-222">Buscar una frase exacta en los archivos adjuntos de los elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5eee2-222">Search attachments of items in a folder for an exact phrase</span></span>](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [<span data-ttu-id="5eee2-223">Buscar y obtener citas de un intervalo de tiempo</span><span class="sxs-lookup"><span data-stu-id="5eee2-223">Search and obtain appointments in a time range</span></span>](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [<span data-ttu-id="5eee2-224">Filtrar citas periódicas y buscar una cadena en el asunto</span><span class="sxs-lookup"><span data-stu-id="5eee2-224">Filter recurring appointments and search for a string in the subject</span></span>](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [<span data-ttu-id="5eee2-225">Buscar y obtener elementos en una vista agregada</span><span class="sxs-lookup"><span data-stu-id="5eee2-225">Search and obtain items in an aggregated view</span></span>](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[<span data-ttu-id="5eee2-226">Sesiones</span><span class="sxs-lookup"><span data-stu-id="5eee2-226">Sessions</span></span>](sessions.md)

- [<span data-ttu-id="5eee2-227">Obtener e iniciar sesión en una instancia de Outlook</span><span class="sxs-lookup"><span data-stu-id="5eee2-227">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[<span data-ttu-id="5eee2-228">Almacenes</span><span class="sxs-lookup"><span data-stu-id="5eee2-228">Stores</span></span>](stores.md)

- [<span data-ttu-id="5eee2-229">Obtener información sobre los almacenes en un perfil</span><span class="sxs-lookup"><span data-stu-id="5eee2-229">Get information about stores in a profile</span></span>](how-to-get-information-about-stores-in-a-profile.md)
- [<span data-ttu-id="5eee2-230">Agregar o eliminar un almacén</span><span class="sxs-lookup"><span data-stu-id="5eee2-230">Add or remove a store</span></span>](how-to-add-or-remove-a-store.md)

[<span data-ttu-id="5eee2-231">Tareas</span><span class="sxs-lookup"><span data-stu-id="5eee2-231">Tasks</span></span>](tasks.md)

- [<span data-ttu-id="5eee2-232">Crear un elemento de tarea</span><span class="sxs-lookup"><span data-stu-id="5eee2-232">Create a task item</span></span>](how-to-create-a-task-item.md)
- [<span data-ttu-id="5eee2-233">Asignar una tarea a un destinatario</span><span class="sxs-lookup"><span data-stu-id="5eee2-233">Assign a task to a recipient</span></span>](how-to-assign-a-task-to-a-recipient.md)
- [<span data-ttu-id="5eee2-234">Mostrar los elementos de solicitud de tarea enviados a un destinatario</span><span class="sxs-lookup"><span data-stu-id="5eee2-234">Display the task request items sent to a recipient</span></span>](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [<span data-ttu-id="5eee2-235">Responder a un elemento de solicitud de tarea</span><span class="sxs-lookup"><span data-stu-id="5eee2-235">Respond to a task request item</span></span>](how-to-respond-to-a-task-request-item.md)
- [<span data-ttu-id="5eee2-236">Crear una tarea periódica</span><span class="sxs-lookup"><span data-stu-id="5eee2-236">Create a recurring task</span></span>](how-to-create-a-recurring-task.md)
- [<span data-ttu-id="5eee2-237">Marcar los elementos de correo de un administrador para su seguimiento</span><span class="sxs-lookup"><span data-stu-id="5eee2-237">Flag mail items from a manager for follow-up</span></span>](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[<span data-ttu-id="5eee2-238">Vistas</span><span class="sxs-lookup"><span data-stu-id="5eee2-238">Views</span></span>](views.md)

- [<span data-ttu-id="5eee2-239">Crear una vista</span><span class="sxs-lookup"><span data-stu-id="5eee2-239">Create a view</span></span>](how-to-create-a-view.md)
- [<span data-ttu-id="5eee2-240">Agregar campos a una vista</span><span class="sxs-lookup"><span data-stu-id="5eee2-240">Add fields to a view</span></span>](how-to-add-fields-to-a-view.md)
- [<span data-ttu-id="5eee2-241">Enumerar elementos de una vista de tabla</span><span class="sxs-lookup"><span data-stu-id="5eee2-241">Enumerate items in a table view</span></span>](how-to-enumerate-items-in-a-table-view.md)



