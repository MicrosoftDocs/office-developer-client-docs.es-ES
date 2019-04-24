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
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322130"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="49073-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="49073-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="49073-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49073-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49073-105">Define una función de devolución de llamada para procesar teclas de aceleración en un cuadro de diálogo de la libreta de direcciones sin modo.</span><span class="sxs-lookup"><span data-stu-id="49073-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49073-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="49073-106">Header file:</span></span>  <br/> |<span data-ttu-id="49073-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="49073-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="49073-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="49073-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="49073-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="49073-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="49073-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="49073-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="49073-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="49073-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="49073-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="49073-112">Parameters</span></span>

 <span data-ttu-id="49073-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="49073-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="49073-114">a Valor específico de la implementación que se usa para pasar información de la interfaz de usuario a una función.</span><span class="sxs-lookup"><span data-stu-id="49073-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="49073-115">En las aplicaciones que se ejecutan en Microsoft Windows, _ulUIParam_ es el controlador de la ventana principal de un cuadro de diálogo y es del tipo HWND, convertido a **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="49073-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="49073-116">Un valor de cero indica que no hay ventana principal.</span><span class="sxs-lookup"><span data-stu-id="49073-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="49073-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="49073-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="49073-118">a Puntero a un mensaje de Windows.</span><span class="sxs-lookup"><span data-stu-id="49073-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="49073-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49073-119">Return value</span></span>

<span data-ttu-id="49073-120">Una función con el prototipo **ACCELERATEABSDI** devuelve true si controla el mensaje.</span><span class="sxs-lookup"><span data-stu-id="49073-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="49073-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49073-121">Remarks</span></span>

<span data-ttu-id="49073-122">Una función basada en el prototipo **ACCELERATEABSDI** se usa solo con un cuadro de diálogo no modal, es decir, solo si la aplicación cliente ha establecido la marca DIALOG_SDI en el miembro _ulFlags_ de la estructura [ADRPARM](adrparm.md) .</span><span class="sxs-lookup"><span data-stu-id="49073-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="49073-123">Un cuadro de diálogo no modal comparte el bucle de mensajes de Windows de la aplicación cliente, en lugar de tener su propio bucle.</span><span class="sxs-lookup"><span data-stu-id="49073-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="49073-124">La aplicación, que controla el bucle de mensajes, no sabe qué teclas de aceleración utiliza el cuadro de diálogo, por lo que llama a una función basada en **ACCELERATEABSDI** para probar y actuar sobre teclas de aceleración, como Ctrl + P para imprimir.</span><span class="sxs-lookup"><span data-stu-id="49073-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="49073-125">El bucle de mensajes de un cliente llama a la función basada en **ACCELERATEABSDI** cuando el cliente invoca un cuadro de diálogo de la libreta de direcciones sin modo con el método [IAddrBook:: Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="49073-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="49073-126">Esta llamada finaliza cuando MAPI llama a una función basada en el prototipo de función [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="49073-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

