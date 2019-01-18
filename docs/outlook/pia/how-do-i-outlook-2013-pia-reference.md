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
# <a name="how-do-i-outlook-2013-pia-reference"></a>¿Cómo se puede... (Referencia a PIA de Outlook 2013)

Esta sección contiene temas de tareas de procedimientos y ejemplos de código en Visual Basic y C\# que muestran cómo realizar algunas tareas comunes en Outlook.

Para ejecutar estos ejemplos de código, debe tener instalado Outlook 2010 y Visual Studio 2008,o una versión posterior de estos productos.

Los ejemplos de código que se muestran en sección no requieren que tenga instalado Office Developer Tools para Visual Studio. Sin embargo, puede consultar el portal [Introducción al desarrollo de Office](https://developer.microsoft.com/office/docs) para obtener información sobre cómo usar las herramientas, y consultar [Soluciones de Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) para ver ejemplos de tareas básicas escritas en código administrado.

En esta sección se muestran ejemplos de código de nivel básico e intermedio, y algunos de ellos son adaptaciones del libro [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

El equipo de documentación para desarrolladores de Office agradece los códigos de ejemplo y las ideas sobre tareas que desee enviarnos. Si usamos sus ejemplos de código en el contenido de Outlook, se reconocerá su trabajo con una línea de autor y un vínculo a su sitio web. Para obtener más información, póngase en contacto con nosotros a través de la dirección docthis@microsoft.com.

## <a name="in-this-section"></a>En esta sección 

[Cuentas](accounts.md)

- [Obtener información de la cuenta](how-to-get-account-information.md)
- [Crear un elemento que puede enviarse para una cuenta específica basándose en la carpeta actual](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [Obtener la cuenta de una carpeta](how-to-get-the-account-for-a-folder.md)
- [Obtener información de varias cuentas](how-to-get-information-about-multiple-accounts.md)
- [Enviar un elemento de correo con una cuenta de Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[Administración de complementos](add-in-administration.md)

- [Determinar si Outlook es una aplicación de Hacer clic y ejecutar en un equipo](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[Libreta de direcciones](address-book.md)

- [Mostrar en el cuadro de diálogo Seleccionar nombres la libreta de direcciones correspondiente a una carpeta Contactos](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [Obtener la lista global de direcciones o un conjunto de listas de direcciones para un almacén](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [Enumerar las entradas en la lista global de direcciones](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [Mostrar las listas de direcciones para un perfil](how-to-display-the-address-lists-for-a-profile.md)

[Citas](appointments.md)

- [Crear una cita que sea un evento de todo el día](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [Crear una cita que comience en la zona horaria del Pacífico y finalice en la zona horaria oriental](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [Especificar diferentes tipos de destinatarios de un elemento de reunión](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [Crear una cita periódica mediante el patrón de periodicidad predeterminado](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [Crear una cita periódica con un patrón semanal](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [Crear una cita de periodicidad anual que usa un patrón YearNth](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [Buscar una cita específica de una serie de citas periódicas](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [Crear una excepción para una cita en una serie de citas periódicas](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [Crear un recordatorio para un elemento de cita](how-to-create-a-reminder-for-an-appointment-item.md)
- [Importar datos XML de una cita en objetos de citas de Outlook](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[Archivos adjuntos](attachments.md)

- [Adjuntar un archivo a un elemento de correo](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [Adjuntar un elemento de contacto de Outlook a un mensaje de correo electrónico](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [Limitar el tamaño de los datos adjuntos de un mensaje de correo electrónico de Outlook](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [Modificar los datos adjuntos de un mensaje de correo electrónico de Outlook](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [Quitar datos adjuntos de nivel 2 de seguridad de los mensajes y guardarlos en el disco mediante programación](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[Calendario](calendar.md)

- [Compartir la programación de disponibilidad en un período específico de un calendario](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [Compartir información del calendario por correo electrónico](how-to-share-calendar-information-through-e-mail.md)
- [Mostrar un calendario compartido de un destinatario](how-to-display-a-shared-calendar-of-a-recipient.md)
- [Guardar un calendario en el disco](how-to-save-a-calendar-to-disk.md)
- [Abrir y ver los contenidos de un archivo de iCalendar](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[Categorías de color](color-categories.md)

- [Enumerar y agregar categorías](how-to-enumerate-and-add-categories.md)
- [Asignar categorías a un elemento](how-to-assign-categories-to-an-item.md)

[Contactos](contacts.md)

- [Crear un elemento de contacto](how-to-create-a-contact-item.md)
- [Crear un elemento de contacto personalizado](how-to-create-a-custom-contact-item.md)
- [Crear un elemento de contacto desde un archivo vCard y guardar el elemento en una carpeta](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[Conversaciones](conversations.md)

- [Administrar elementos en una conversación](how-to-get-and-display-items-in-a-conversation.md)
- [Obtener y enumerar las conversaciones seleccionadas](how-to-get-and-enumerate-selected-conversations.md)

[Tarjetas de presentación electrónicas](electronic-business-cards.md)

- [Modificar el diseño de una tarjeta de presentación electrónica](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [Enviar un elemento de correo con una tarjeta de presentación electrónica](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[Usuarios de Exchange](exchange-users.md)

- [Obtener información sobre el usuario actual](how-to-get-information-about-the-current-user.md)
- [Obtener información sobre todas las listas de distribución de las que el usuario actual es un miembro](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [Crear una lista de distribución](how-to-create-a-distribution-list.md)
- [Obtener miembros de una lista de distribución de Exchange](how-to-get-members-of-an-exchange-distribution-list.md)
- [Obtener información sobre el administrador de usuario actual](how-to-get-information-about-the-current-user-s-manager.md)
- [Obtener información de disponibilidad de un administrador de usuario de Exchange](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [Consultar la respuesta de un administrador a una convocatoria de reunión](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [Obtener información sobre subordinados directos del administrador del usuario actual](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[Carpetas](folders.md)

- [Agregar una carpeta a la lista de carpetas](how-to-add-a-folder-to-the-folder-list.md)
- [Enumerar carpetas](how-to-enumerate-folders.md)
- [Obtener una carpeta predeterminada y enumerar sus subcarpetas](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [Obtener una carpeta con la ruta de acceso](how-to-get-a-folder-based-on-its-folder-path.md)
- [Seleccionar una carpeta y mostrar la información de la carpeta](how-to-select-a-folder-and-display-folder-information.md)
- [Obtener la clase de mensaje predeterminada de una carpeta](how-to-get-the-default-message-class-of-a-folder.md)
- [Acceder a datos específicos de la solución almacenados como un mensaje oculto en una carpeta](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [Asegurarse de que las propiedades personalizadas del elemento se admiten en las consultas de nivel de carpeta](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[Elementos generales de Outlook](general-outlook-items.md)

- [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Mostrar elementos seleccionados en el Explorer activo](how-to-display-selected-items-in-the-active-explorer.md)

[Uso compartido de grupos](group-sharing.md)

- [Suscribirse a una fuente RSS](how-to-subscribe-to-an-rss-feed.md)
- [Sincronizar Outlook con una carpeta de SharePoint](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[Correo](mail.md)

- [Crear un elemento de correo con una plantilla de mensaje](how-to-create-a-mail-item-by-using-a-message-template.md)
- [Crear un elemento de correo, adjuntar un informe y enviar el elemento de correo al administrador del usuario](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [Enviar un correo electrónico según la dirección SMTP de una cuenta](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [Agregar opciones de votación a un elemento de correo](how-to-add-voting-options-to-a-mail-item.md)
- [Agregar una acción personalizada como respuesta a un elemento de correo](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [Obtener la dirección SMTP del remitente de un elemento de correo](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [Especificar diferentes tipos de destinatarios para un elemento de correo](how-to-specify-different-recipient-types-for-a-mail-item.md)

[Convocatorias de reunión](meeting-requests.md)

- [Crear una convocatoria de reunión, agregar destinatarios y especificar una ubicación](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [Obtener el organizador de una reunión](how-to-get-the-organizer-of-a-meeting.md)
- [Comprobar todas las respuestas a una convocatoria de reunión](how-to-check-all-responses-to-a-meeting-request.md)
- [Buscar el elemento de cita asociado a una convocatoria de reunión](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [Aceptar automáticamente una convocatoria de reunión](how-to-automatically-accept-a-meeting-request.md)
- [Mostrar una notificación al usuario para que responda a una convocatoria de reunión](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[Destinatarios](recipients.md)

- [Mostrar el cuadro de diálogo Seleccionar nombres para resolver los destinatarios](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [Usar el cuadro de diálogo Seleccionar nombres para obtener y asignar destinatarios a una cita](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [Obtener la dirección de correo electrónico de un destinatario](how-to-get-the-e-mail-address-of-a-recipient.md)

[Reglas](rules.md)

- [Crear una regla para archivar elementos de correo enviados por un administrador y marcarlos para seguimiento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [Ejecutar una regla instantáneamente](how-to-execute-a-rule-instantly.md)
- [Ejecutar una regla en un equipo local](how-to-execute-a-rule-on-a-local-computer.md)
- [Crear una regla para asignar categorías a elementos de correo basándose en varias palabras del asunto](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[Tareas de ejemplo que usan eventos de Outlook](sample-tasks-using-outlook-events.md)

- [Implementar un contenedor para inspectores y realizar un seguimiento de eventos al nivel del elemento en cada inspector](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[Buscar y filtrar](search-and-filter.md)

- [Filtrar y enumerar de forma eficaz elementos de una carpeta](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [Usar SetColumns para enumerar de forma eficaz elementos de una carpeta](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [Usar matrices para enumerar de forma eficaz elementos de una carpeta](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [Enumerar los elementos de la carpeta Bandeja de entrada en función de la hora de la última modificación](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [Filtrar y mostrar los elementos de la bandeja de entrada modificados en el último mes](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [Filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [Filtrar y mostrar propiedades calculadas al enumerar elementos en una carpeta](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [Enumerar elementos ocultos de una carpeta](how-to-enumerate-hidden-items-in-a-folder.md)
- [Usar la Búsqueda instantánea para buscar en todas las carpetas y todos los almacenes una frase en el asunto](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [Buscar una frase en el cuerpo de los elementos de una carpeta](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [Buscar una frase exacta en los archivos adjuntos de los elementos de una carpeta](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [Buscar y obtener citas de un intervalo de tiempo](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [Filtrar citas periódicas y buscar una cadena en el asunto](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [Buscar y obtener elementos en una vista agregada](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[Sesiones](sessions.md)

- [Obtener e iniciar sesión en una instancia de Outlook](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[Almacenes](stores.md)

- [Obtener información sobre los almacenes en un perfil](how-to-get-information-about-stores-in-a-profile.md)
- [Agregar o eliminar un almacén](how-to-add-or-remove-a-store.md)

[Tareas](tasks.md)

- [Crear un elemento de tarea](how-to-create-a-task-item.md)
- [Asignar una tarea a un destinatario](how-to-assign-a-task-to-a-recipient.md)
- [Mostrar los elementos de solicitud de tarea enviados a un destinatario](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [Responder a un elemento de solicitud de tarea](how-to-respond-to-a-task-request-item.md)
- [Crear una tarea periódica](how-to-create-a-recurring-task.md)
- [Marcar los elementos de correo de un administrador para su seguimiento](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[Vistas](views.md)

- [Crear una vista](how-to-create-a-view.md)
- [Agregar campos a una vista](how-to-add-fields-to-a-view.md)
- [Enumerar elementos de una vista de tabla](how-to-enumerate-items-in-a-table-view.md)



