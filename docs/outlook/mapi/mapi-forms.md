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
ms.openlocfilehash: e3f35126f3887bc1f2979721deb90891b97c9322
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818129"
---
# <a name="mapi-forms"></a><span data-ttu-id="bda6d-103">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="bda6d-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="bda6d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bda6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bda6d-105">Después de leer esta información general de la arquitectura de formulario MAPI, tendrá una idea clara de qué son los formularios MAPI y cómo interactúan con otros componentes del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="bda6d-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="bda6d-106">El propósito de esta sección es ofrecerle el conocimiento conceptual que necesita para implementar sus propios servidores de formulario MAPI.</span><span class="sxs-lookup"><span data-stu-id="bda6d-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="bda6d-107">Antes de leer esta sección, debe familiarizarse con el material en el tema de [Introducción a los formularios MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="bda6d-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bda6d-108">Debido a que la arquitectura de formulario MAPI se basa en el modelo de objetos componentes (COM), desarrollo de aplicaciones de servidor de formulario requiere conocimientos de programación COM.</span><span class="sxs-lookup"><span data-stu-id="bda6d-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="bda6d-109">Para obtener más información acerca de COM, vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="bda6d-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

