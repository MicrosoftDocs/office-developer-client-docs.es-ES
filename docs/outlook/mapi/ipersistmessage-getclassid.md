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
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309628"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="e9b23-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="e9b23-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="e9b23-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9b23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9b23-105">Devuelve un identificador que representa el servidor de formularios que puede administrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="e9b23-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="e9b23-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e9b23-106">Parameters</span></span>

 <span data-ttu-id="e9b23-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="e9b23-107">_lpClassID_</span></span>
  
> <span data-ttu-id="e9b23-108">[in, out] Un puntero al identificador de clase (CLSID) del formulario.</span><span class="sxs-lookup"><span data-stu-id="e9b23-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9b23-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9b23-109">Return value</span></span>

<span data-ttu-id="e9b23-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9b23-110">S_OK</span></span> 
  
> <span data-ttu-id="e9b23-111">El identificador de clase se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="e9b23-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9b23-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9b23-112">Remarks</span></span>

<span data-ttu-id="e9b23-113">El método **IPersistMessge:: GetClassID** establece el contenido del parámetro _lpClassID_ en el identificador de clase del servidor de formularios y Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="e9b23-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="e9b23-114">Cuando un visor de formularios llama a **GetClassID** y vuelve correctamente, el formulario se coloca en el estado sin [inicializar](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="e9b23-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="e9b23-115">Para obtener más información acerca de cómo se usan los identificadores de clase con objetos de almacenamiento estructurados, vea la documentación del método [IPersist:: GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e9b23-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9b23-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9b23-116">See also</span></span>



[<span data-ttu-id="e9b23-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9b23-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

