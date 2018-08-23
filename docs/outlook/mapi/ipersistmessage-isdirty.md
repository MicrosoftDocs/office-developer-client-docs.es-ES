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
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576207"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="3543f-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="3543f-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="3543f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3543f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3543f-105">Comprueba el formulario para que los cambios realizados desde la última vez que guardó.</span><span class="sxs-lookup"><span data-stu-id="3543f-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="3543f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3543f-106">Parameters</span></span>

<span data-ttu-id="3543f-107">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3543f-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3543f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3543f-108">Return value</span></span>

<span data-ttu-id="3543f-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3543f-109">S_OK</span></span> 
  
> <span data-ttu-id="3543f-110">El formulario tiene los cambios realizados desde la última vez que se guardó.</span><span class="sxs-lookup"><span data-stu-id="3543f-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="3543f-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3543f-111">S_FALSE</span></span> 
  
> <span data-ttu-id="3543f-112">El formulario no tiene los cambios realizados desde la última vez que se guardó.</span><span class="sxs-lookup"><span data-stu-id="3543f-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3543f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3543f-113">Remarks</span></span>

<span data-ttu-id="3543f-114">Visores de formulario llamar al método **IPersistMessage::IsDirty** para determinar si el mensaje se han guardado los datos.</span><span class="sxs-lookup"><span data-stu-id="3543f-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3543f-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3543f-115">See also</span></span>



[<span data-ttu-id="3543f-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3543f-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

