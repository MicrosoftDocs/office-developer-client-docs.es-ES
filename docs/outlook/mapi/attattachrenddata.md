---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331916"
---
# <a name="attattachrenddata"></a><span data-ttu-id="1425e-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="1425e-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="1425e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1425e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1425e-105">El atributo **attAttachRenddata** se codifica como una estructura **RENDDATA** que describe cómo y dónde se representan los datos adjuntos en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1425e-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="1425e-106">La estructura **RENDDATA** se codifica simplemente en la secuencia TNEF como bytes **sizeof (RENDDATA)** , comenzando por el primer miembro de la estructura **RENDDATA** .</span><span class="sxs-lookup"><span data-stu-id="1425e-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="1425e-107">Si el valor del miembro **dwFlags** de la estructura **RENDDATA** se establece en **MAC_BINARY**, los datos de los siguientes datos adjuntos se almacenan en formato MacBinary; de lo contrario, los datos adjuntos se codifican de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="1425e-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

