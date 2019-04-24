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
ms.openlocfilehash: 951a1c88d2fd4291ee0b48924de6eda8f43c3e47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351348"
---
# <a name="mapi-forms"></a><span data-ttu-id="70e8b-103">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="70e8b-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="70e8b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70e8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70e8b-105">Después de leer esta información general sobre la arquitectura de formularios MAPI, tendrá conocimientos de qué son los formularios MAPI y cómo interactúan con los demás componentes del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="70e8b-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="70e8b-106">El propósito de esta sección es proporcionarle los conocimientos conceptuales que necesita para implementar sus propios servidores de formularios MAPI.</span><span class="sxs-lookup"><span data-stu-id="70e8b-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="70e8b-107">Antes de leer esta sección, debe familiarizarse con el material del tema de [información general sobre los formularios de MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="70e8b-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="70e8b-108">Debido a que la arquitectura de formularios MAPI se basa en el modelo de objetos componentes (COM), el desarrollo de aplicaciones de servidor de formularios requiere conocimientos de programación COM.</span><span class="sxs-lookup"><span data-stu-id="70e8b-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="70e8b-109">Para obtener más información acerca de COM, vea la sección servicios de objetos ActiveX y COM en el SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="70e8b-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

