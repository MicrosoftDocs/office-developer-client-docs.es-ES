---
title: Administrar la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7a72d0e90e6c28874f341fc9ba7af843a44c5da8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583326"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="382a2-103">Administrar la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="382a2-103">Handling the address book</span></span>
  
<span data-ttu-id="382a2-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="382a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="382a2-105">Controlar la libreta de direcciones MAPI puede incluir la extracci�n de entradas que se usar� como destinatarios del mensaje, modificar propiedades de los destinatarios, adici�n de usuarios de mensajer�a o listas de distribuci�n, creaci�n de uso �nico y mostrar uno o varios de los cuadros de di�logo comunes de direcci�n para permitir a los usuarios examinar informaci�n de direcci�n y realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="382a2-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="382a2-106">[Abrir la libreta de direcciones](opening-the-address-book.md): describe cómo utilizar MAPI para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="382a2-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="382a2-107">[Mostrar el cuadro de diálogo dirección comunes](displaying-the-common-address-dialog-box.md): describe cómo mostrar los contenedores de la libreta de direcciones diferente.</span><span class="sxs-lookup"><span data-stu-id="382a2-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="382a2-108">[Abrir un contenedor de la libreta de direcciones](opening-an-address-book-container.md): describe cómo abrir contenedores de la libreta de direcciones diferente.</span><span class="sxs-lookup"><span data-stu-id="382a2-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="382a2-109">[Configurar las opciones de la libreta de direcciones](setting-address-book-options.md): describe cómo se establecen las propiedades que se describen las opciones para el uso de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="382a2-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="382a2-110">[Creación de un destinatario](creating-a-recipient.md): describe cómo se crean los destinatarios al hacer frente a los mensajes y agregar entradas a contenedores de la libreta de direcciones modificable.</span><span class="sxs-lookup"><span data-stu-id="382a2-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="382a2-111">[Creación de una lista de distribución](creating-a-distribution-list.md): se describe cómo crear una lista de distribución en un contenedor modificable.</span><span class="sxs-lookup"><span data-stu-id="382a2-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="382a2-112">[Copiar un destinatario](copying-a-recipient.md): describe cómo copiar los destinatarios de un contenedor a otro o el mismo contenedor.</span><span class="sxs-lookup"><span data-stu-id="382a2-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="382a2-113">[Eliminación de un destinatario](deleting-a-recipient.md): se describe cómo quitar entradas de la libreta de direcciones de uno o más de un contenedor modificable.</span><span class="sxs-lookup"><span data-stu-id="382a2-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="382a2-114">[Preparación de un destinatario](preparing-a-recipient.md): describe cómo se prepara los destinatarios mediante la conversión de sus identificadores de entrada a corto plazo a los identificadores de entrada a largo plazo y, posiblemente, agregar, cambiar o reordenación de propiedades.</span><span class="sxs-lookup"><span data-stu-id="382a2-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="382a2-115">[Obtener acceso a los miembros de una lista de distribución](accessing-the-members-of-a-distribution-list.md): describe cómo tener acceso a los miembros de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="382a2-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="382a2-116">[Recuperar propiedades de destinatario](retrieving-recipient-properties.md): describe cómo tener acceso a una o varias propiedades de una entrada de la libreta de dirección del destinatario.</span><span class="sxs-lookup"><span data-stu-id="382a2-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="382a2-117">[Búsqueda de la libreta de direcciones](searching-the-address-book.md): se describen los dos niveles de funcionalidad de búsqueda MAPI.</span><span class="sxs-lookup"><span data-stu-id="382a2-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="382a2-118">[Uso de un cuadro de diálogo Búsqueda avanzada](using-an-advanced-search-dialog-box.md): se describe cómo ejecutar una funcionalidad de búsqueda avanzada en un contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="382a2-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="382a2-119">[Resolución de un nombre del destinatario](resolving-a-recipient-name.md): describe cómo resolver un nombre de una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="382a2-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="382a2-120">[Expandir las listas de distribución](expanding-distribution-lists.md): describe cómo solicitar confirmación MAPI para expandir una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="382a2-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

