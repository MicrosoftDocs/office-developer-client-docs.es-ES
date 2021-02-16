---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtiene una cadena que describe las capacidades del proveedor.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408106"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="d33b1-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d33b1-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="d33b1-104">Obtiene una cadena que describe las capacidades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d33b1-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="d33b1-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d33b1-105">Parameters</span></span>

<span data-ttu-id="d33b1-106">_result_</span><span class="sxs-lookup"><span data-stu-id="d33b1-106">_result_</span></span>
  
> <span data-ttu-id="d33b1-107">[salida] Cadena XML que representa las capacidades de un proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="d33b1-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d33b1-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d33b1-108">Remarks</span></span>

<span data-ttu-id="d33b1-109">La  _cadena_ XML de resultado devuelta debe cumplir con la definición de esquema para el elemento **capabilities,** tal como se define en el esquema XML para la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="d33b1-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="d33b1-110">El proveedor debe devolver una cadena  _de_ resultados para permitir que las llamadas posteriores desde el OSC al proveedor funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="d33b1-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d33b1-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="d33b1-111">See also</span></span>

- [<span data-ttu-id="d33b1-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d33b1-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

