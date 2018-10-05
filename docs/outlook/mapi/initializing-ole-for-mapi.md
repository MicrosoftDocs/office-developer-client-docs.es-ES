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
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388424"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="fe9de-103">Inicializar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="fe9de-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="fe9de-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe9de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe9de-105">Si también utiliza OLE, llame a la función OLE [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) para inicializar las bibliotecas OLE.</span><span class="sxs-lookup"><span data-stu-id="fe9de-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="fe9de-106">**OleInitialize** inicializa datos globales para la sesión y prepara las bibliotecas OLE para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="fe9de-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="fe9de-107">Para obtener información acerca de la llamada **OleInitialize**, vea el SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="fe9de-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

