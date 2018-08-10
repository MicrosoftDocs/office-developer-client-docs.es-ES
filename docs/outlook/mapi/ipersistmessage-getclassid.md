---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817863"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="d78b7-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="d78b7-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="d78b7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d78b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d78b7-105">Devuelve un identificador que representa el servidor de formulario que puede administrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="d78b7-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="d78b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d78b7-106">Parameters</span></span>

 <span data-ttu-id="d78b7-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="d78b7-107">_lpClassID_</span></span>
  
> <span data-ttu-id="d78b7-108">[entrada, salida] Un puntero para el identificador de clase (CLSID) del formulario.</span><span class="sxs-lookup"><span data-stu-id="d78b7-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d78b7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d78b7-109">Return value</span></span>

<span data-ttu-id="d78b7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d78b7-110">S_OK</span></span> 
  
> <span data-ttu-id="d78b7-111">El identificador de clase se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d78b7-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d78b7-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d78b7-112">Remarks</span></span>

<span data-ttu-id="d78b7-113">El método **IPersistMessge::GetClassID** establece el contenido del parámetro _lpClassID_ al identificador de clase del servidor de formulario y devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="d78b7-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="d78b7-114">Cuando llama a un visor de formulario **GetClassID** y devuelve correctamente, el formulario se coloca en el estado de [Uninitialized](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="d78b7-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="d78b7-115">Para obtener más información acerca de cómo se usan los identificadores de clase con objetos de almacenamiento estructurado, consulte la documentación para el método [IPersist:: GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d78b7-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d78b7-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d78b7-116">See also</span></span>



[<span data-ttu-id="d78b7-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d78b7-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
