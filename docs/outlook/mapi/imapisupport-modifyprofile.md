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
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817504"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="8254c-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="8254c-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="8254c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8254c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8254c-105">Hace que los cambios realizados en un mensaje de almacenar permanente de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="8254c-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8254c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8254c-106">Parameters</span></span>

 <span data-ttu-id="8254c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8254c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8254c-108">[entrada] Almacenar una máscara de bits de marcadores que indica el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8254c-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="8254c-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="8254c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8254c-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="8254c-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="8254c-111">El almacén de mensajes es temporal y no debe agregarse a la tabla de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8254c-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="8254c-112">Cuando se establece MDB_TEMPORARY, **ModifyProfile** devuelve S_OK inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8254c-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8254c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8254c-113">Return value</span></span>

<span data-ttu-id="8254c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8254c-114">S_OK</span></span> 
  
> <span data-ttu-id="8254c-115">Los cambios realizados en la sección de perfil se realizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="8254c-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8254c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8254c-116">Remarks</span></span>

<span data-ttu-id="8254c-117">El método **IMAPISupport::ModifyProfile** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8254c-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8254c-118">Mensaje de llamada de los proveedores de almacén de **ModifyProfile** para solicitar MAPI para modificar la información de su perfil.</span><span class="sxs-lookup"><span data-stu-id="8254c-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="8254c-119">**ModifyProfile** agrega la sección de perfil que está asociada con el proveedor de llamada a la lista de recursos de proveedor de almacén de mensaje instalados.</span><span class="sxs-lookup"><span data-stu-id="8254c-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="8254c-120">Esto hace que el almacén de mensajes que se mostrarán en la tabla de almacén de mensajes, que está disponible para los clientes a través del método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) y que se abra sin la presentación de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8254c-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="8254c-121">Si se establece la marca MDB_TEMPORARY, MAPI no realiza ninguna acción y el método devuelve inmediatamente con S_OK.</span><span class="sxs-lookup"><span data-stu-id="8254c-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8254c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8254c-122">See also</span></span>



[<span data-ttu-id="8254c-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="8254c-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="8254c-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8254c-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

