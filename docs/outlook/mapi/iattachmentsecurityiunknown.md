---
title: IUnknown IAttachmentSecurity
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
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411417"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="79fc3-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79fc3-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="79fc3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79fc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79fc3-105">Permite que las soluciones de Microsoft Outlook 2010 y Microsoft Outlook 2013 descubran si los datos adjuntos se consideran no seguros y bloqueados para la visualización y la indización.</span><span class="sxs-lookup"><span data-stu-id="79fc3-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79fc3-106">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="79fc3-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="79fc3-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="79fc3-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="79fc3-108">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="79fc3-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="79fc3-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="79fc3-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="79fc3-110">Comprueba si los datos adjuntos especificados están bloqueados por Outlook 2010 o Outlook 2013 para su visualización e indización.</span><span class="sxs-lookup"><span data-stu-id="79fc3-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79fc3-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79fc3-111">Remarks</span></span>

<span data-ttu-id="79fc3-112">Las soluciones de Outlook 2010 y Outlook 2013 pueden consultar esta interfaz para ver si hay datos adjuntos bloqueados.</span><span class="sxs-lookup"><span data-stu-id="79fc3-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="79fc3-113">Los datos adjuntos bloqueados por Outlook 2010 o Outlook 2013 varían en función de cómo se haya configurado Outlook 2010 o Outlook 2013 y de las directivas que haya aplicado un administrador.</span><span class="sxs-lookup"><span data-stu-id="79fc3-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79fc3-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="79fc3-114">See also</span></span>



[<span data-ttu-id="79fc3-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="79fc3-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="79fc3-116">Comprobar que los datos adJuntos están bloqueados</span><span class="sxs-lookup"><span data-stu-id="79fc3-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

