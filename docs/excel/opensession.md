---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815692"
---
# <a name="opensession"></a><span data-ttu-id="e7df8-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="e7df8-103">OpenSession</span></span>

<span data-ttu-id="e7df8-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e7df8-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e7df8-105">Crea una sesión en el que se pueden ejecutar funciones definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e7df8-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="e7df8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7df8-106">Parameters</span></span>

<span data-ttu-id="e7df8-107">_Params_</span><span class="sxs-lookup"><span data-stu-id="e7df8-107">_Params_</span></span>
  
> <span data-ttu-id="e7df8-108">Un puntero a la cadena UNICODE delimitada por punto y coma de los parámetros de la sesión.</span><span class="sxs-lookup"><span data-stu-id="e7df8-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="e7df8-109">Excel no utiliza este argumento.</span><span class="sxs-lookup"><span data-stu-id="e7df8-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7df8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7df8-110">Return value</span></span>

<span data-ttu-id="e7df8-111">Un identificador de sesión para usar en otras llamadas para el conector de clúster, si la sesión se ha creado correctamente; en caso contrario, **xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="e7df8-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7df8-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7df8-112">See also</span></span>

- [<span data-ttu-id="e7df8-113">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="e7df8-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

