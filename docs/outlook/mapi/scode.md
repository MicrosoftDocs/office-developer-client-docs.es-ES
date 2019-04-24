---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351243"
---
# <a name="scode"></a><span data-ttu-id="e4e68-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="e4e68-103">SCODE</span></span>

<span data-ttu-id="e4e68-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4e68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4e68-105">Un valor de estado de 32 bits que se usa para describir un error o una advertencia.</span><span class="sxs-lookup"><span data-stu-id="e4e68-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="e4e68-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4e68-106">Remarks</span></span>

<span data-ttu-id="e4e68-107">El tipo de datos **SCODE** es el mismo que el tipo de datos [HRESULT](hresult.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e68-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="e4e68-108">Un valor **SCODE** se divide en cuatro campos:</span><span class="sxs-lookup"><span data-stu-id="e4e68-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="e4e68-109">Un código de gravedad de un solo bit que se establece en 0 para indicar correcto y 1 para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="e4e68-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="e4e68-110">Un campo reservado de 11 bits</span><span class="sxs-lookup"><span data-stu-id="e4e68-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="e4e68-111">Un código de instalación de 4 bits que indica el área responsable del error o advertencia.</span><span class="sxs-lookup"><span data-stu-id="e4e68-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="e4e68-112">Un código de advertencia o error de 16 bits que describe el problema que está causando el error o la advertencia.</span><span class="sxs-lookup"><span data-stu-id="e4e68-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="e4e68-113">Muchas de las funciones y métodos de MAPI devuelven los valores de **SCODE** definidos como tipos de datos **HRESULT** como los métodos y funciones OLE.</span><span class="sxs-lookup"><span data-stu-id="e4e68-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="e4e68-114">OLE define varias macros que se pueden usar para realizar la conversión entre **SCODE** y **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e4e68-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e4e68-115">En MAPI de 64 bits, **SCODE** sigue siendo un valor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4e68-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="e4e68-116">Para obtener más información acerca de cómo MAPI usa el tipo de datos **SCODE** , consulte [control de errores](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e4e68-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="e4e68-117">Para obtener más información acerca de OLE y el tipo de datos **SCODE** , vea la *Referencia del programador de OLE* .</span><span class="sxs-lookup"><span data-stu-id="e4e68-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4e68-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4e68-118">See also</span></span>



<span data-ttu-id="e4e68-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="e4e68-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="e4e68-120">Tipos de datos MAPI</span><span class="sxs-lookup"><span data-stu-id="e4e68-120">MAPI Data Types</span></span>](mapi-data-types.md)

