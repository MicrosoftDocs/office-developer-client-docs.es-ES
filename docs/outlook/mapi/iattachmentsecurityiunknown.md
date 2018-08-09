---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817145"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="3258c-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3258c-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="3258c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3258c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3258c-105">Permite que las soluciones de Microsoft Outlook 2010 y Microsoft Outlook 2013 averiguar si se considera como datos adjuntos no seguros y bloqueados para su visualización e indización.</span><span class="sxs-lookup"><span data-stu-id="3258c-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3258c-106">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="3258c-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3258c-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="3258c-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3258c-108">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="3258c-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3258c-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="3258c-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="3258c-110">Comprueba si los datos adjuntos especificados está bloqueado por Outlook 2010 o Outlook 2013 para su visualización e indización.</span><span class="sxs-lookup"><span data-stu-id="3258c-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3258c-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3258c-111">Remarks</span></span>

<span data-ttu-id="3258c-112">Soluciones de Outlook 2010 y Outlook 2013 pueden consultar esta interfaz para ver si se bloquea un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="3258c-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="3258c-113">Los datos adjuntos que están bloqueados por Outlook 2010 o Outlook 2013 varían dependiendo de cómo se haya configurado Outlook 2010 o Outlook 2013 y las directivas que se ha aplicado un administrador.</span><span class="sxs-lookup"><span data-stu-id="3258c-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3258c-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="3258c-114">See also</span></span>



[<span data-ttu-id="3258c-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3258c-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3258c-116">Comprobar si los datos adjuntos están bloqueados</span><span class="sxs-lookup"><span data-stu-id="3258c-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

