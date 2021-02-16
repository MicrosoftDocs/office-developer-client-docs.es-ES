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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427139"
---
# <a name="attattachrenddata"></a><span data-ttu-id="64bef-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="64bef-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="64bef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64bef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64bef-105">El **atributo attAttachRenddata** se codifica como una estructura **RENDDATA** que describe cómo y dónde se representan los datos adjuntos en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="64bef-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="64bef-106">La **estructura RENDDATA** simplemente se codifica en la secuencia TNEF como bytes **sizeof(RENDDATA)** que comienzan por el primer miembro de la estructura **RENDDATA.**</span><span class="sxs-lookup"><span data-stu-id="64bef-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="64bef-107">Si el valor del miembro **dwFlags** de la estructura **RENDDATA** se establece en **MAC_BINARY**, los datos de los siguientes datos adjuntos se almacenan en formato MacBinary; de lo contrario, los datos adjuntos se codifican como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="64bef-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

