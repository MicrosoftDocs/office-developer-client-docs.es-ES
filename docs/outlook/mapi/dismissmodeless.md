---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428189"
---
# <a name="dismissmodeless"></a><span data-ttu-id="49ede-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="49ede-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="49ede-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49ede-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49ede-105">Define una función de devolución de llamada que llama a MAPI cuando ha desechado un cuadro de diálogo de la libreta de direcciones sin modo.</span><span class="sxs-lookup"><span data-stu-id="49ede-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49ede-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="49ede-106">Header file:</span></span>  <br/> |<span data-ttu-id="49ede-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="49ede-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="49ede-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="49ede-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="49ede-109">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="49ede-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="49ede-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="49ede-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="49ede-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="49ede-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="49ede-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="49ede-112">Parameters</span></span>

 <span data-ttu-id="49ede-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="49ede-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="49ede-114">a Valor específico de la implementación que se suele usar para pasar información de la interfaz de usuario a una función.</span><span class="sxs-lookup"><span data-stu-id="49ede-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="49ede-115">Por ejemplo, en Microsoft Windows este parámetro es el identificador de la ventana principal del cuadro de diálogo y es del tipo HWND, convertido a **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="49ede-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="49ede-116">Un valor de cero indica que no hay ventana principal.</span><span class="sxs-lookup"><span data-stu-id="49ede-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="49ede-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="49ede-117">_lpvContext_</span></span>
  
> <span data-ttu-id="49ede-118">a Puntero a un valor arbitrario que se pasa a la función de devolución de llamada cuando MAPI la llama.</span><span class="sxs-lookup"><span data-stu-id="49ede-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="49ede-119">Este valor puede representar una dirección de importancia para la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="49ede-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="49ede-120">Normalmente, en el código de C++, _lpvContext_ es un puntero a la dirección de una instancia de objeto de c++.</span><span class="sxs-lookup"><span data-stu-id="49ede-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="49ede-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49ede-121">Return value</span></span>

<span data-ttu-id="49ede-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="49ede-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49ede-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49ede-123">Remarks</span></span>

<span data-ttu-id="49ede-124">Cuando la aplicación cliente invoca un cuadro de diálogo de la libreta de direcciones sin modo, incluye en su bucle de mensajes de Windows una llamada a una función basada en el prototipo [ACCELERATEABSDI](accelerateabsdi.md) , que comprueba y procesa las teclas de aceleración.</span><span class="sxs-lookup"><span data-stu-id="49ede-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="49ede-125">Cuando se cierra el cuadro de diálogo, MAPI llama a la función basada en **DISMISSMODELESS** para que la aplicación cliente deje de llamar a la función basada en **ACCELERATEABSDI** .</span><span class="sxs-lookup"><span data-stu-id="49ede-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49ede-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="49ede-126">See also</span></span>



[<span data-ttu-id="49ede-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="49ede-127">ADRPARM</span></span>](adrparm.md)

