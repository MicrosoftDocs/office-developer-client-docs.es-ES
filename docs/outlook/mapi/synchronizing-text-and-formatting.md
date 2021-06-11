---
title: Sincronización de texto y formato
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435106"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="23c2b-103">Sincronización de texto y formato</span><span class="sxs-lookup"><span data-stu-id="23c2b-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="23c2b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23c2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23c2b-105">El principal desafío al enviar mensajes de formato de texto enriquecido (RTF) es mantener el texto sincronizado con el formato.</span><span class="sxs-lookup"><span data-stu-id="23c2b-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="23c2b-106">Para asegurarse de que cuando los mensajes llegan a su destino son como sus originores están diseñados y que el texto y el formato están sincronizados, MAPI proporciona la [función RTFSync.](rtfsync.md)</span><span class="sxs-lookup"><span data-stu-id="23c2b-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="23c2b-107">**RtfSync** suele ser llamado por los clientes con rtf antes de mostrar los mensajes entrantes y por la cola MAPI cuando descarga mensajes a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="23c2b-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="23c2b-108">Los autores de llamadas especifican el área de posible discrepancia pasando una o dos marcas a **RTFSync:**</span><span class="sxs-lookup"><span data-stu-id="23c2b-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="23c2b-109">RTF_SYNC_BODY_CHANGED para indicar una modificación en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23c2b-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="23c2b-110">RTF_SYNC_RTF_CHANGED para indicar una modificación en el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23c2b-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="23c2b-111">El proceso de sincronización que se produce en **RTFSync** es una comprobación de redundancia cíclica sofisticada (CRC) del texto del mensaje que omite algunos caracteres y convierte otros.</span><span class="sxs-lookup"><span data-stu-id="23c2b-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="23c2b-112">Se omiten los caracteres que probablemente agregaron los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="23c2b-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="23c2b-113">MAPI define varias propiedades para trabajar con RTF, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="23c2b-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="23c2b-114">**Rtf (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="23c2b-114">**RTF property**</span></span>|<span data-ttu-id="23c2b-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23c2b-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23c2b-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23c2b-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23c2b-117">Indica el principio del texto del mensaje real.</span><span class="sxs-lookup"><span data-stu-id="23c2b-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="23c2b-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23c2b-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23c2b-119">Contiene el resultado de la comprobación de redundancia cíclica del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23c2b-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="23c2b-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23c2b-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23c2b-121">Contiene el número de caracteres de **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="23c2b-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="23c2b-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23c2b-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23c2b-123">Se establece en TRUE cuando se han sincronizado el texto y el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23c2b-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="23c2b-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23c2b-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23c2b-125">Contiene el número de caracteres nowhitespace que preceieron el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23c2b-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="23c2b-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23c2b-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23c2b-127">Contiene el número de caracteres que no sonwhitespace que arrastran el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23c2b-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

