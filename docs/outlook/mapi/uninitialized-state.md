---
title: Estado sin inicializar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425564"
---
# <a name="uninitialized-state"></a><span data-ttu-id="b9276-103">Estado sin inicializar</span><span class="sxs-lookup"><span data-stu-id="b9276-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="b9276-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9276-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9276-105">El estado sin inicializar es el estado inicial en que los objetos de formulario deben estar en la primera vez que se crean.</span><span class="sxs-lookup"><span data-stu-id="b9276-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="b9276-106">Los objetos de formulario se inicializan con los datos del mensaje cuando una aplicación cliente llama al método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) o [IPersistMessage:: Load](ipersistmessage-load.md) en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="b9276-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="b9276-107">En la tabla siguiente se describen las transiciones permitidas desde el estado Unitialized.</span><span class="sxs-lookup"><span data-stu-id="b9276-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="b9276-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="b9276-108">**IPersistMessage method**</span></span>|<span data-ttu-id="b9276-109">**Acción**</span><span class="sxs-lookup"><span data-stu-id="b9276-109">**Action**</span></span>|<span data-ttu-id="b9276-110">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="b9276-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b9276-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="b9276-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="b9276-112">Cargue el objeto Form con datos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b9276-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="b9276-113">Normal</span><span class="sxs-lookup"><span data-stu-id="b9276-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="b9276-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="b9276-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="b9276-115">Cargue el objeto de formulario con datos del mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="b9276-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="b9276-116">Normal</span><span class="sxs-lookup"><span data-stu-id="b9276-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="b9276-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="b9276-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="b9276-118">Devuelve Success o establece el último error en y devuelve E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="b9276-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="b9276-119">Sin inicializar</span><span class="sxs-lookup"><span data-stu-id="b9276-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="b9276-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b9276-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="b9276-121">Devolver el último error.</span><span class="sxs-lookup"><span data-stu-id="b9276-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="b9276-122">Sin inicializar</span><span class="sxs-lookup"><span data-stu-id="b9276-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="b9276-123">Otros [IPersistMessage:](ipersistmessageiunknown.md) métodos o métodos IUnknown de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="b9276-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="b9276-124">Establezca el último error en y devuelva E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="b9276-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="b9276-125">Sin inicializar</span><span class="sxs-lookup"><span data-stu-id="b9276-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9276-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="b9276-126">See also</span></span>



[<span data-ttu-id="b9276-127">Estado normal</span><span class="sxs-lookup"><span data-stu-id="b9276-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="b9276-128">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="b9276-128">Form States</span></span>](form-states.md)

