---
title: IUnknown IMAPIControl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280144"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="a8c2c-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8c2c-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="a8c2c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c2c-105">Habilita y deshabilita un control de botón y realiza tareas cuando un usuario de una aplicación cliente hace clic en el control habilitado.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="a8c2c-106">Los proveedores de servicios implementan objetos de control para crear botones personalizados en cuadros de diálogo, como hojas de propiedades de configuración, que se definen mediante tablas de presentación.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="a8c2c-107">Para obtener más información acerca de cómo trabajar con tablas de visualización y objetos de control, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a8c2c-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8c2c-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a8c2c-108">Header file:</span></span>  <br/> |<span data-ttu-id="a8c2c-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a8c2c-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a8c2c-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="a8c2c-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a8c2c-111">Objetos de control</span><span class="sxs-lookup"><span data-stu-id="a8c2c-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="a8c2c-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a8c2c-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8c2c-113">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a8c2c-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="a8c2c-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a8c2c-114">Called by:</span></span>  <br/> |<span data-ttu-id="a8c2c-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c2c-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8c2c-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="a8c2c-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a8c2c-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="a8c2c-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="a8c2c-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="a8c2c-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="a8c2c-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="a8c2c-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a8c2c-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="a8c2c-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a8c2c-121">Volvió</span><span class="sxs-lookup"><span data-stu-id="a8c2c-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="a8c2c-122">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="a8c2c-123">Activate</span><span class="sxs-lookup"><span data-stu-id="a8c2c-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="a8c2c-124">Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación mediante programación cuando un usuario de la aplicación cliente hace clic en el control del botón.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="a8c2c-125">GetState</span><span class="sxs-lookup"><span data-stu-id="a8c2c-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="a8c2c-126">Recupera un valor que indica si el control de botón está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8c2c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8c2c-127">See also</span></span>



[<span data-ttu-id="a8c2c-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c2c-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

