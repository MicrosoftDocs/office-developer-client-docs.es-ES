---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtiene una cadena que describe las funciones del proveedor.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285768"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="9a87f-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="9a87f-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="9a87f-104">Obtiene una cadena que describe las funciones del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9a87f-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="9a87f-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a87f-105">Parameters</span></span>

<span data-ttu-id="9a87f-106">_result_</span><span class="sxs-lookup"><span data-stu-id="9a87f-106">_result_</span></span>
  
> <span data-ttu-id="9a87f-107">contempla Cadena XML que representa las funciones de un proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="9a87f-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a87f-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a87f-108">Remarks</span></span>

<span data-ttu-id="9a87f-109">La cadena XML de _resultado_ devuelta debe cumplir con la definición de esquema del elemento **Capabilities** , tal como se define en el esquema XML de la extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="9a87f-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="9a87f-110">El proveedor debe devolver una cadena de _resultado_ para permitir llamadas posteriores desde el OSC al proveedor para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="9a87f-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a87f-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a87f-111">See also</span></span>

- [<span data-ttu-id="9a87f-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a87f-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

