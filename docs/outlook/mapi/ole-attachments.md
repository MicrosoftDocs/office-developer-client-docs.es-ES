---
title: Datos adjuntos OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: fb716ce014ec3c4b21ce2b021c1a9f6f291d511c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417150"
---
# <a name="ole-attachments"></a><span data-ttu-id="c9e8c-103">Datos adjuntos OLE</span><span class="sxs-lookup"><span data-stu-id="c9e8c-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="c9e8c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9e8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9e8c-p101">Datos adjuntos que son objetos OLE se codifican como objetos stream de OLE 1 para compatibilidad con versiones anteriores. Si el objeto original es realmente un objeto de **IStorage** de OLE 2, se debe convertir el objeto en una secuencia de OLE 1. Esta conversi�n se realiza mediante la funci�n **OleConvertIStorageToOLESTREAM**, que forma parte de las bibliotecas de Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="c9e8c-p101">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility. If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream. This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

