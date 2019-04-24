---
title: Implementación de una tabla de un contenedor de un solo uso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332889"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="11729-103">Implementación de una tabla de un contenedor de un solo uso</span><span class="sxs-lookup"><span data-stu-id="11729-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="11729-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11729-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11729-105">Para tener acceso a la tabla de uso único que pertenece a uno de los contenedores, MAPI llama al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con el **IMAPITable** . interfaces.</span><span class="sxs-lookup"><span data-stu-id="11729-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="11729-106">Se pide al contenedor que devuelva su tabla de un solo uso cuando una aplicación cliente está intentando agregar un destinatario al contenedor.</span><span class="sxs-lookup"><span data-stu-id="11729-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="11729-107">Si el contenedor permite a los destinatarios, el proveedor puede devolver su propia implementación de tabla o llamar a [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md) para devolver la implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="11729-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="11729-108">El conjunto de plantillas de la tabla de un contenedor único debe reflejar el tipo de destinatarios que puede contener el contenedor en particular.</span><span class="sxs-lookup"><span data-stu-id="11729-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="11729-109">Normalmente, esto incluye una o dos plantillas, plantillas para crear un usuario de mensajería individual o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="11729-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="11729-110">Los identificadores de entrada de estas plantillas se encuentran en las propiedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11729-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="11729-111">Sin embargo, los contenedores no son en absoluto limitados a estos tipos de entradas.</span><span class="sxs-lookup"><span data-stu-id="11729-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="11729-112">Pueden contener otros tipos de destinatarios o entradas que no son de destinatario, como directorios.</span><span class="sxs-lookup"><span data-stu-id="11729-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

