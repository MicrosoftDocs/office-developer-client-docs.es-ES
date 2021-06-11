---
title: Implementación de una tabla de One-Off contenedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417423"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="da6de-103">Implementación de una tabla de One-Off contenedor</span><span class="sxs-lookup"><span data-stu-id="da6de-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="da6de-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da6de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da6de-105">Para obtener acceso a la tabla de uso único que pertenece a uno de los contenedores, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con la interfaz **IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="da6de-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="da6de-106">Se le pide al contenedor que devuelva su tabla de uso único cuando una aplicación cliente intente agregar un destinatario al contenedor.</span><span class="sxs-lookup"><span data-stu-id="da6de-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="da6de-107">Si el contenedor permite a algún destinatario, el proveedor puede devolver su propia implementación de tabla o llamar a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para devolver la implementación MAPI.</span><span class="sxs-lookup"><span data-stu-id="da6de-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="da6de-108">El conjunto de plantillas de la tabla de uso único del contenedor debe reflejar el tipo de destinatarios que puede contener el contenedor en particular.</span><span class="sxs-lookup"><span data-stu-id="da6de-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="da6de-109">Normalmente, esto incluye una o dos plantillas, plantillas para crear un usuario de mensajería individual o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="da6de-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="da6de-110">Los identificadores de entrada de estas plantillas se mantienen en las propiedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6de-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="da6de-111">Sin embargo, los contenedores no están limitados a estos tipos de entradas.</span><span class="sxs-lookup"><span data-stu-id="da6de-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="da6de-112">Pueden contener otros tipos de destinatarios o entradas que no son destinatarios, como directorios.</span><span class="sxs-lookup"><span data-stu-id="da6de-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

