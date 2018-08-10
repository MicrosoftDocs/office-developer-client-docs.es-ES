---
title: Admitir texto RTF para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820824"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="508b0-103">Admitir texto RTF para proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="508b0-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="508b0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="508b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="508b0-105">Algunas aplicaciones de cliente permiten a los usuarios usar formato de texto enriquecido (RTF) texto en sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="508b0-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="508b0-106">Si el mensaje almacena las necesidades de proveedor para admitir texto RTF en los mensajes, necesita controlar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), además de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="508b0-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="508b0-107">Principalmente, esto significa que almacenar las dos propiedades y asegurándose de que **PR_BODY** contiene una versión de texto sin formato del texto en **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="508b0-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="508b0-108">La función [RTFSync](rtfsync.md) es útil para este propósito.</span><span class="sxs-lookup"><span data-stu-id="508b0-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="508b0-109">Hay dos indicadores que se pueden establecer en la propiedad de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del objeto de almacén de mensajes que indican a los clientes lo que pueden esperar desde el proveedor de almacén de mensajes con respecto a la **PR_BODY** y **PR_ RTF_COMPRESSED** las propiedades de los mensajes en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="508b0-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="508b0-110">El indicador STORE_RTF_OK indica que el almacén puede generar el valor de la propiedad **PR_BODY** de la propiedad **PR_RTF_COMPRESSED** dinámicamente, lo que evita que los clientes de la carga de sincronización de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="508b0-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="508b0-111">El indicador STORE_UNCOMPRESSED_RTF indica que el proveedor de almacenamiento de mensajes puede admitir datos sin comprimir en **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="508b0-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="508b0-112">Los proveedores de almacén de mensajes que no admiten texto RTF necesitan eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) cuando la propiedad **PR_BODY** cambia para que interopere correctamente con las aplicaciones cliente que admiten texto RTF .</span><span class="sxs-lookup"><span data-stu-id="508b0-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="508b0-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="508b0-113">See also</span></span>



[<span data-ttu-id="508b0-114">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="508b0-114">Message Store Features</span></span>](message-store-features.md)

