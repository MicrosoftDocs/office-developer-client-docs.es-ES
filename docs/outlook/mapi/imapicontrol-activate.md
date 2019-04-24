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
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280205"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="f7eca-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="f7eca-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="f7eca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7eca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7eca-105">Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación mediante programación cuando un usuario de la aplicación cliente hace clic en el control del botón.</span><span class="sxs-lookup"><span data-stu-id="f7eca-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="f7eca-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f7eca-106">Parameters</span></span>

 <span data-ttu-id="f7eca-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7eca-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f7eca-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f7eca-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f7eca-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f7eca-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="f7eca-110">a Identificador de la ventana principal del cuadro de diálogo en el que aparece el control de botón.</span><span class="sxs-lookup"><span data-stu-id="f7eca-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7eca-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7eca-111">Return value</span></span>

<span data-ttu-id="f7eca-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7eca-112">S_OK</span></span> 
  
> <span data-ttu-id="f7eca-113">El control de botón se activó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f7eca-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7eca-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7eca-114">Remarks</span></span>

<span data-ttu-id="f7eca-115">El método **IMAPIControl:: Activate** realiza tareas tras el clic del usuario en el control botón.</span><span class="sxs-lookup"><span data-stu-id="f7eca-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="f7eca-116">Cuando se produce el clic, como parte del procesamiento de la tabla de visualización, MAPI realiza una llamada \*\*\*\* a Activate después de llamar primero a [IMAPIControl:: GetState](imapicontrol-getstate.md) para determinar si el botón está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f7eca-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="f7eca-117">Para obtener más información acerca de cómo \*\*\*\* implementar activate y los otros métodos [IMAPIControl: IUnknown](imapicontroliunknown.md) , vea [control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f7eca-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7eca-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7eca-118">See also</span></span>



[<span data-ttu-id="f7eca-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="f7eca-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="f7eca-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7eca-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

