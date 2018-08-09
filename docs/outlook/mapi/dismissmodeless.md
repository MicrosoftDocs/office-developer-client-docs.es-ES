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
ms.openlocfilehash: dc830665f425b747d2fdb05641dc037a2e84f695
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816695"
---
# <a name="dismissmodeless"></a><span data-ttu-id="3268f-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="3268f-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="3268f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3268f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3268f-105">Define una función de devolución de llamada que llama MAPI cuando ha descartado un cuadro de diálogo de la libreta de direcciones no modal.</span><span class="sxs-lookup"><span data-stu-id="3268f-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3268f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3268f-106">Header file:</span></span>  <br/> |<span data-ttu-id="3268f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3268f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3268f-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="3268f-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="3268f-109">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="3268f-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="3268f-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="3268f-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="3268f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="3268f-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="3268f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3268f-112">Parameters</span></span>

 <span data-ttu-id="3268f-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3268f-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="3268f-114">[entrada] Un valor específico de la implementación suele utilizado para pasar información de interfaz de usuario a una función.</span><span class="sxs-lookup"><span data-stu-id="3268f-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="3268f-115">Por ejemplo, en Microsoft Windows en este parámetro es el identificador de ventana primario para el cuadro de diálogo y es de tipo HWND, que se convierte en un **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="3268f-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="3268f-116">Un valor de cero indica que no hay ninguna ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="3268f-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="3268f-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="3268f-117">_lpvContext_</span></span>
  
> <span data-ttu-id="3268f-118">[entrada] Puntero a un valor arbitrario se pasa a la función de devolución de llamada cuando llama a MAPI.</span><span class="sxs-lookup"><span data-stu-id="3268f-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="3268f-119">Este valor puede representar una dirección de importancia a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3268f-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="3268f-120">Normalmente, para el código de C++, _lpvContext_ es un puntero a la dirección de una instancia de objeto de C++.</span><span class="sxs-lookup"><span data-stu-id="3268f-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3268f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3268f-121">Return value</span></span>

<span data-ttu-id="3268f-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3268f-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3268f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3268f-123">Remarks</span></span>

<span data-ttu-id="3268f-124">Cuando la aplicación cliente invoca un cuadro de diálogo de la libreta de direcciones no modal, en el bucle de mensajes de Windows incluye una llamada a una función según el prototipo [ACCELERATEABSDI](accelerateabsdi.md) , que busca y procesa las teclas de aceleración.</span><span class="sxs-lookup"><span data-stu-id="3268f-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="3268f-125">Cuando se cierra el cuadro de diálogo, el **DISMISSMODELESS** en la función de función para que la aplicación cliente se detendrá al llamar a la **ACCELERATEABSDI** de las llamadas MAPI en función (función).</span><span class="sxs-lookup"><span data-stu-id="3268f-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3268f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3268f-126">See also</span></span>



[<span data-ttu-id="3268f-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="3268f-127">ADRPARM</span></span>](adrparm.md)

