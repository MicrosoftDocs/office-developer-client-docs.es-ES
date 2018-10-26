---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580687"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="c84b0-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="c84b0-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="c84b0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c84b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c84b0-105">Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación de programación cuando un usuario de la aplicación cliente hace clic en el control de botón.</span><span class="sxs-lookup"><span data-stu-id="c84b0-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="c84b0-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c84b0-106">Parameters</span></span>

 <span data-ttu-id="c84b0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c84b0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c84b0-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c84b0-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c84b0-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c84b0-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c84b0-110">[entrada] Identificador de la ventana principal del cuadro de diálogo en el que aparece el control de botón.</span><span class="sxs-lookup"><span data-stu-id="c84b0-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c84b0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c84b0-111">Return value</span></span>

<span data-ttu-id="c84b0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c84b0-112">S_OK</span></span> 
  
> <span data-ttu-id="c84b0-113">El control botón se activó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c84b0-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c84b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c84b0-114">Remarks</span></span>

<span data-ttu-id="c84b0-115">El método **IMAPIControl::Activate** realiza tareas siguiendo hacer clic en un usuario el control de botón.</span><span class="sxs-lookup"><span data-stu-id="c84b0-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="c84b0-116">Una vez que se produce el clic, como parte del procesamiento de la tabla para mostrar, MAPI realiza una llamada a **Activar** después de la primera llamada [IMAPIControl::GetState](imapicontrol-getstate.md) para determinar si está habilitado el botón.</span><span class="sxs-lookup"><span data-stu-id="c84b0-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="c84b0-117">Para obtener más información acerca de cómo implementar **Activar** y la otra [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, vea [Implementación de objeto de Control](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c84b0-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c84b0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c84b0-118">See also</span></span>



[<span data-ttu-id="c84b0-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="c84b0-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="c84b0-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c84b0-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

