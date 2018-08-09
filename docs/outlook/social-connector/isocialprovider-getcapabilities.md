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
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821106"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="9f5d5-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="9f5d5-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="9f5d5-104">Obtiene una cadena que describe las capacidades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9f5d5-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="9f5d5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f5d5-105">Parameters</span></span>

<span data-ttu-id="9f5d5-106">_resultado_</span><span class="sxs-lookup"><span data-stu-id="9f5d5-106">_result_</span></span>
  
> <span data-ttu-id="9f5d5-107">[out] Una cadena XML que representa las funciones de un proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="9f5d5-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f5d5-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f5d5-108">Remarks</span></span>

<span data-ttu-id="9f5d5-109">La cadena XML devuelto _resultados_ debe cumplir con la definición del esquema para el elemento **capabilities** , tal como se define en el esquema XML de extensibilidad de proveedores OSC.</span><span class="sxs-lookup"><span data-stu-id="9f5d5-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="9f5d5-110">El proveedor debe devolver una cadena de _resultado_ para habilitar las llamadas subsiguientes desde el OSC para el proveedor funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="9f5d5-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f5d5-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f5d5-111">See also</span></span>

- [<span data-ttu-id="9f5d5-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f5d5-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

