---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419992"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="98622-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="98622-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="98622-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98622-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98622-105">Realiza cambios permanentes en una sección de perfil de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="98622-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="98622-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98622-106">Parameters</span></span>

 <span data-ttu-id="98622-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98622-107">_ulFlags_</span></span>
  
> <span data-ttu-id="98622-108">[entrada] Máscara de bits de marcas que indica el tipo de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="98622-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="98622-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="98622-109">The following flag can be set:</span></span>
    
<span data-ttu-id="98622-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="98622-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="98622-111">El almacén de mensajes es temporal y no debe agregarse a la tabla del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="98622-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="98622-112">Cuando MDB_TEMPORARY se establece, **ModifyProfile** devuelve S_OK inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="98622-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98622-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98622-113">Return value</span></span>

<span data-ttu-id="98622-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="98622-114">S_OK</span></span> 
  
> <span data-ttu-id="98622-115">Los cambios realizados en la sección de perfil se realizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="98622-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98622-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98622-116">Remarks</span></span>

<span data-ttu-id="98622-117">El **método IMAPISupport::ModifyProfile** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="98622-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="98622-118">Los proveedores del almacén de mensajes **llaman a ModifyProfile** para solicitar a MAPI que modifique su información de perfil.</span><span class="sxs-lookup"><span data-stu-id="98622-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="98622-119">**ModifyProfile** agrega la sección de perfil asociada con el proveedor de llamadas a la lista de recursos del proveedor de almacenamiento de mensajes instalados.</span><span class="sxs-lookup"><span data-stu-id="98622-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="98622-120">Esto hace que el almacén de mensajes aparezca en la tabla del almacén de mensajes, que está disponible para los clientes a través del método [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) y se abre sin mostrar un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="98622-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="98622-121">Si se MDB_TEMPORARY marca, MAPI no hace nada y el método vuelve inmediatamente con S_OK.</span><span class="sxs-lookup"><span data-stu-id="98622-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98622-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98622-122">See also</span></span>



[<span data-ttu-id="98622-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="98622-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="98622-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="98622-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

