---
title: Implementar una tabla puntual de contenedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 83351e18750ccbffbe60c4e19f9b04a9c94a42e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817663"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="2f577-103">Implementar una tabla puntual de contenedor</span><span class="sxs-lookup"><span data-stu-id="2f577-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="2f577-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2f577-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2f577-105">Para obtener acceso a la tabla de uso único que pertenecen a uno de los contenedores, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con el **IMAPITable** interfaz.</span><span class="sxs-lookup"><span data-stu-id="2f577-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="2f577-106">El contenedor se le pide que devuelva su tabla de uso único cuando una aplicación cliente intenta agregar a un destinatario al contenedor.</span><span class="sxs-lookup"><span data-stu-id="2f577-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="2f577-107">Si el contenedor permite a los destinatarios, su proveedor puede devolver su propia implementación de la tabla o llamar a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para devolver la implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f577-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="2f577-108">El conjunto de plantillas en la tabla de uso único de contenedor debe reflejar el tipo de destinatarios que puede contener el contenedor determinado.</span><span class="sxs-lookup"><span data-stu-id="2f577-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="2f577-109">Normalmente, esto incluye uno o dos plantillas, plantillas para la creación de un usuario de mensajería individual o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="2f577-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="2f577-110">Los identificadores de entrada para estas plantillas se conservan en las propiedades de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) y **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2f577-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="2f577-111">Sin embargo, los contenedores de ninguna manera se limitan a estos tipos de entradas.</span><span class="sxs-lookup"><span data-stu-id="2f577-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="2f577-112">Pueden contener otros tipos de destinatarios o de las entradas de destinatario que no sean tales como los directorios.</span><span class="sxs-lookup"><span data-stu-id="2f577-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

