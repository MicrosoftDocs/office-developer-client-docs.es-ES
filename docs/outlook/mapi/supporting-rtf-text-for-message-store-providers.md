---
title: Compatibilidad con texto RTF para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414217"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="d4631-103">Compatibilidad con texto RTF para proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="d4631-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="d4631-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4631-105">Algunas aplicaciones cliente permiten a los usuarios usar el formato de texto enriquecido (RTF) en sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="d4631-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="d4631-106">Si su proveedor de almacenamiento de mensajes necesita admitir texto RTF en mensajes, necesita controlar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), además de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d4631-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="d4631-107">Principalmente, esto significa almacenar ambas propiedades y asegurarse de que **PR_BODY** contiene una versión de texto sin formato del texto en **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="d4631-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="d4631-108">La función [RTFSync](rtfsync.md) es útil para este propósito.</span><span class="sxs-lookup"><span data-stu-id="d4631-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="d4631-109">Hay dos marcadores que se pueden establecer en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del objeto de almacén de mensajes que indican a los clientes lo que pueden esperar del proveedor de almacenamiento de mensajes con respecto a los **PR_BODY** y \*\*PR_ \*\*Propiedades de RTF_COMPRESSED en los mensajes del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d4631-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="d4631-110">La marca STORE_RTF_OK indica que el almacén puede generar dinámicamente el valor de la propiedad **PR_BODY** desde la propiedad **PR_RTF_COMPRESSED** , lo que libera a los clientes de la carga de sincronizarlos de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="d4631-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="d4631-111">La marca STORE_UNCOMPRESSED_RTF indica que el proveedor de almacén de mensajes puede admitir datos sin comprimir en **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="d4631-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="d4631-112">Los proveedores de almacenamiento de mensajes que no admiten texto RTF necesitan eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) cuando cambia la propiedad **PR_BODY** para interoperar correctamente con aplicaciones cliente que admiten texto RTF .</span><span class="sxs-lookup"><span data-stu-id="d4631-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4631-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="d4631-113">See also</span></span>



[<span data-ttu-id="d4631-114">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="d4631-114">Message Store Features</span></span>](message-store-features.md)

