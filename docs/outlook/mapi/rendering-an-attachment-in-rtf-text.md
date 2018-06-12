---
title: Representación de un dato adjunto en texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cf22e360a0319a662c9b7dd31856dbb6eccec02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820496"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="0a269-103">Representación de un dato adjunto en texto RTF</span><span class="sxs-lookup"><span data-stu-id="0a269-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="0a269-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a269-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a269-105">Formato de texto de Rich (RTF)-tener en cuenta los clientes pueden recuperar información de posición de representación de texto del mensaje RTF mediante busca la siguiente secuencia de escape en la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="0a269-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="0a269-106">**Para buscar información de representación en texto con formato**</span><span class="sxs-lookup"><span data-stu-id="0a269-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="0a269-107">Llame a **IMessage::GetAttachmentTable** para obtener acceso a la tabla de datos adjuntos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0a269-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="0a269-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="0a269-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="0a269-109">Crear una restricción de propiedad que limita la tabla a las filas que tienen **PR_RENDERING_POSITION** no es igual a -1.</span><span class="sxs-lookup"><span data-stu-id="0a269-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="0a269-110">Para obtener más información, vea **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0a269-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="0a269-111">Llamar a **IMAPITable:: Restrict** para aplicar la restricción.</span><span class="sxs-lookup"><span data-stu-id="0a269-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="0a269-112">Para obtener más información, vea [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="0a269-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="0a269-113">Llamar a **SortTable** para ordenar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0a269-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="0a269-114">Para obtener más información, vea [SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="0a269-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="0a269-115">Llamar a **IMAPITable:: QueryRows** para recuperar las filas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="0a269-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="0a269-116">Para obtener más información, vea [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="0a269-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="0a269-117">Llamar al método **IMAPIProp::OpenProperty** del mensaje para recuperar **PR_RTF_COMPRESSED** con la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0a269-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="0a269-118">Para obtener más información, vea [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="0a269-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="0a269-119">Examinar la secuencia, busca el marcador de posición de representación, `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="0a269-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="0a269-120">El carácter que sigue a este marcador de posición es el lugar para los datos adjuntos siguiente de la tabla ordenada.</span><span class="sxs-lookup"><span data-stu-id="0a269-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

