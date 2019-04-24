---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301634"
---
# <a name="opensession"></a><span data-ttu-id="33afc-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="33afc-103">OpenSession</span></span>

<span data-ttu-id="33afc-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="33afc-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="33afc-105">Crea una sesión en la que se pueden ejecutar funciones definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="33afc-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="33afc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="33afc-106">Parameters</span></span>

<span data-ttu-id="33afc-107">_Params_</span><span class="sxs-lookup"><span data-stu-id="33afc-107">_Params_</span></span>
  
> <span data-ttu-id="33afc-108">Puntero a una cadena uniCODE delimitada por punto y coma de los parámetros de la sesión.</span><span class="sxs-lookup"><span data-stu-id="33afc-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="33afc-109">Excel no utiliza este argumento.</span><span class="sxs-lookup"><span data-stu-id="33afc-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33afc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33afc-110">Return value</span></span>

<span data-ttu-id="33afc-111">Un identificador de sesión que se va a usar en otras llamadas al conector de clúster, si la sesión se ha creado correctamente; de lo contrario **xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="33afc-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33afc-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="33afc-112">See also</span></span>

- [<span data-ttu-id="33afc-113">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="33afc-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

