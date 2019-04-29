---
title: HRESULT
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
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435022"
---
# <a name="hresult"></a><span data-ttu-id="74bfa-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="74bfa-103">HRESULT</span></span>

  
  
<span data-ttu-id="74bfa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74bfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74bfa-105">Un valor de 32 bits que se usa para describir un error o una advertencia.</span><span class="sxs-lookup"><span data-stu-id="74bfa-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="74bfa-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74bfa-106">Remarks</span></span>

<span data-ttu-id="74bfa-107">El tipo de datos **HRESULT** es el mismo que el tipo de datos [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="74bfa-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="74bfa-108">Un valor **HRESULT** consta de los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="74bfa-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="74bfa-109">Un código de 1 bit que indica la gravedad, donde cero representa el éxito y 1 representa un error.</span><span class="sxs-lookup"><span data-stu-id="74bfa-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="74bfa-110">Un valor reservado de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="74bfa-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="74bfa-111">Un código de 11 bits que indica la responsabilidad del error o advertencia, también conocido como código de servicio.</span><span class="sxs-lookup"><span data-stu-id="74bfa-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="74bfa-112">Un código de 16 bits que describe el error o la advertencia.</span><span class="sxs-lookup"><span data-stu-id="74bfa-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="74bfa-113">La mayoría de los métodos y funciones de la interfaz MAPI devuelven valores **HRESULT** para proporcionar una formación de causa detallada.</span><span class="sxs-lookup"><span data-stu-id="74bfa-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="74bfa-114">Los valores **HRESULT** también se usan ampliamente en los métodos de interfaz OLE.</span><span class="sxs-lookup"><span data-stu-id="74bfa-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="74bfa-115">OLE proporciona varias macros para convertir entre valores **HRESULT** y valores **SCODE** , otro tipo de datos comunes para el tratamiento de errores.</span><span class="sxs-lookup"><span data-stu-id="74bfa-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="74bfa-116">En MAPI de 64 bits, **HRESULT** sigue siendo un valor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="74bfa-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="74bfa-117">Para obtener información sobre el uso OLE de valores **HRESULT** , vea la *Referencia del programador de OLE* .</span><span class="sxs-lookup"><span data-stu-id="74bfa-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="74bfa-118">Para obtener más información acerca del uso de estos valores en MAPI, vea [control de errores](error-handling-in-mapi.md) y cualquiera de los siguientes métodos de interfaz:</span><span class="sxs-lookup"><span data-stu-id="74bfa-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="74bfa-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74bfa-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="74bfa-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74bfa-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="74bfa-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74bfa-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="74bfa-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74bfa-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="74bfa-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74bfa-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="74bfa-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="74bfa-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="74bfa-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="74bfa-125">See also</span></span>



[<span data-ttu-id="74bfa-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="74bfa-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="74bfa-127">Tipos de datos MAPI</span><span class="sxs-lookup"><span data-stu-id="74bfa-127">MAPI Data Types</span></span>](mapi-data-types.md)

