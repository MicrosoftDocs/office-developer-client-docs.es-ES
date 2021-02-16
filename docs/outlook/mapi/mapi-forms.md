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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409975"
---
# <a name="mapi-forms"></a><span data-ttu-id="6193c-103">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="6193c-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="6193c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6193c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6193c-105">Después de leer esta descripción general de la arquitectura de formulario MAPI, tendrá conocimientos sobre qué son los formularios MAPI y cómo interactúan con otros componentes del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="6193c-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="6193c-106">El propósito de esta sección es proporcionar los conocimientos conceptuales necesarios para implementar sus propios servidores de formulario MAPI.</span><span class="sxs-lookup"><span data-stu-id="6193c-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="6193c-107">Antes de leer esta sección, debe familiarizarse con el material del tema Información general sobre [formularios MAPI.](mapi-forms-overview.md)</span><span class="sxs-lookup"><span data-stu-id="6193c-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6193c-108">Dado que la arquitectura de formulario MAPI se basa en el modelo de objetos componentes (COM), el desarrollo de aplicaciones de servidor de formulario requiere conocimientos de programación COM.</span><span class="sxs-lookup"><span data-stu-id="6193c-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="6193c-109">Para obtener más información sobre COM, consulta la sección COM ActiveX Object Services en Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6193c-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

