---
title: Sincronizar texto y formato
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 40d7a45ab97e0d2f8e9d3db1e1d38eb3bdb75158
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820841"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="18615-103">Sincronizar texto y formato</span><span class="sxs-lookup"><span data-stu-id="18615-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="18615-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18615-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18615-105">El desafío principal en el envío de mensajes de formato de texto enriquecido (RTF) es mantener el texto sincronizado con el formato.</span><span class="sxs-lookup"><span data-stu-id="18615-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="18615-106">Para asegurarse de que, cuando los mensajes llegan a su destino se hayan definido como sus creadores pensados y que el formato de texto y se sincronizan, MAPI proporciona la función [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="18615-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="18615-107">**RTFSync** normalmente se llama por los clientes de tener en cuenta RTF antes de mostrar los mensajes entrantes y por la cola MAPI cuando descarga los mensajes a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="18615-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="18615-108">Los autores de llamadas especifican el área de discrepancia posible pasando uno o dos indicadores a **RTFSync**:</span><span class="sxs-lookup"><span data-stu-id="18615-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="18615-109">RTF_SYNC_BODY_CHANGED para indicar una modificación en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="18615-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="18615-110">RTF_SYNC_RTF_CHANGED para indicar una modificación en el formato de mensaje.</span><span class="sxs-lookup"><span data-stu-id="18615-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="18615-111">El proceso de sincronización que se produce en **RTFSync** es una comprobación sofisticada redundancia cíclica (CRC) del texto del mensaje que se pasa por alto algunos caracteres y convierte a otras personas.</span><span class="sxs-lookup"><span data-stu-id="18615-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="18615-112">Se omiten los caracteres que se agregaron más probable es que por los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="18615-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="18615-113">MAPI define varias propiedades para trabajar con formato RTF, tal como se describe en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="18615-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="18615-114">**Propiedad RTF**</span><span class="sxs-lookup"><span data-stu-id="18615-114">**RTF property**</span></span>|<span data-ttu-id="18615-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18615-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18615-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18615-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="18615-117">Indica el principio del texto del mensaje real.</span><span class="sxs-lookup"><span data-stu-id="18615-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="18615-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18615-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="18615-119">Contiene el resultado de la comprobación de redundancia cíclica del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="18615-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="18615-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18615-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="18615-121">Contiene el número de caracteres en **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="18615-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="18615-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18615-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="18615-123">Establecer en TRUE cuando el mensaje de formato de texto y se hayan sincronizado.</span><span class="sxs-lookup"><span data-stu-id="18615-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="18615-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18615-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="18615-125">Contiene el número de caracteres nonwhitespace que incluya el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="18615-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="18615-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18615-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="18615-127">Contiene el número de caracteres nonwhitespace que finalizan el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="18615-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

