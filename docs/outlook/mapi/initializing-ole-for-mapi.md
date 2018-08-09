---
title: Inicializar OLE para MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817811"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="38398-103">Inicializar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="38398-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="38398-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38398-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38398-105">Si también utiliza OLE, llame a la función OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) para inicializar las bibliotecas OLE.</span><span class="sxs-lookup"><span data-stu-id="38398-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="38398-106">**OleInitialize** inicializa datos globales para la sesión y prepara las bibliotecas OLE para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="38398-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="38398-107">Para obtener información acerca de la llamada **OleInitialize**, vea el SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="38398-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

