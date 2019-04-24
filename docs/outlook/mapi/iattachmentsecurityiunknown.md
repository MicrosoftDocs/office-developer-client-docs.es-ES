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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326988"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="22251-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22251-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="22251-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22251-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22251-105">Permite que las soluciones de Microsoft Outlook 2010 y Microsoft Outlook 2013 descubran si los datos adjuntos se consideran no seguros y bloqueados para la visualización y la indización.</span><span class="sxs-lookup"><span data-stu-id="22251-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22251-106">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="22251-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="22251-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="22251-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="22251-108">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="22251-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="22251-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="22251-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="22251-110">Comprueba si los datos adjuntos especificados están bloqueados por Outlook 2010 o Outlook 2013 para su visualización e indización.</span><span class="sxs-lookup"><span data-stu-id="22251-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22251-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22251-111">Remarks</span></span>

<span data-ttu-id="22251-112">Las soluciones de Outlook 2010 y Outlook 2013 pueden consultar esta interfaz para ver si hay datos adjuntos bloqueados.</span><span class="sxs-lookup"><span data-stu-id="22251-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="22251-113">Los datos adjuntos bloqueados por Outlook 2010 o Outlook 2013 varían en función de cómo se haya configurado Outlook 2010 o Outlook 2013 y de las directivas que haya aplicado un administrador.</span><span class="sxs-lookup"><span data-stu-id="22251-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="22251-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="22251-114">See also</span></span>



[<span data-ttu-id="22251-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="22251-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="22251-116">Comprobar que los datos adJuntos están bloqueados</span><span class="sxs-lookup"><span data-stu-id="22251-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

