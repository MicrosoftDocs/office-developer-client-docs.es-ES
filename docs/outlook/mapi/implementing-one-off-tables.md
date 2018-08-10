---
title: Implementación tablas puntuales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b72b8658270a8e007123df3ead01168208b8d1b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817692"
---
# <a name="implementing-one-off-tables"></a><span data-ttu-id="11932-103">Implementación tablas puntuales</span><span class="sxs-lookup"><span data-stu-id="11932-103">Implementing One-Off Tables</span></span>

<span data-ttu-id="11932-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11932-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11932-105">El proveedor podría implementar una o varias tablas de uso único.</span><span class="sxs-lookup"><span data-stu-id="11932-105">Your provider might implement one or more one-off tables.</span></span> <span data-ttu-id="11932-106">Una tabla de uso único es una lista de resumen de uso único plantillas que se usan para crear a destinatarios, ya sea directamente en un contenedor o en la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="11932-106">A one-off table is a summary list of one-off templates used to create recipients, either directly into a container or into the recipient list of an outgoing message.</span></span> <span data-ttu-id="11932-107">Una plantilla de uso único es un emplean de los usuarios del formulario para escribir datos relevantes para un determinado tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="11932-107">A one-off template is a form users employ for entering data relevant to a particular type of address.</span></span> <span data-ttu-id="11932-108">Cuando el usuario es terminado de trabajar con la plantilla, su proveedor crea el destinatario nuevo y lo agrega al mensaje.</span><span class="sxs-lookup"><span data-stu-id="11932-108">When the user is finished working with the template, your provider creates the new recipient and adds it to the message.</span></span> <span data-ttu-id="11932-109">Normalmente, cada plantilla controla un tipo de una sola dirección.</span><span class="sxs-lookup"><span data-stu-id="11932-109">Typically each template handles a single address type.</span></span> <span data-ttu-id="11932-110">Sin embargo, es posible para una plantilla controlar varios tipos o para varias plantillas controlar el mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="11932-110">However, it is possible for a template to handle multiple types or for multiple templates to handle the same type.</span></span> 
  
<span data-ttu-id="11932-111">El proveedor debe admitir el método **OpenEntry** para cada plantilla que incluye en la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="11932-111">Your provider must support the **OpenEntry** method for each template that it includes in the one-off table.</span></span> <span data-ttu-id="11932-112">La implementación de **OpenEntry** debe recuperar una tabla para mostrar para la plantilla.</span><span class="sxs-lookup"><span data-stu-id="11932-112">The implementation of **OpenEntry** should retrieve a display table for the template.</span></span> <span data-ttu-id="11932-113">MAPI utiliza la tabla de presentación para que la plantilla sea visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="11932-113">MAPI uses the display table to make the template visible to the user.</span></span> 
  
<span data-ttu-id="11932-114">Aunque la mayoría de las filas de tablas de uso único representa plantillas, algunas de las filas se pueden usar para clasificar o de grupo, las plantillas.</span><span class="sxs-lookup"><span data-stu-id="11932-114">Although most of the rows in one-off tables represent templates, some of the rows can be used to categorize, or group, templates.</span></span> <span data-ttu-id="11932-115">Representa una fila en una tabla de uso único o no una plantilla se indica mediante el valor de la columna **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11932-115">Whether or not a row in a one-off table represents a template is indicated by the value of its **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) column.</span></span> <span data-ttu-id="11932-116">Las filas que representan las plantillas tienen la columna PR_SELECTABLE establecida en TRUE; las filas que no se representan las plantillas tienen establecido en FALSE.</span><span class="sxs-lookup"><span data-stu-id="11932-116">Rows that represent templates have the PR_SELECTABLE column set to TRUE; rows that do not represent templates have it set to FALSE.</span></span>
  
<span data-ttu-id="11932-117">MAPI define tres tipos de tablas de uso único:</span><span class="sxs-lookup"><span data-stu-id="11932-117">MAPI defines three types of one-off tables:</span></span>
  
- <span data-ttu-id="11932-118">Una tabla de uso único que refleja las plantillas que admite un contenedor individual</span><span class="sxs-lookup"><span data-stu-id="11932-118">A one-off table that reflects the templates that an individual container supports</span></span>
    
- <span data-ttu-id="11932-119">Una tabla de uso único que refleja todas las plantillas que admita el proveedor</span><span class="sxs-lookup"><span data-stu-id="11932-119">A one-off table that reflects all of the templates that your provider supports</span></span> 
    
- <span data-ttu-id="11932-120">Una tabla de uso único que refleja todas las plantillas de todos los proveedores en el perfil de admitan plus algunas que es compatible con MAPI</span><span class="sxs-lookup"><span data-stu-id="11932-120">A one-off table that reflects all of the templates that all of the providers in the profile support plus some that MAPI supports</span></span>
    
<span data-ttu-id="11932-121">Los dos primeros tipos se implementan los proveedores que admiten a los destinatarios de creación, ya sea en un mensaje o en un contenedor.</span><span class="sxs-lookup"><span data-stu-id="11932-121">The first two types are implemented by providers that support the creation recipients, either onto a message or into a container.</span></span> <span data-ttu-id="11932-122">Su proveedor puede incluir el mismo conjunto o un conjunto diferente de plantillas en sus tablas de uso único.</span><span class="sxs-lookup"><span data-stu-id="11932-122">Your provider can include the same set or a different set of templates in its one-off tables.</span></span> <span data-ttu-id="11932-123">La diferencia principal entre los dos tipos es que la tabla de proveedor debe incluir plantillas para la creación de los destinatarios que se pueden usar en los mensajes salientes y su tabla de contenedor debe incluir plantillas para la creación de los destinatarios que se agregarán a su contenedor.</span><span class="sxs-lookup"><span data-stu-id="11932-123">The main difference between the two types is that your provider table should include templates for creating recipients that can be used on outgoing messages and your container table should include templates for creating recipients to be added to your container.</span></span> <span data-ttu-id="11932-124">Un contenedor sólo puede admitir un conjunto limitado de plantillas, pero la tabla de uso único proveedor debe incluir todas las plantillas del proveedor admite.</span><span class="sxs-lookup"><span data-stu-id="11932-124">A container may only support a restricted set of templates, but the provider one-off table should include every template the provider supports.</span></span>
  
<span data-ttu-id="11932-125">El tercer tipo de tabla de uso único se implementa mediante MAPI; proveedores de obtienen acceso a ella mediante una llamada a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).</span><span class="sxs-lookup"><span data-stu-id="11932-125">The third type of one-off table is implemented by MAPI; providers gain access to it by calling [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).</span></span> <span data-ttu-id="11932-126">En la tabla de uso único de MAPI es la unión de todas las tablas de proveedor; incluye todas las plantillas que admite cada proveedor en el perfil.</span><span class="sxs-lookup"><span data-stu-id="11932-126">The MAPI one-off table is the union of all of the provider tables; it includes every template supported by every provider in the profile.</span></span> <span data-ttu-id="11932-127">También incluye plantillas compatibles con MAPI.</span><span class="sxs-lookup"><span data-stu-id="11932-127">It also includes templates supported by MAPI.</span></span> <span data-ttu-id="11932-128">Puede utilizar esta tabla en lugar de la tabla que solicitó para un contenedor en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="11932-128">Your provider can use this table in place of the table requested for a container.</span></span> <span data-ttu-id="11932-129">Sin embargo, las plantillas de esta tabla también se pueden usar para la creación de destinatarios para los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="11932-129">However, the templates in this table can also be used for creating recipients for outgoing messages.</span></span>
  
