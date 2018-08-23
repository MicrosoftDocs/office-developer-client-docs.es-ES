---
title: Formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b53cdb4fe379405018555f1cca9fa40ddc5d0fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592489"
---
# <a name="mapi-forms"></a><span data-ttu-id="fff72-103">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="fff72-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="fff72-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fff72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fff72-105">Después de leer esta información general de la arquitectura de formulario MAPI, tendrá una idea clara de qué son los formularios MAPI y cómo interactúan con otros componentes del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="fff72-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="fff72-106">El propósito de esta sección es ofrecerle el conocimiento conceptual que necesita para implementar sus propios servidores de formulario MAPI.</span><span class="sxs-lookup"><span data-stu-id="fff72-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="fff72-107">Antes de leer esta sección, debe familiarizarse con el material en el tema de [Introducción a los formularios MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="fff72-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fff72-108">Debido a que la arquitectura de formulario MAPI se basa en el modelo de objetos componentes (COM), desarrollo de aplicaciones de servidor de formulario requiere conocimientos de programación COM.</span><span class="sxs-lookup"><span data-stu-id="fff72-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="fff72-109">Para obtener más información acerca de COM, vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="fff72-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

