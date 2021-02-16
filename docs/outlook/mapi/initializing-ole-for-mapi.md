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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317230"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="a5e79-103">Inicializar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="a5e79-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="a5e79-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5e79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5e79-105">Si también usa OLE, llame a la función [OLE OleInitialize para](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) inicializar las bibliotecas OLE.</span><span class="sxs-lookup"><span data-stu-id="a5e79-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="a5e79-106">**OleInitialize inicializa** los datos globales de la sesión y prepara las bibliotecas OLE para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="a5e79-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="a5e79-107">Para obtener información sobre cómo **llamar a OleInitialize,** consulta windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a5e79-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

