---
title: Estado no inicializado
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
# <a name="uninitialized-state"></a><span data-ttu-id="becdf-103">Estado no inicializado</span><span class="sxs-lookup"><span data-stu-id="becdf-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="becdf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="becdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="becdf-105">El estado Uninitialized es el estado inicial en el que deben estar los objetos de formulario cuando se crean por primera vez.</span><span class="sxs-lookup"><span data-stu-id="becdf-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="becdf-106">Los objetos de formulario se inicializan con datos de mensaje cuando una aplicación cliente llama al método [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="becdf-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="becdf-107">En la tabla siguiente se describen las transiciones permitidas desde el estado Unitialized.</span><span class="sxs-lookup"><span data-stu-id="becdf-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="becdf-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="becdf-108">**IPersistMessage method**</span></span>|<span data-ttu-id="becdf-109">**Acción**</span><span class="sxs-lookup"><span data-stu-id="becdf-109">**Action**</span></span>|<span data-ttu-id="becdf-110">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="becdf-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="becdf-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="becdf-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="becdf-112">Cargue el objeto de formulario con datos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="becdf-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="becdf-113">Normal</span><span class="sxs-lookup"><span data-stu-id="becdf-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="becdf-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="becdf-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="becdf-115">Cargue el objeto de formulario con datos del mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="becdf-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="becdf-116">Normal</span><span class="sxs-lookup"><span data-stu-id="becdf-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="becdf-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="becdf-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="becdf-118">Devuelve el resultado correcto o establece el último error en y devuelve E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="becdf-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="becdf-119">Sin inicializar</span><span class="sxs-lookup"><span data-stu-id="becdf-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="becdf-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="becdf-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="becdf-121">Devuelve el último error.</span><span class="sxs-lookup"><span data-stu-id="becdf-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="becdf-122">Sin inicializar</span><span class="sxs-lookup"><span data-stu-id="becdf-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="becdf-123">Otros [métodos de IPersistMessage : IUnknown](ipersistmessageiunknown.md) o de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="becdf-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="becdf-124">Establezca el último error en y devuelva E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="becdf-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="becdf-125">Sin inicializar</span><span class="sxs-lookup"><span data-stu-id="becdf-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="becdf-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="becdf-126">See also</span></span>



[<span data-ttu-id="becdf-127">Estado normal</span><span class="sxs-lookup"><span data-stu-id="becdf-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="becdf-128">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="becdf-128">Form States</span></span>](form-states.md)

