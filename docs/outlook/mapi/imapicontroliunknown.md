---
title: IMAPIControl IUnknown
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
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817207"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="8403e-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8403e-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="8403e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8403e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8403e-105">Habilita y deshabilita un control de botón y realiza tareas cuando un usuario de una aplicación de cliente hace clic en el control habilitado.</span><span class="sxs-lookup"><span data-stu-id="8403e-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="8403e-106">Proveedores de servicios de implementan objetos de control para crear botones personalizados en los cuadros de diálogo, como las hojas de propiedades de configuración, que se definen mediante el uso de las tablas para mostrar.</span><span class="sxs-lookup"><span data-stu-id="8403e-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="8403e-107">Para obtener más información acerca de cómo trabajar con tablas para mostrar y controlar objetos, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8403e-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8403e-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8403e-108">Header file:</span></span>  <br/> |<span data-ttu-id="8403e-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8403e-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8403e-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="8403e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="8403e-111">Objetos de control</span><span class="sxs-lookup"><span data-stu-id="8403e-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="8403e-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="8403e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="8403e-113">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8403e-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="8403e-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8403e-114">Called by:</span></span>  <br/> |<span data-ttu-id="8403e-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="8403e-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="8403e-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="8403e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8403e-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="8403e-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="8403e-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="8403e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="8403e-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="8403e-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8403e-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="8403e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8403e-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="8403e-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="8403e-122">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior.</span><span class="sxs-lookup"><span data-stu-id="8403e-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="8403e-123">Activate</span><span class="sxs-lookup"><span data-stu-id="8403e-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="8403e-124">Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación de programación cuando un usuario de la aplicación cliente hace clic en el control de botón.</span><span class="sxs-lookup"><span data-stu-id="8403e-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="8403e-125">GetState</span><span class="sxs-lookup"><span data-stu-id="8403e-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="8403e-126">Recupera un valor que indica si el control de botón está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8403e-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8403e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8403e-127">See also</span></span>



[<span data-ttu-id="8403e-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8403e-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

