---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b7d4d758f7031c55aa3a23b662ec8727ea1e0719
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816378"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="7c16d-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="7c16d-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="7c16d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c16d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c16d-105">Define una función de devolución de llamada para teclas de aceleración de proceso en un cuadro de diálogo de la libreta de direcciones no modal.</span><span class="sxs-lookup"><span data-stu-id="7c16d-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c16d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7c16d-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c16d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c16d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7c16d-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="7c16d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="7c16d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7c16d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7c16d-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="7c16d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="7c16d-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="7c16d-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="7c16d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c16d-112">Parameters</span></span>

 <span data-ttu-id="7c16d-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7c16d-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="7c16d-114">[entrada] Un valor específico de la implementación utilizado para pasar información de interfaz de usuario a una función.</span><span class="sxs-lookup"><span data-stu-id="7c16d-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="7c16d-115">En las aplicaciones que se ejecutan en Microsoft Windows, _ulUIParam_ es el identificador de ventana primario para un cuadro de diálogo y es del tipo HWND, que se convierte en un **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="7c16d-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="7c16d-116">Un valor de cero indica que no hay ninguna ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="7c16d-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="7c16d-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="7c16d-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="7c16d-118">[entrada] Puntero a un mensaje de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c16d-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c16d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c16d-119">Return value</span></span>

<span data-ttu-id="7c16d-120">Una función con el prototipo **ACCELERATEABSDI** devuelve TRUE si controla el mensaje.</span><span class="sxs-lookup"><span data-stu-id="7c16d-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7c16d-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c16d-121">Remarks</span></span>

<span data-ttu-id="7c16d-122">Una función según el prototipo **ACCELERATEABSDI** sólo se utiliza con un cuadro de diálogo no modal, es decir, sólo si la aplicación cliente ha establecido el indicador DIALOG_SDI en el miembro _ulFlags_ de la estructura [ADRPARM](adrparm.md) .</span><span class="sxs-lookup"><span data-stu-id="7c16d-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="7c16d-123">Un cuadro de diálogo no modal comparte bucle de mensaje de Windows de la aplicación de cliente, en lugar de tener su propio bucle.</span><span class="sxs-lookup"><span data-stu-id="7c16d-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="7c16d-124">La aplicación, que controla el bucle de mensajes, no sabe qué teclas de aceleración usará el cuadro de diálogo, por lo que se llama una **ACCELERATEABSDI** según función para probar y actuar de teclas de aceleración, como CTRL + P para su impresión.</span><span class="sxs-lookup"><span data-stu-id="7c16d-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="7c16d-125">Llamadas de bucle de mensaje de un cliente la **ACCELERATEABSDI** en función (función) cuando el cliente invoca un cuadro de diálogo de la libreta de direcciones no modal con el método [IAddrBook::Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="7c16d-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="7c16d-126">Esta llamada se termina cuando MAPI llama a una función según el prototipo de función [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="7c16d-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

