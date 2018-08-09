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
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817874"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="46ec0-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="46ec0-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="46ec0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46ec0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46ec0-105">Comprueba el formulario para que los cambios realizados desde la última vez que guardó.</span><span class="sxs-lookup"><span data-stu-id="46ec0-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="46ec0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46ec0-106">Parameters</span></span>

<span data-ttu-id="46ec0-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="46ec0-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="46ec0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46ec0-108">Return value</span></span>

<span data-ttu-id="46ec0-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="46ec0-109">S_OK</span></span> 
  
> <span data-ttu-id="46ec0-110">El formulario tiene los cambios realizados desde la última vez que se guardó.</span><span class="sxs-lookup"><span data-stu-id="46ec0-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="46ec0-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="46ec0-111">S_FALSE</span></span> 
  
> <span data-ttu-id="46ec0-112">El formulario no tiene los cambios realizados desde la última vez que se guardó.</span><span class="sxs-lookup"><span data-stu-id="46ec0-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46ec0-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46ec0-113">Remarks</span></span>

<span data-ttu-id="46ec0-114">Visores de formulario llamar al método **IPersistMessage::IsDirty** para determinar si el mensaje se han guardado los datos.</span><span class="sxs-lookup"><span data-stu-id="46ec0-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46ec0-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="46ec0-115">See also</span></span>



[<span data-ttu-id="46ec0-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46ec0-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

