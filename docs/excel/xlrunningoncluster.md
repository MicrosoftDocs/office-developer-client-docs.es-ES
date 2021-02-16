---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418291"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="d1e60-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="d1e60-104">xlRunningOnCluster</span></span>

<span data-ttu-id="d1e60-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d1e60-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d1e60-106">Devuelve un valor que indica si la función definida por el usuario se ejecuta en un clúster.</span><span class="sxs-lookup"><span data-stu-id="d1e60-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="d1e60-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1e60-107">Parameters</span></span>

<span data-ttu-id="d1e60-108">Esta función no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="d1e60-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d1e60-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1e60-109">Return value</span></span>

<span data-ttu-id="d1e60-110">Si la función se ejecuta en un proceso de Excel, devuelve 0 en un **XLOPER12** de tipo **xlTypeInt**.</span><span class="sxs-lookup"><span data-stu-id="d1e60-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="d1e60-111">Si la función se ejecuta en un clúster, el tipo y el valor devueltos los determina el proveedor del conector de clúster.</span><span class="sxs-lookup"><span data-stu-id="d1e60-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="d1e60-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1e60-112">Requirements</span></span>

<span data-ttu-id="d1e60-113">Esta función se define en el archivo de encabezado Xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="d1e60-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1e60-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d1e60-114">See also</span></span>

- [<span data-ttu-id="d1e60-115">Funciones seguras para clústeres</span><span class="sxs-lookup"><span data-stu-id="d1e60-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="d1e60-116">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="d1e60-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

