---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407574"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="8b336-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="8b336-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="8b336-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b336-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b336-105">Comprueba el formulario en busca de cambios realizados desde la última vez que guardó.</span><span class="sxs-lookup"><span data-stu-id="8b336-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="8b336-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b336-106">Parameters</span></span>

<span data-ttu-id="8b336-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8b336-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="8b336-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b336-108">Return value</span></span>

<span data-ttu-id="8b336-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b336-109">S_OK</span></span> 
  
> <span data-ttu-id="8b336-110">El formulario tiene cambios realizados desde la última vez que se guardó.</span><span class="sxs-lookup"><span data-stu-id="8b336-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="8b336-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="8b336-111">S_FALSE</span></span> 
  
> <span data-ttu-id="8b336-112">El formulario no tiene cambios realizados desde la última vez que se guardó.</span><span class="sxs-lookup"><span data-stu-id="8b336-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b336-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b336-113">Remarks</span></span>

<span data-ttu-id="8b336-114">Los visores de formularios llaman al método **IPersistMessage:: IsDirty** para determinar si el mensaje tiene datos sin guardar.</span><span class="sxs-lookup"><span data-stu-id="8b336-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b336-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="8b336-115">See also</span></span>



[<span data-ttu-id="8b336-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b336-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

